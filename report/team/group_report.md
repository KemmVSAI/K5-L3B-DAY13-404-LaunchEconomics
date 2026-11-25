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

Trước khi thuyết trình, nhóm cần làm rõ bốn điểm: (1) công khai đánh đổi power `0,64` ở MDE 5 điểm; (2) nêu B4 và lộ trình hạ tỉ lệ xem lại để giữ dưới 8.000 đ/việc; (3) ghi rõ rollback có hiệu lực trong 30 phút; (4) giao điều kiện cho đúng vai trò có thẩm quyền thay vì ghi chung là “Người kiểm số”. Hạn chế là nhiều chi phí vẫn [simulated], nên pilot phải ghi event và kiểm tra luật dừng trước quyết định 2027-01-05. Nhóm không được diễn giải số liệu hiện tại như bằng chứng trợ lý đã cải thiện kết quả.

## 8. Tài liệu tham khảo
