# User stories — 4 paths

## Feature: Tư vấn chọn xe theo nhu cầu

**Trigger:** Người dùng nhập nhu cầu (ngân sách, số chỗ, quãng đường/ngày, ưu tiên tiết kiệm hay tiện nghi) -> AI đề xuất 1-2 mẫu xe phù hợp, kèm lý do và nguồn.

| Path | Câu hỏi thiết kế | Mô tả |
|------|-------------------|-------|
| Happy — AI đúng, tự tin | Người dùng thấy gì? Kết thúc ra sao? | AI gợi ý “VF5 phù hợp đi phố 30-50 km/ngày trong ngân sách X”, nêu 3 lý do và trích nguồn; người dùng bấm “Hữu ích”, sau đó xem bảng so sánh chi tiết. |
| Low-confidence — AI không chắc | Hệ thống báo “không chắc” thế nào? | Khi dữ liệu thiếu/mâu thuẫn, AI hiển thị “Độ chắc chắn thấp”, đưa tối đa 2 phương án và hỏi thêm câu làm rõ nhu cầu. |
| Failure — AI sai | Người dùng phát hiện sai bằng cách nào? | AI đề xuất xe vượt ngân sách hoặc lệch nhu cầu; người dùng bấm “Sai”; hệ thống xin lỗi, hỏi lại điều kiện bắt buộc, sau đó truy xuất lại và trả lời mới. |
| Correction — người dùng sửa | Người dùng sửa bằng cách nào? Dữ liệu đi đâu? | Người dùng chỉnh ngân sách/tiêu chí và bấm “Lưu phản hồi”; dữ liệu vào correction log để cải thiện bước hiểu ý định và xếp hạng kết quả. |

---

## Feature: Hỏi đáp thông số và review có dẫn nguồn

**Trigger:** Người dùng hỏi về thông số, giá, hoặc trải nghiệm thực tế của một mẫu xe cụ thể -> AI trả lời ngắn gọn, có dẫn nguồn.

| Path | Câu hỏi thiết kế | Mô tả |
|------|-------------------|-------|
| Happy — AI đúng, tự tin | Người dùng thấy gì? Kết thúc ra sao? | AI trả lời đúng trọng tâm, kèm 2-3 nguồn liên quan; người dùng tiếp tục hỏi sâu hoặc chọn nhận tư vấn từ showroom. |
| Low-confidence — AI không chắc | Hệ thống báo “không chắc” thế nào? | Nếu dữ liệu cũ hoặc thiếu nguồn tin cậy, AI không khẳng định tuyệt đối; hiển thị cảnh báo “Cần xác minh tại showroom”. |
| Failure — AI sai | Người dùng phát hiện sai bằng cách nào? | AI nêu sai giá theo phiên bản; người dùng bấm “Thiếu chính xác” và chọn “Sai giá”; hệ thống buộc truy xuất lại từ nguồn giá mới nhất trước khi trả lời lại. |
| Correction — người dùng sửa | Người dùng sửa bằng cách nào? Dữ liệu đi đâu? | Người dùng gửi nguồn/giá bổ sung; dữ liệu vào hàng chờ kiểm duyệt trước khi cập nhật kho tri thức để tránh nhiễu dữ liệu. |
