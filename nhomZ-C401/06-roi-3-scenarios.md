# ROI 3 kịch bản

**Định nghĩa chung:** “Thông tin liên hệ hợp lệ” là bản ghi có ít nhất số điện thoại hoặc email + nhu cầu mua xe cơ bản, đủ để đội tư vấn liên hệ lại.

|   | Conservative | Realistic | Optimistic |
|---|-------------|-----------|------------|
| **Assumption** | 120 người dùng/ngày, 55% thấy hữu ích, 3% để lại thông tin liên hệ hợp lệ | 400 người dùng/ngày, 70% thấy hữu ích, 6% để lại thông tin liên hệ hợp lệ | 1200 người dùng/ngày, 80% thấy hữu ích, 9% để lại thông tin liên hệ hợp lệ |
| **Cost** | $45/ngày (LLM + embedding + hạ tầng) | $140/ngày | $360/ngày |
| **Benefit** | Tiết kiệm 3 giờ tư vấn viên/ngày + 3.6 khách để lại thông tin liên hệ hợp lệ/ngày | Tiết kiệm 10 giờ/ngày + 24 khách để lại thông tin liên hệ hợp lệ/ngày | Tiết kiệm 28 giờ/ngày + 108 khách để lại thông tin liên hệ hợp lệ/ngày |
| **Net** | Dương nhẹ nếu mỗi khách để lại thông tin hợp lệ tạo giá trị >= $15 | Dương rõ rệt, có thể hoàn vốn vận hành theo ngày | Dương mạnh, phù hợp mở rộng đa kênh (web, app, kiosk showroom) |

**Kill criteria:** Dừng hoặc đổi hướng nếu trong 8 tuần liên tiếp có một trong các điều kiện: (1) tỷ lệ “Hữu ích” < 50%, (2) lỗi sai giá/an toàn chưa đưa về 0, hoặc (3) chi phí vận hành lớn hơn lợi ích định lượng trong 2 tháng liên tục.
