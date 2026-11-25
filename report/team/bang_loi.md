# Bảng lỗi và cách khắc phục · Nhiệm vụ C

20 ca lỗi nằm trong `docs/Ngay13_Lab13_De_bai_hoc_vien.docx`. Năm loại theo Google PAIR: **Do người dùng · Hệ thống · Ngữ cảnh · Giới hạn hệ thống · Ngầm**. Gắn nhãn theo nguyên nhân gốc, không theo chỗ cần sửa.

## Hai bộ nhãn độc lập

Người gắn nhãn 1: Cao Trung Hiếu · Người gắn nhãn 2: Đinh Quốc Việt (gắn trong 8 phút, không trao đổi)

| Ca | Nhãn người 1 | Nhãn người 2 | Trùng? | Nhãn thống nhất |
| --: | --- | --- | --- | --- |
| 1 | Do người dùng | Do người dùng | Có | Do người dùng |
| 2 | Hệ thống | Hệ thống | Có | Hệ thống |
| 3 | Ngữ cảnh | Ngữ cảnh | Có | Ngữ cảnh |
| 4 | Giới hạn hệ thống | Giới hạn hệ thống | Có | Giới hạn hệ thống |
| 5 | Ngầm | Ngầm | Có | Ngầm |
| 6 | Do người dùng | Do người dùng | Có | Do người dùng |
| 7 | Hệ thống | Hệ thống | Có | Hệ thống |
| 8 | Hệ thống | Hệ thống | Có | Hệ thống |
| 9 | Do người dùng | Do người dùng | Có | Do người dùng |
| 10 | Ngữ cảnh | Ngữ cảnh | Có | Ngữ cảnh |
| 11 | Giới hạn hệ thống | Giới hạn hệ thống | Có | Giới hạn hệ thống |
| 12 | Ngầm | Ngầm | Có | Ngầm |
| 13 | Giới hạn hệ thống | Giới hạn hệ thống | Có | Giới hạn hệ thống |
| 14 | Do người dùng | Do người dùng | Có | Do người dùng |
| 15 | Hệ thống | Hệ thống | Có | Hệ thống |
| 16 | Ngữ cảnh | Ngữ cảnh | Có | Ngữ cảnh |
| 17 | Ngầm | Ngầm | Có | Ngầm |
| 18 | Ngữ cảnh | Ngữ cảnh | Có | Ngữ cảnh |
| 19 | Giới hạn hệ thống | Giới hạn hệ thống | Có | Giới hạn hệ thống |
| 20 | Hệ thống | Hệ thống | Có | Hệ thống |

**Tỉ lệ đồng thuận:** 20 / 20 = 100%

## Căn cứ nhãn của người gắn nhãn 1

Mỗi ca được phân loại theo nguyên nhân gốc và câu hỏi nhận ra của hướng dẫn.

