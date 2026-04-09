# AI Product Canvas — VinFast AI Advisor

## Canvas

|   | Value | Trust | Feasibility |
|---|-------|-------|-------------|
| **Câu hỏi guide** | User nào? Pain gì? AI giải quyết gì mà cách hiện tại không giải được? | Khi AI sai thì user bị ảnh hưởng thế nào? User biết AI sai bằng cách nào? User sửa bằng cách nào? | Cost bao nhiêu/request? Latency bao lâu? Risk chính là gì? |
| **Trả lời** | **User:** người đang cân nhắc mua xe VinFast lần đầu hoặc muốn đổi xe trong 6-12 tháng tới. <br><br> **Pain:** phải đọc nhiều review rời rạc (YouTube, forum, báo), thông tin giá/thông số dễ mâu thuẫn, mất 2-5 giờ mới có quyết định sơ bộ. <br><br> **AI giải quyết:** chatbot tổng hợp nhanh theo nhu cầu cá nhân (ngân sách, quãng đường, số chỗ), gợi ý 1-2 mẫu xe phù hợp và nêu lý do có dẫn nguồn. | **Ảnh hưởng khi AI sai:** user có thể hiểu sai giá, sai thông số, hoặc chọn nhầm mẫu xe không phù hợp nhu cầu. <br><br> **User biết AI sai:** phát hiện câu trả lời mâu thuẫn với nguồn đính kèm hoặc với thông tin showroom/chính hãng. <br><br> **User sửa:** bấm “Sai/Thiếu nguồn”, chọn loại lỗi, nhập thông tin đúng hoặc hỏi lại với điều kiện rõ hơn; hệ thống ghi correction log. | **Cost:** khoảng **$0.002-$0.02/request** tùy số lần gọi tool + độ dài phản hồi. <br><br> **Latency:** mục tiêu **P95 < 4 giây**. <br><br> **Risk:** hallucination ở nhóm thông tin nhạy cảm (giá/an toàn), dữ liệu cũ, truy xuất nhầm nguồn cùng tên xe. |

---

## Automation hay augmentation?

☐ Automation — AI làm thay, user không can thiệp
☑ Augmentation — AI gợi ý, user quyết định cuối cùng

**Justify:**  
AI chỉ đóng vai trò tư vấn ban đầu và tổng hợp thông tin. Quyết định mua xe, lái thử, ký hợp đồng và xác nhận giá cuối cùng vẫn do khách hàng + tư vấn viên thực hiện, nên cost of reject thấp và dễ kiểm soát rủi ro.

---

## Learning signal

| # | Câu hỏi | Trả lời |
|---|---------|---------|
| 1 | User correction đi vào đâu? | Vào correction log gồm: câu hỏi, câu trả lời, tool đã gọi, nguồn trích dẫn, loại lỗi (sai giá/sai thông số/sai nguồn), thời điểm, và nội dung user chỉnh sửa. |
| 2 | Product thu signal gì để biết tốt lên hay tệ đi? | - Tỷ lệ “Hữu ích” <br> - Tỷ lệ “Sai/Thiếu nguồn” <br> - Tỷ lệ user hỏi sâu (>= 3 câu/phiên) <br> - Tỷ lệ để lại thông tin liên hệ hợp lệ |
| 3 | Data thuộc loại nào? | ☑ Domain-specific · ☑ Human-judgment · ☑ Real-time (một phần) · ☑ User-specific (mức nhẹ) |

**Giải thích:**

- **Domain-specific:** thông số kỹ thuật xe, phiên bản, phân khúc, review tiếng Việt theo từng mẫu xe
- **Human-judgment:** phản hồi “Hữu ích”/“Sai” và dữ liệu user sửa câu trả lời
- **Real-time (một phần):** giá/khuyến mãi và tình trạng thị trường thay đổi theo thời điểm
- **User-specific (mức nhẹ):** ngữ cảnh phiên chat hiện tại (nhu cầu, ngân sách, ưu tiên)

---

## Có marginal value không?

Có **marginal value rõ ràng**.

Thông tin công khai (giá niêm yết, thông số cơ bản) thì đối thủ cũng có thể thu thập.

Nhưng lợi thế tích lũy nằm ở:

- correction log nội bộ theo lỗi thực tế của người dùng Việt
- dữ liệu tương tác theo ngữ cảnh nhu cầu mua xe (đi phố/đường dài/gia đình)
- hiệu quả gợi ý theo hành vi user ở giai đoạn tiền mua

Những tín hiệu này giúp hệ thống cải thiện chất lượng tư vấn theo thời gian, khó sao chép nhanh.
