# Eval metrics + threshold

## Precision hay recall?

☑ Precision — khi AI nói "có" thì thực sự đúng (ít false positive)

☐ Recall — tìm được hết những cái cần tìm (ít false negative)

**Tại sao?** Bài toán tư vấn mua xe cần độ đúng cao; sai thông tin giá/an toàn làm mất niềm tin ngay từ lần đầu.

**Nếu sai ngược lại thì sao?** Nếu thiên về recall quá mức, chatbot có thể trả lời nhiều nhưng kém chắc chắn, làm tăng lỗi và giảm tỷ lệ để lại thông tin liên hệ.

## Metrics table

| Metric | Threshold | Red flag (dừng khi) |
|--------|-----------|---------------------|
| Độ chính xác thông tin có dẫn nguồn (factual precision) | >= 90% | < 80% trong 1 tuần |
| Tỷ lệ bịa thông tin ở nhóm giá/an toàn | = 0% | > 1 lỗi xác nhận sai/ngày |
| Tỷ lệ câu trả lời có dẫn nguồn khi có số liệu | >= 95% | < 85% trong 3 ngày liên tiếp |
| Tỷ lệ người dùng bấm “Hữu ích” | >= 70% | < 50% trong 2 tuần |
| P95 latency (95% phản hồi dưới ngưỡng) | < 4 giây | > 6 giây trong giờ cao điểm, 3 ngày liên tiếp |
| Tỷ lệ để lại thông tin liên hệ hợp lệ | >= 5% | < 2% trong 4 tuần |
