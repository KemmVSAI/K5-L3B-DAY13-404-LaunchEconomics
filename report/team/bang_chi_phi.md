# Bảng chi phí · Nhiệm vụ A và B

Số tính bằng `src/lab13.py`. Mọi con số tính từ cột `_simulated` ghi nhãn `simulated`. Mỗi câu trả lời không quá ba dòng, có ít nhất một con số.

## A1 · Ba phép thử đáp án biết trước

| Phép thử (p = 0,8) | Kết quả của nhóm |
| --- | --- |
| Số lần chạy trung bình, tối đa 2 lần | 1,20 |
| Số lần chạy trung bình, chạy đến khi đúng | 1,25 |
| Hệ số chi phí mỗi việc thành công, tối đa 3 lần | 1,25 |

## A2 · Mô hình chi phí từ trace

| Khoản | Số tiền (đ) | Nguồn | Nhãn |
| --- | ---: | --- | --- |
| Token | 245.585 | `logix_runs.csv` | đo từ trace |
| Tool | 84.000 | `logix_runs.csv` | đo từ trace |
| Trong đó, phần của lần chạy thứ 2 và 3 | 93.804 | attempt lớn hơn 1 | đo từ trace |
| Xem lại | 1.780.000 | `phut_xem_lai_simulated` | simulated |
| Làm lại | 2.264.000 | `phut_lam_lai_simulated` | simulated |
| Tổng chi phí | 4.373.585 | gồm phần simulated | simulated |
| Số việc thành công | 978 | `ket_qua` | đo từ trace |
| Chi phí mỗi việc thành công | 4.472 | gồm phần simulated | simulated |
| Hoá đơn token và tool chia cho số yêu cầu | 274,7 | `logix_runs.csv` | đo từ trace |

- Chi phí mỗi việc thành công gấp bao nhiêu lần "hoá đơn chia số yêu cầu"? Gấp **16,3 lần** (4.472 đ [simulated] / 274,7 đ). Khi cộng thêm 222 ca không thành công do nhân viên làm thay (12.000 đ/ca), chi phí cả hệ thống là **5.865 đ/yêu cầu = 0,49×** so với 12.000 đ [simulated].
- Khoản nào chiếm tỉ trọng lớn nhất trong tổng chi phí, bao nhiêu phần trăm? **Làm lại** chiếm **51,8%** (2.264.000 đ [simulated]), tiếp theo là xem lại **40,7%** (1.780.000 đ [simulated]); tổng giờ nhân viên chiếm 92,5% chi phí.

**Kiểm tay A2.** Tiền token = (5.771.712 × 26 + 734.774 × 130) / 1.000 = 245.585,132 đ; tiền tool = 5.600 × 15 = 84.000 đ. Phần chạy lại đã nằm trong hai khoản này.
Cộng (890 + 1.132) × 2.000 đ tiền nhân viên rồi chia 978 việc thành công được 4.471,97 đ/việc [simulated]. Nếu tính cả 222 ca phải xử lý tay thì chi phí toàn hệ thống là 5.865 đ/yêu cầu [simulated].


## A3 · Tách theo loại yêu cầu

| Loại | Số yêu cầu | Tỉ lệ thành công | Số lần chạy mỗi yêu cầu | Chi phí mỗi việc thành công | So với 12.000 đ |
| --- | ---: | ---: | ---: | ---: | ---: |
| noi_dia | 824 | 95,0% | 1,11 | 2.696 đ [simulated] | 0,22× [simulated] |
| hang_nang | 158 | 74,1% | 1,47 | 8.221 đ [simulated] | 0,69× [simulated] |
| quoc_te | 150 | 27,3% | 2,32 | 22.515 đ [simulated] | 1,88× [simulated] |
| doi_tac | 68 | 54,4% | 1,88 | 10.215 đ [simulated] | 0,85× [simulated] |

- Loại nào không đáng để trợ lý xử lý? Với loại đó, cho chạy lại tới 3 lần có giúp không? `quoc_te` không đáng xử lý vì tốn **22.515 đ/việc** (1,88× của 12.000 đ [simulated], thành công 27,3%); chạy lại tới 3 lần không giúp vì tỉ lệ `ok` giảm từ 30,0% (lần 1) xuống 11,4% (lần 2) và 2,2% (lần 3). `doi_tac` cũng sát ngưỡng (0,85× [simulated]) nên loại khỏi phạm vi pilot.

## A4 · Chi phí cố định (phạm vi noi_dia + hang_nang)

