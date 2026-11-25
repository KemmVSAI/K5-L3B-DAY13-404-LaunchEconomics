# Phiếu chấm hội đồng Gate 2a

Nhóm số n chấm nhóm số n + 1; nhóm cuối chấm nhóm 1. Chấm theo bằng chứng trong hồ sơ, không theo cách trình bày: một đề xuất No-go có lý do bằng số được điểm cao hơn một đề xuất Go bỏ qua con số bất lợi.

- Nhóm chấm (hội đồng): K5-L3B-404
- Nhóm được chấm: 3npc — https://github.com/ngominhcuong/K5-L3B-DAY13-3npc-LaunchEconomics

| Tiêu chí | 0 điểm | 5 điểm | 10 điểm | Điểm | Lý do (có số) |
| --- | --- | --- | --- | ---: | --- |
| Đề xuất khớp bằng chứng | Mâu thuẫn với số của chính nhóm | Khớp nhưng bỏ qua một con số bất lợi | Khớp, nêu cả con số bất lợi và cách xử lý | **10** | Đề xuất Go có điều kiện chỉ pilot `noi_dia + hang_nang`, loại `quoc_te` vì **22.515 đ = 1,88×** và nêu rõ xem lại 100% có thể lên **12.415 đ = 1,03×**. Hồ sơ đưa ra 4 điều kiện, người phụ trách và ngày kiểm tra. |
| Số giả lập và phạm vi | Không nhãn; phạm vi "mọi yêu cầu" | Có nhãn hoặc có thu hẹp phạm vi | Nhãn ở mọi số giả lập; phạm vi thu hẹp có lý do bằng số | **10** | Các số chi phí thời gian đều ghi `simulated`; phạm vi được thu hẹp bằng số: `noi_dia` **0,22×**, `hang_nang` **0,69×**, loại `quoc_te` **1,88×** và `doi_tac` **0,85×**. |
| Pilot ra được quyết định | Không đối chứng hoặc thiếu cỡ mẫu | Đủ cỡ mẫu, luật dừng chung chung | Tách được tác động, đủ mẫu, luật dừng có ngưỡng, thời hạn, người có quyền dừng | **10** | Có đối chứng đồng thời **20+20** nhân viên, `n = 859`/nhóm, `m >= 299` yêu cầu/người, MDE **6 điểm**, 3 luật dừng có ngưỡng/thời hạn/người hành động và rollback **30 phút**. |
| **Tổng** | | | | **30 / 30** | Hồ sơ đáp ứng đủ ba tiêu chí chấm. |

**Quyết định của hội đồng:** **Go có điều kiện**

**Lý do:** Nhóm 3npc trình bày nhất quán với bằng chứng trong `bang_chi_phi.md`, `bang_loi.md`, `pilot_plan.yaml`, `chi_so.md` và `ho_so_launch_v0.md`. Nhóm không che giấu bất lợi kinh tế và không gọi số `simulated` là kết quả pilot thực tế.

**Một câu hỏi cho đội trình:** Vì sao nhóm chấp nhận MDE 6 điểm thay vì 5 điểm, trong khi power ở hiệu ứng 5 điểm chỉ còn khoảng 0,64?

**Câu trả lời của đội trình (theo hồ sơ):** Vì chỉ có 40 nhân viên, chia theo cụm không đủ cỡ mẫu cho MDE 5 điểm. Nhóm công khai đánh đổi này, chọn MDE 6 điểm để đạt power 0,80, giữ đối chứng đồng thời và chỉ mở rộng khi vượt các luật dừng đã viết trước.
