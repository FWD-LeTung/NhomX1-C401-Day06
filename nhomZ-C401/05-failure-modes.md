# Top 3 failure modes

| # | Trigger | Hậu quả | Mitigation |
|---|---------|---------|------------|
| 1 | Câu hỏi mơ hồ, có từ lóng/châm biếm, hệ thống hiểu sai ý định | Tư vấn sai nhu cầu nhưng trả lời rất tự tin | Bắt buộc hỏi làm rõ khi điểm tự tin hiểu ý định thấp |
| 2 | Dữ liệu giá/khuyến mãi cũ hoặc lẫn phiên bản xe | Người dùng nhận thông tin giá sai, giảm niềm tin vào hệ thống | Đặt thời hạn hiệu lực dữ liệu giá; nếu quá hạn thì hiển thị “Cần xác minh tại showroom” |
| 3 | Truy xuất nhầm nguồn (khác hãng hoặc nhầm mẫu xe tên gần giống) | AI trích sai nguồn và đề xuất lệch | Lọc cứng theo hãng/mẫu xe trước khi sinh câu trả lời; kiểm tra chéo nội dung trả lời với metadata nguồn |

**Failure nguy hiểm nhất:** AI trả lời nghe hợp lý nhưng sai thực tế, và người dùng không phát hiện ngay.
