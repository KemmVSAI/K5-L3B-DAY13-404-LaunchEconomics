# Báo cáo nhóm

Báo cáo ngắn, tối đa 2 trang. Số liệu chi tiết nằm trong các file hồ sơ; ở đây chỉ dẫn lại con số chính.

## 1. Thông tin nhóm

- Tên nhóm: K5-L3B-DAY13-404-LaunchEconomics
- Lớp: L3B
- Thành viên: xem `TEAM.md`

## 2. Mục tiêu và cách tiếp cận

Nhóm dùng dữ liệu giả lập của 1.200 yêu cầu và bám năm checkpoint A–E. CP1–CP2 tính chi phí và độ nhạy; CP3 phân loại 20 ca lỗi độc lập; CP4 chọn pilot theo nhân viên; CP5 định nghĩa chỉ số, rủi ro và hồ sơ Gate 2a.

## 3. Giải pháp

Nhóm tính chi phí và độ nhạy trong `bang_chi_phi.md`, phân loại 20 ca lỗi trong `bang_loi.md`, thiết kế pilot trong `pilot_plan.yaml`, định nghĩa chỉ số trong `chi_so.md` và tổng hợp quyết định trong `ho_so_launch_v0.md`.

## 4. Kết quả

Kết quả chính là **5.865 đ/yêu cầu [simulated]**, bằng `0,49×` chi phí nhân viên tự làm 12.000 đ. Nhóm đề xuất Go có điều kiện cho `noi_dia` và `hang_nang`, loại `quoc_te` vì **1,88×**. Pilot dùng 20 nhân viên đối chứng và 20 nhân viên can thiệp, MDE 6 điểm.

Kết quả duyệt chéo từ nhóm 3npc: **20/30 điểm — Go có điều kiện**. Điểm thành phần: đề xuất khớp bằng chứng **5/10**, số giả lập và phạm vi **10/10**, pilot ra quyết định **5/10**.

Nhận xét chính của hội đồng là hồ sơ chưa làm nổi bật power còn khoảng **0,64** nếu hiệu ứng thực chỉ 5 điểm, kịch bản xem lại 100% **11.743–12.415 đ/việc**, lộ trình giảm xem lại, thời hạn của ngưỡng 40% và cơ chế rollback. Đây là các điểm nhóm cần trình bày rõ khi bảo vệ.

## 5. Khó khăn và cách xử lý

Khó khăn chính là giới hạn cỡ mẫu khi chia theo cụm và rủi ro xem lại/làm lại chiếm chi phí; nhóm xử lý bằng cách ghi rõ đánh đổi, luật dừng và event cần đo. Khi duyệt chéo, nhóm được góp ý cần đưa các bất lợi này lên phần kết luận thay vì chỉ để trong bảng chi tiết.

## 6. Tổng hợp đóng góp

Chi tiết đóng góp của bốn thành viên nằm trong `TEAM.md` và các báo cáo cá nhân.

## 7. Hạn chế và hướng cải thiện

Sau góp ý duyệt chéo, nhóm đã cập nhật trực tiếp bốn điểm vào `ho_so_launch_v0.md`: (1) công khai đánh đổi power còn `0,64` ở MDE 5 điểm; (2) nêu rõ chi phí xem lại 100% (`11.743–12.415 đ/việc [simulated]`) và lộ trình giảm xem lại theo bậc để giữ dưới `8.000 đ/việc`; (3) bổ sung thời hạn rollback `30 phút` và ngưỡng dừng `> 40% trong 1 tuần`; (4) giao toàn bộ mục và điều kiện cho đúng vai trò có thẩm quyền (`Giám đốc vận hành LogiX-VN`, `PM trợ lý hoàn phí`, `Kỹ sư trưởng agent`, `Trưởng nhóm CSKH`) thay vì ghi `Người kiểm số`. Hạn chế còn lại là chi phí thời gian vẫn ở mức `[simulated]`, nên pilot phải bật đủ event `trace_id` và đo thật từ tuần 1 trước ngày quyết định `2027-01-05`. Nhóm không diễn giải số liệu chạy thử hiện tại như bằng chứng trợ lý đã cải thiện kết quả.

## 8. Tài liệu tham khảo

- Erol và cộng sự, *Cost-of-Pass: An Economic Framework for Evaluating Language Models* ([arxiv.org/abs/2504.13359](https://arxiv.org/abs/2504.13359)).
- Google PAIR, *People + AI Guidebook*, chương "Errors + Graceful Failure" ([pair.withgoogle.com](https://pair.withgoogle.com)).
- Tài liệu thư viện `statsmodels`, lớp `NormalIndPower` (`statsmodels.stats.power`).
- Bộ dữ liệu giả lập và hướng dẫn Lab 13: `docs/du_lieu_va_cong_thuc.md`, `docs/Lab13_Huong_dan_chi_tiet_buoi_chieu.md`.
