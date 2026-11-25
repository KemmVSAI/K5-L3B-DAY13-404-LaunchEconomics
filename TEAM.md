# Team

## Thông tin nhóm

- Tên nhóm: K5-L3B-DAY13-404-LaunchEconomics
- Lớp: L3B
- Repo nhóm: `K5-L3B-DAY13-404-LaunchEconomics` (xem [SUBMISSION.md](SUBMISSION.md))
- URL repo, nhánh nộp, commit chốt: https://github.com/KemmVSAI/K5-L3B-DAY13-404-LaunchEconomics (nhánh `main`)

## Thành viên

| STT | Họ tên | MSSV | Email | GitHub | Vai trò |
| --: | ------ | ---- | ----- | ------ | ------- |
|   1 | Đinh Quốc Việt | 2A202603885 | 26ai.vietdq3@vinuni.edu.vn | KemmVSAI | Người gắn nhãn 2, kiêm giữ hồ sơ |
|   2 | Cao Trung Hiếu | 2A202603993 | 26ai.hieuct@vinuni.edu.vn | HieuCaoTlu | Người gắn nhãn 1 |
|   3 | Vũ Đình Huy | 2A202603985 | huyvudinh1608@gmail.com | VNno1TH | Người viết code |
|   4 | Cao Phạm Thành Đạt | 2A202603970 | 26ai.datcpt@vinuni.edu.vn | tcaopham216-gif | Người kiểm số |

Bốn vai của lab:

- **Người viết code:** viết và chạy `src/lab13.py`.
- **Người kiểm số:** tính tay một con số để đối chiếu, điền bảng.
- **Người gắn nhãn 1:** đọc đề, theo dõi điều kiện "Xong khi"; gắn nhãn 20 ca độc lập ở CP3.
- **Người gắn nhãn 2, kiêm giữ hồ sơ:** điền `report/team/ho_so_launch_v0.md` từ đầu buổi; gắn nhãn 20 ca độc lập ở CP3.

Đổi người viết code sau giờ giải lao, để ít nhất hai người trong nhóm tự tay tính được chi phí.

## Cá nhân

Mỗi thành viên đồng thời tạo một báo cáo riêng trong `report/` theo dạng:

```text
report/team/MSSV_HoTen.md
```

Ví dụ: `report/team/20241234_NguyenVanAn.md`.

## Đinh Quốc Việt - 2A202603885

### Phần việc phụ trách

- Người gắn nhãn 2, kiêm giữ hồ sơ: gắn nhãn độc lập 20 ca CP3, giữ `report/team/ho_so_launch_v0.md` và hoàn thiện hồ sơ nhóm.

### Đóng góp cụ thể

- Hoàn thiện bộ nhãn độc lập 20 ca lỗi, đối chiếu đạt đồng thuận 20/20 = 100% trong `report/team/bang_loi.md`.
- Tổng hợp `ho_so_launch_v0.md`, chấm chéo nhóm `3npc` trong `phieu_cham.md` và cập nhật `group_report.md`.

### Bằng chứng

- `report/team/bang_loi.md`, `report/team/ho_so_launch_v0.md`, `report/team/phieu_cham.md`, `report/team/group_report.md`, `report/team/2A202603885_DinhQuocViet.md`.

## Cao Trung Hiếu - 2A202603993

### Phần việc phụ trách

- Người gắn nhãn 1: gắn nhãn 20 ca lỗi (CP3) và theo dõi điều kiện "Xong khi" của các checkpoint.

### Đóng góp cụ thể

- Gắn nhãn 20 ca lỗi theo 5 loại Google PAIR, ghi căn cứ cho từng ca và quy tắc phân biệt các ca dễ lẫn.
- Soạn bảng khắc phục 5 ca (đủ 5 loại) với cách phát hiện đo được và vai trò phụ trách.

### Bằng chứng

- `report/team/bang_loi.md`, `report/team/2A202603993_CaoTrungHieu.md`.

## Vũ Đình Huy - 2A202603985

### Phần việc phụ trách

- Người viết code: xây dựng và chạy `src/lab13.py` cho CP1, CP2, CP4 và tính thử chỉ số E1 (CP5).

### Đóng góp cụ thể

- Cài đặt các hàm A1 (`1,20 · 1,25 · 1,25`), mô hình chi phí A2–A4, phân tích độ nhạy B1–B4 trong `src/lab13.py` và điền `report/team/bang_chi_phi.md`.
- Viết phần tính cỡ mẫu D1 (`1.251`, `859`, `m >= 299`, `power = 0,64`), hoàn thiện `report/team/pilot_plan.yaml` và `report/team/chi_so.md` (E1, event, E2).

### Bằng chứng

- `src/lab13.py`, `report/team/bang_chi_phi.md`, `report/team/pilot_plan.yaml`, `report/team/chi_so.md`, `report/team/2A202603985_VuDinhHuy.md`.

## Cao Phạm Thành Đạt - 2A202603970

### Phần việc phụ trách

- Người kiểm số: tính tay đối chiếu số liệu và kiểm tra bảng chi phí, độ nhạy và rủi ro kinh tế.

### Đóng góp cụ thể

- Đối chiếu các con số chi phí chính (A2–A4, B1–B4) với kết quả chạy từ `src/lab13.py` và rà soát nhãn `simulated`.

### Bằng chứng

- `report/team/bang_chi_phi.md`, `report/team/chi_so.md`, `report/team/ho_so_launch_v0.md`, `report/team/2A202603970_CaoPhamThanhDat.md`.
