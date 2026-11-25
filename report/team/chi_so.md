# Đặc tả chỉ số, event và rủi ro kinh tế · Nhiệm vụ E1, E2

## E1 · Đặc tả chỉ số

| Loại | Chỉ số | Công thức | Tính thử trên 1.200 yêu cầu |
| --- | --- | --- | --- |
| Chính (kết quả) | % yêu cầu đóng trong 24 giờ và không mở lại trong 7 ngày | `dong_trong_24h` bằng 1 và `mo_lai_trong_7_ngay` bằng 0, chia tổng số yêu cầu | **82,83%** (994 / 1.200) |
| Dùng | Tỉ lệ bỏ qua gợi ý | `quyet_dinh_xem_lai` là `sua` hoặc `bo`, chia số yêu cầu được xem lại | **27,12%** (48 / 177) |
| An toàn | Tỉ lệ lỗi lọt đến khách | `mo_lai_trong_7_ngay` bằng 1, chia tổng số yêu cầu | **4,25%** (51 / 1.200) |
| Dùng | Tỉ lệ mở trợ lý ở nhóm can thiệp | Số yêu cầu nhóm can thiệp có `agent_suggestion_shown` chia tổng số yêu cầu giao cho nhóm can thiệp | Không cần tính |
| An toàn | Tỉ lệ đơn hoàn sai tiền qua kiểm tra mẫu hàng tuần | Số đơn `lech_tien != 0` trong `audit_sample_checked` chia tổng số đơn kiểm tra mẫu (100 đơn/tuần) | Không cần tính |

Chỉ số trong đợt chạy thử là **82,83%** (chỉ có 1 nhóm chạy thử, không viết "trợ lý đã nâng chỉ số" vì chưa có nhóm đối chứng).

## Danh sách event

Ít nhất sáu event, mỗi event có `trace_id` để nối với trace của agent.

| Event | Ai tạo | Thuộc tính chính | Thời điểm |
| --- | --- | --- | --- |
| `refund_request_created` | App khách | `request_id, loai, so_tien_vnd, depot, arm, trace_id` | Khi khách gửi yêu cầu hoàn phí |
| `agent_run_completed` | Agent | `request_id, attempt, tokens_in, tokens_out, tool_calls, status, trace_id` | Sau mỗi lần chạy (kể cả lần lỗi) |
| `agent_suggestion_shown` | Giao diện CSKH | `request_id, staff_id, so_tien_de_xuat, trace_id` | Khi gợi ý của trợ lý hiển thị cho nhân viên |
| `staff_review_decision` | Nhân viên CSKH | `request_id, staff_id, quyet_dinh (giu/sua/bo), phut_xem_lai, trace_id` | Khi nhân viên bấm giữ, sửa hoặc bỏ gợi ý |
| `staff_rework_completed` | Nhân viên CSKH | `request_id, staff_id, phut_lam_lai, ly_do, trace_id` | Khi nhân viên hoàn tất làm lại ca sai |
| `handoff_to_staff` | Agent | `request_id, reason, tom_tat, trace_id` | Khi trợ lý chuyển ca sang nhân viên xử lý |
| `refund_ledger_write` | Dịch vụ sổ cái | `request_id, order_id, idempotency_key, so_tien, ket_qua, trace_id` | Khi ghi nhận lệnh hoàn tiền vào sổ cái |
| `ticket_closed` | Hệ thống ticket | `request_id, closed_at, trong_24h, trace_id` | Khi đóng yêu cầu hoàn phí |
| `ticket_reopened` | Khách / Ticket | `request_id, reopened_at, trong_7_ngay, reason, trace_id` | Khi khách mở lại yêu cầu trong 7 ngày |
| `audit_sample_checked` | Kế toán | `request_id, so_tien_da_hoan, so_tien_dung, lech_tien, trace_id` | Kiểm tra mẫu 100 đơn hàng tuần |

**Kiểm tra chéo:** với mỗi chỉ số ở bảng E1, ghi event dùng để tính. Chỉ số nào không tính được từ danh sách event thì chưa đo được.

- **Chỉ số chính:** tính từ `refund_request_created`, `ticket_closed` (`trong_24h == 1`) và không có `ticket_reopened` (`trong_7_ngay == 1`) cùng `trace_id`/`request_id`.
- **Chỉ số dùng:** tính từ `staff_review_decision` (`quyet_dinh in ['sua', 'bo']` chia tổng số lượt xem lại).
- **Chỉ số an toàn:** tính từ `ticket_reopened` (`trong_7_ngay == 1`) chia `refund_request_created`.
- **Chỉ số tự đề xuất:** tính từ `agent_suggestion_shown` và `audit_sample_checked`; các event này cũng giúp kiểm tra mức sử dụng và lỗi tiền.

## E2 · Rủi ro kinh tế

Ít nhất hai dòng, số lấy từ bảng độ nhạy (`bang_chi_phi.md`).

| Rủi ro | Tác động đã tính | Dấu hiệu theo dõi | Hành động | Người phụ trách |
| --- | --- | --- | --- | --- |
| Số ca làm lại tăng gấp đôi | Chi phí mỗi việc thành công tăng **+51,8%**, lên **6.787 đ [simulated]** | Tỉ lệ ca phải làm lại theo tuần > 7% | Thu hẹp phạm vi về `noi_dia`, rà soát 20 trace làm lại | PM trợ lý hoàn phí |
| Phải xem lại 100% kéo dài | Chi phí lên **11.743–12.415 đ [simulated]**, mất lợi ích tiết kiệm | Tỉ lệ xem lại > 50% ở rollout 0,25 hoặc > 5 phút/ca | Giảm tỉ lệ xem lại theo bậc khi sửa + bỏ < 15% trong 1 tuần | Trưởng nhóm CSKH |
| Khối lượng giảm một nửa | Chi phí cố định/việc tăng **1.185 → 2.370 đ**, CPS **5.784 đ [simulated]** | Việc thành công/tuần < 50% kế hoạch trong 2 tuần | Tạm dừng mở rộng, rà lại chi phí hạ tầng | PM trợ lý hoàn phí |