| Khối lượng | Việc thành công mỗi tháng | Chi phí cố định mỗi việc | Chi phí mỗi việc thành công + cố định | So với 12.000 đ |
| --- | ---: | ---: | ---: | ---: |
| 45.000 yêu cầu/tháng | 33.750 | 1.185 đ | 4.599 đ [simulated] | 0,38× [simulated] |
| Một nửa khối lượng | 16.875 | 2.370 đ | 5.784 đ [simulated] | 0,48× [simulated] |

- Chi phí cố định có đổi kết luận không? Ở khối lượng nào? Ở quy mô 45.000 yêu cầu/tháng (4.599 đ = **0,38×** [simulated]) hay một nửa (5.784 đ = **0,48×** [simulated]) đều không đổi kết luận so với 3.414 đ [simulated] chưa cộng cố định, nhưng đơn giá cố định tăng gấp đôi lên 2.370 đ khi khối lượng giảm một nửa.

## B1 · Đổi từng yếu tố

Các chi phí và tỷ lệ thay đổi trong B1–B4 đều có phần thời gian nhân viên **[simulated]**.

| Kịch bản | Cách tính | Chi phí mỗi việc thành công | Thay đổi (%) |
| --- | --- | ---: | ---: |
| Giá token gấp đôi | 52 đ và 260 đ cho 1.000 token; giá tool giữ nguyên | 4.723 | +5,6% |
| Giá token giảm một nửa | 13 đ và 65 đ | 4.346 | −2,8% |
| Tỉ lệ xem lại gấp đôi | Tiền xem lại × 2 | 6.292 | +40,7% |
| Tỉ lệ xem lại giảm một nửa | Tiền xem lại ÷ 2 | 3.562 | −20,3% |
| Số ca làm lại gấp đôi | Tiền làm lại × 2 | 6.787 | +51,8% |
| Số ca làm lại giảm một nửa | Tiền làm lại ÷ 2 | 3.315 | −25,9% |
| Lương nhân viên tăng 25% | 2.500 đ mỗi phút | 5.506 | +23,1% |
| Chỉ cho chạy tối đa 2 lần | Bỏ lần chạy có attempt > 2; yêu cầu có so_lan_chay > 2 coi là chuyen_nhan_vien | 4.237 | −5,2% |
| Chỉ cho chạy 1 lần | Như trên với giới hạn 1 | 4.111 | −8,1% |

Mốc B1 là 4.471,97 đ/việc [simulated]. Khi giới hạn số lần chạy, chỉ giữ run trong giới hạn; yêu cầu vượt giới hạn chuyển cho nhân viên và có 0 phút xem lại/làm lại. Chi phí cả hệ thống ở B3 cộng thêm 12.000 đ cho mỗi yêu cầu chưa thành công.


## B2 · Đổi một cặp và xếp hạng

- Giá token gấp đôi cùng lúc tỉ lệ xem lại gấp đôi: 6.543 đ/việc, tăng 46,3% [simulated]; cộng thêm 245.585 đ tiền token và 1.780.000 đ tiền xem lại, giữ 978 việc thành công.
- Xếp hạng ba yếu tố ảnh hưởng mạnh nhất: 1. làm lại ×2 (+51,8%) · 2. xem lại ×2 (+40,7%) · 3. lương tăng 25% (+23,1%) [simulated]

## B3 · Giới hạn chạy lại có thật sự rẻ hơn

| Giới hạn | Tổng chi phí trợ lý | Số yêu cầu không thành công | Chi phí cả hệ thống | Chi phí mỗi việc thành công |
| --- | ---: | ---: | ---: | ---: |
| 1 lần | 3.621.781 | 319 | 7.449.781 | 4.111 |
| 2 lần | 4.093.220 | 234 | 6.901.220 | 4.237 |
| 3 lần | 4.373.585 | 222 | 7.037.585 | 4.472 |

- Giới hạn nào rẻ nhất cho công ty? Có trùng với giới hạn cho chi phí mỗi việc thành công thấp nhất không? 2 lần rẻ nhất cho công ty (6.901.220 đ). Giới hạn 1 lần có mức thấp nhất theo việc thành công (4.111 đ), nhưng đẩy thêm 85 việc sang nhân viên [simulated].

## B4 · Nếu phải xem lại tất cả

- Chi phí mỗi việc thành công khi xem lại 100% (`noi_dia` + `hang_nang`), so với 12.000 đ: (224.513 + 948 × 5 × 2.000 + 48 × 9 × 2.000) / 900 = 11.743 đ, bằng 0,98× mức thủ công [simulated], chưa cộng cố định.
- Kết quả này nói gì về thứ pilot cần học được? Khoảng tiết kiệm chỉ còn 257 đ/việc trước cố định [simulated]. Pilot cần đo phút xem lại thực tế và xác định ca nào cần duyệt để giữ chất lượng với ít công duyệt hơn.
