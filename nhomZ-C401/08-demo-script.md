# Demo script — 5 phút trình bày + 5 phút Q&A

## Structure (5 phút trình bày)

| Phần | Thời gian | Nội dung | Ai nói |
|------|-----------|----------|--------|
| Problem + Before | 45s | Người mua xe VinFast đang gặp gì? Tại sao flow cũ tốn thời gian và khó tin cậy? | Thành viên 1 |
| Solution + After | 45s | VinFast AI Advisor giải quyết thế nào? Automation hay augmentation? | Thành viên 2 |
| Live demo | 120s | Demo 1 flow chính: ngân sách + nhu cầu -> AI đề xuất xe + nguồn -> user feedback | Thành viên 3 |
| Impact + Lessons | 45s | Metric mục tiêu, failure mode nguy hiểm nhất, bài học khi xây dựng | Thành viên 4 |

## Script gợi ý từng phần

### 1) Problem + Before (45s)

"Người dùng tìm mua xe VinFast thường phải đọc nhiều nguồn rời rạc, mất 2-5 giờ để có quyết định sơ bộ. Vấn đề là thông tin dễ mâu thuẫn, khó đối chiếu theo nhu cầu cá nhân."

### 2) Solution + After (45s)

"Chúng tôi xây VinFast AI Advisor theo hướng augmentation: AI gợi ý và tổng hợp, còn quyết định cuối cùng vẫn do user và showroom xác nhận. Hệ thống có các tool: RAG thông số, lọc theo ngân sách, tìm showroom, tìm review YouTube/Reddit."

### 3) Live demo (120s)

1. Nhập: “Tôi có 500 triệu, đi phố 40 km/ngày, ưu tiên tiết kiệm.”
2. Show AI gọi tool phù hợp và trả lời đề xuất 1-2 mẫu xe.
3. Nhắc rõ phần dẫn nguồn và cảnh báo nếu dữ liệu không chắc.
4. Bấm feedback “Hữu ích” hoặc “Sai/Thiếu nguồn” để minh họa learning loop.
5. (Nếu còn thời gian) Demo edge case: câu hỏi mơ hồ -> AI hỏi thêm để làm rõ.

### 4) Impact + Lessons (45s)

"Mục tiêu hệ thống: factual precision >= 90%, tỷ lệ câu trả lời có nguồn >= 95%, P95 latency < 4s. Failure mode nguy hiểm nhất là AI trả lời nghe hợp lý nhưng sai thực tế. Vì vậy chúng tôi ưu tiên precision-first và bắt buộc dẫn nguồn cho thông tin quan trọng."

## Q&A (5 phút)

- Câu hỏi thường gặp:
  - Tại sao không dùng ChatGPT trực tiếp?
  - Nếu AI sai thì sao?
  - Hệ thống học từ feedback như thế nào?
  - Team member đóng góp gì?

## Checklist trước demo

- [ ] Dry run ít nhất 1 lần, bấm giờ đủ 5 phút
- [ ] Mở sẵn app Chainlit + internet ổn định
- [ ] Có backup screenshot/video nếu demo crash
- [ ] Mỗi thành viên nói ít nhất 1 phần
