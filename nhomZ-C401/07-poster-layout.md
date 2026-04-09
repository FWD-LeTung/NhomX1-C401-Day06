# Poster layout — 1 trang

## 1) Tên product + problem statement

**VinFast AI Advisor**

Người mua xe VinFast mất nhiều giờ đọc review rời rạc và khó kiểm chứng. AI Advisor tổng hợp thông tin theo nhu cầu, có dẫn nguồn rõ ràng để ra quyết định nhanh hơn.

## 2) Before | After

**Before (hiện tại):**

- Tự tìm review trên nhiều kênh (YouTube, forum, báo)
- Tự lọc thông số/giá, dễ nhầm phiên bản
- Mất 2-5 giờ cho quyết định sơ bộ

**After (với AI):**

- Nhập nhu cầu bằng ngôn ngữ tự nhiên
- AI đề xuất 1-2 mẫu xe + lý do + nguồn
- User có thể hỏi tiếp theo từng khía cạnh (giá, pin, review, showroom)
- Rút xuống 5-15 phút để có shortlist

## 3) Live demo

- Screenshot màn hình chat + tool calls
- Input mẫu: “Tôi có 500 triệu, đi phố 40 km/ngày, nên mua xe nào?”
- Output: đề xuất mẫu xe + trích nguồn + bước tiếp theo
- QR code: trỏ đến demo Chainlit

## 4) Impact

- Thời gian tìm hiểu: 2-5 giờ -> 5-15 phút
- Tỷ lệ câu trả lời có nguồn (khi có số liệu): mục tiêu >= 95%
- P95 latency: mục tiêu < 4 giây
- Tỷ lệ user đánh giá “Hữu ích”: mục tiêu >= 70%

## 5) Failure modes | Learning signal

**Failure modes chính:**

1. Hiểu sai intent với câu hỏi mơ hồ
2. Sai giá do dữ liệu cũ
3. Trích nhầm nguồn/mẫu xe

**Learning signal:**

- Click “Hữu ích” / “Sai-Thiếu nguồn”
- Số lần user hỏi lại và bổ sung thông tin
- Correction log để cải thiện retrieval + prompt