| Ca | Nhãn | Căn cứ từ chính mô tả ca |
| --: | --- | --- |
| 1 | Do người dùng | Khách nhập thiếu hai chữ số tài khoản; ngân hàng báo lỗi là hệ quả của đầu vào sai. |
| 2 | Hệ thống | Gọi tool với tham số hàng thường cho kiện 28 kg, trái thiết kế; sai lộ ra khi khách mở lại. |
| 3 | Ngữ cảnh | Hoàn về ví LogiX trong 5 phút đúng thiết kế; khách giả định tiền về ngân hàng. |
| 4 | Giới hạn hệ thống | LogiX không có dữ liệu chặng hãng nước ngoài; trợ lý chuyển nhân viên. |
| 5 | Ngầm | 14 đơn hoàn thừa 12.000 đ; không khách báo, chỉ lộ qua kiểm tra mẫu. |
| 6 | Do người dùng | Khách chọn sai mục giao trễ cho hàng vỡ; trợ lý làm đúng luồng đã chọn. |
| 7 | Hệ thống | Sổ cái lỗi 503 nhưng trợ lý vẫn báo đã hoàn thành; trái thiết kế. |
| 8 | Hệ thống | Dẫn Điều 7.2 không tồn tại; trích dẫn sai nhìn thấy được, không phải lỗi ngầm. |
| 9 | Do người dùng | Khách nhập mã đơn sàn thay mã vận đơn; việc không gợi ý là cách khắc phục. |
| 10 | Ngữ cảnh | Từ chối bất khả kháng đúng chính sách nhưng không khớp kỳ vọng từ giao diện. |
| 11 | Giới hạn hệ thống | Trợ lý không xử lý được tin nhắn thoại, là dạng đầu vào ngoài khả năng. |
| 12 | Ngầm | Câu trả lời đúng nhưng token D05 gấp 3 lần suốt 3 tuần mà không ai thấy. |
| 13 | Giới hạn hệ thống | Bảo hiểm hàng hóa ngoài phạm vi trợ lý. |
| 14 | Do người dùng | Khách bấm nhầm xác nhận đã nhận tiền. |
| 15 | Hệ thống | Tính hoàn 100% thay vì 50% theo chính sách; nhân viên bắt được trước khi gửi. |
| 16 | Ngữ cảnh | Gửi thông báo lúc 2:14 sáng đúng thiết kế gửi ngay, nhưng gây phiền cho khách. |
| 17 | Ngầm | Dùng bảng giá cũ cho 212 đơn trong 9 ngày mà không ai nhận ra. |
| 18 | Ngữ cảnh | Tính đúng 30.000 × 50% = 15.000 nhưng thiếu cách giải thích. |
| 19 | Giới hạn hệ thống | Dữ liệu chỉ có 12 tháng, đơn 14 tháng không tra được và được chuyển nhân viên. |
| 20 | Hệ thống | Hoàn hai lần vì thiếu khóa chống trùng, trái thiết kế. |

## Quy tắc phân biệt cho các ca không trùng

Mỗi ca không trùng một câu. Đồng thuận dưới 80% thì ghi định nghĩa đã viết lại.

- Ca 6 và 9 là Do người dùng vì gốc lỗi là khách chọn sai mục hoặc nhập sai mã; việc trợ lý không gợi ý là cách khắc phục.
- Ca 13 là Giới hạn hệ thống vì yêu cầu ngoài phạm vi, dù cách trợ lý xử lý còn chưa tốt.
- Ca 8 và 15 là Hệ thống vì sai đã lộ ra; Ngầm chỉ dùng khi không ai nhận ra cho tới khi kiểm tra.
- Ca 18 là Ngữ cảnh vì số tiền đúng, chỉ giả định khách hiểu cách tính là không khớp.
- Ca 12 là Ngầm vì kết quả đúng nhưng chi phí cao kéo dài mà không ai phát hiện.

## Bảng khắc phục cho 5 ca, mỗi loại một ca

Cách phát hiện phải đo được (event, ngưỡng, tần suất). Người phụ trách là một vai trò, không ghi "cả đội".

| Ca | Loại lỗi | Phát hiện bằng gì | Khắc phục thế nào | Ai phụ trách |
| --: | --- | --- | --- | --- |
| 14 | Do người dùng | Event `confirm_received_clicked` sau đó có `reopen_request` hoặc khiếu nại trong 7 ngày; cảnh báo khi vượt 1%/tuần | Thêm xác nhận hai lần và cho mở lại yêu cầu trong 48 giờ | PM trợ lý hoàn phí |
| 20 | Hệ thống | Đối soát mỗi giờ: một `order_id` có từ 2 `refund_issued`; ngưỡng 0 ca | Thêm khóa chống trùng theo đơn; lệnh thứ hai trả kết quả lệnh đầu | Kỹ sư trưởng agent |
| 16 | Ngữ cảnh | Event `notification_sent` ngoài 22:00–07:00; ngưỡng 0 tin/tuần | Giữ tin đến 07:00 và cho khách chọn giờ nhận | Trưởng nhóm CSKH |
| 19 | Giới hạn hệ thống | Event `handoff_to_staff` với `reason=ngoai_du_lieu_12_thang`; theo dõi hàng tuần | Từ chối sớm đơn quá 12 tháng và chuyển kèm tóm tắt | PM trợ lý hoàn phí |
| 12 | Ngầm | So token/yêu cầu theo depot; cảnh báo >1,5 lần trung vị trong 3 ngày liên tiếp | Sửa tool D05, thêm cảnh báo chi phí và ghi phiên bản schema vào trace | Kỹ sư trưởng agent |
