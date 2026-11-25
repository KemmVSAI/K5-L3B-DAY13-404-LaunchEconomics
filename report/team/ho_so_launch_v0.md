# Hồ sơ launch v0 · Trợ lý hoàn phí LogiX-VN · Gate 2a

Một trang. Cột trạng thái chỉ nhận: **Xong, có bằng chứng · Chưa · Giả lập**. Mục nào dựa trên cột `_simulated` ghi Giả lập. Người phụ trách là một vai trò, không ghi "cả đội". Gate 2a chỉ duyệt kế hoạch pilot: không viết như thể trợ lý đã được duyệt chạy chính thức (xem quy tắc 5 trong `README.md`).

Nhóm: K5-L3B-DAY13-404-LaunchEconomics · Lớp: L3B

| Mục | Con số chính | Trạng thái | Người phụ trách |
| --- | --- | --- | --- |
| 1 · Chi phí mỗi việc thành công | 4.472 đ/việc thành công [simulated] (16,3× hoá đơn 274,7 đ/yc); phạm vi `noi_dia + hang_nang` có cố định 40 tr/tháng = 4.599 đ/việc [simulated] | Giả lập | PM trợ lý hoàn phí |
| 2 · Ba yếu tố nhạy nhất | 1. Số ca làm lại (+51,8%); 2. Tỉ lệ xem lại (+40,7%); 3. Lương nhân viên (+23,1%) [simulated] | Giả lập | PM trợ lý hoàn phí |
| 3 · So với nhân viên tự làm | Toàn mẫu cả hệ thống: 5.865 đ/yc = 0,49× của 12.000 đ [simulated]; nếu xem lại 100% ở phạm vi pilot: 11.743–12.415 đ (0,98×–1,03×) [simulated] | Giả lập | PM trợ lý hoàn phí |
| 4 · Chỉ số chính, chỉ số dùng, chỉ số an toàn | Đợt chạy thử: Chính 82,83% (994/1.200); Dùng 27,12% bỏ qua gợi ý (48/177); An toàn 4,25% mở lại 7d (51/1.200); 10 event có `trace_id` | Xong, có bằng chứng | Kỹ sư trưởng agent |
| 5 · Bảng lỗi và cách khắc phục | 20 ca đủ 5 loại Google PAIR (đồng thuận 20/20 = 100%); 5 ca khắc phục có cách phát hiện đo được và vai trò phụ trách | Xong, có bằng chứng | Kỹ sư trưởng agent |
| 6 · Pilot plan | Chia theo nhân viên 20+20, đối chứng đồng thời, MDE 6 điểm (`n = 859`/nhóm, `m >= 299`, `DE = 6,96`); nếu hiệu ứng thật 5 điểm thì **power còn 0,64**; rollback tắt cờ trong 30 phút | Giả lập | Giám đốc vận hành LogiX-VN |
| 7 · Rủi ro kinh tế | Làm lại ×2 lên 6.787 đ; xem lại 100% lên 11.743–12.415 đ (0,98×–1,03×); khối lượng giảm nửa làm cố định tăng gấp đôi lên 5.784 đ [simulated] | Giả lập | PM trợ lý hoàn phí |

**Đề xuất:** **Go có điều kiện** — chỉ mở pilot cho `noi_dia` (0,22× [simulated]) và `hang_nang` (0,69× [simulated]) trên 12 depot; loại `quoc_te` (1,88× [simulated], thành công 27,3%) và `doi_tac` (0,85× [simulated], điều khoản riêng). Không khẳng định trợ lý đã cải thiện kết quả vì đợt chạy thử không có nhóm đối chứng.

- Điều kiện 1 (An toàn hệ thống): Sửa khoá chống trùng lệnh hoàn và đối soát sổ cái hàng giờ (ca 7, 20) — **Kỹ sư trưởng agent**, hoàn tất trước ngày bắt đầu pilot.
- Điều kiện 2 (Thống kê & Rollback): Ký chấp nhận đánh đổi MDE 6 điểm (công khai power giảm còn **0,64** nếu tác động thật là 5 điểm) và cơ chế rollback tắt cờ trong **30 phút** về luồng nhân viên tự làm (nếu mở lại 7 ngày vượt đối chứng ≥ 2 điểm hoặc trần 6%, hoặc ≥ 1 ca hoàn trùng trong 3 ngày) — **Giám đốc vận hành LogiX-VN**, trước ngày bắt đầu pilot.
- Điều kiện 3 (Đo thật & Sử dụng): Bật đủ 10 event có `trace_id` để thay thế phút `simulated` bằng phút đo thật sau tuần 1; theo dõi tỉ lệ bỏ qua gợi ý (dừng nếu > 40% trong 1 tuần) — **Kỹ sư trưởng agent** & **Trưởng nhóm CSKH**, kiểm tra cuối tuần 1 và hàng tuần.
- Điều kiện 4 (Kiểm soát chi phí xem lại): Áp dụng lộ trình giảm tỉ lệ xem lại theo bậc khi sửa + bỏ < 15% (tránh mức xem lại 100% vốn tốn **11.743–12.415 đ = 0,98×–1,03× [simulated]**) và giữ chi phí đo thật ≤ 8.000 đ/việc trong 2 tuần liên tiếp trước khi quyết định tại ngày **2027-01-05** — **PM trợ lý hoàn phí** & **Trưởng nhóm CSKH**, kiểm tra cuối bước 0.25 và ngày 2027-01-05.
