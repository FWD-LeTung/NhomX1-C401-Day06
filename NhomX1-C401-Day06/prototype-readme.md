# Prototype — VinFast AI Advisor

## Mô tả
Chatbot tư vấn mua xe VinFast: tra cứu thông số, gợi ý chọn xe theo **ngân sách**, và tổng hợp trải nghiệm/review từ nguồn bên ngoài. Hệ thống kết hợp **RAG** (từ dữ liệu xe đã lập chỉ mục) với **web search** (YouTube/Reddit/Showroom) để trả lời kèm link nguồn. Demo chạy trên **Chainlit UI**, có hiển thị tool steps và nút feedback.

## Level: Working
- End-to-end chạy được: UI → Agent → Tools (RAG/Search) → trả lời
- Có starter prompts, tool steps, feedback (Hữu ích / Sai/Thiếu nguồn)

## Links
- Demo web: **[DÁN LINK DEMO WEB Ở ĐÂY]**
- Video/Drive: **[DÁN LINK DRIVE Ở ĐÂY]**
- GitHub repo: https://github.com/FWD-LeTung/NhomX1-C401-Day06.git

## Tools
- UI: **Chainlit** (`app.py`, `.chainlit/config.toml`)
- Agent orchestration: **LangGraph + LangChain** (`agent/agent.py`)
- AI (LLM): **Qwen 3.5-Flash** (DashScope OpenAI-compatible API)
- Embeddings: **OpenAI Embeddings API**
- Vector DB (RAG): **ChromaDB** (`chroma_db/`, `tools/RAG_tools.py`, `scripts/init_db.py`)
- Search: **Brave Search API** (`tools/search_tools.py`)
- Data crawl/scrape: **Firecrawl API** (pipeline chuẩn bị dữ liệu trong `data/`)

## Phân công
| Thành viên | Phần | Output |
|-----------|------|--------|
| Lê Văn Tùng (2A202600111) | Search Tools (YouTube, Reddit, Showroom) | `tools/search_tools.py` + tool wrappers trong `agent/agent.py` |
| Nguyễn Đức Sĩ (2A202600152) | Xây dựng Database & RAG | `tools/RAG_tools.py`, dữ liệu `data/raw/vinfast_clean/`, vector store `chroma_db/` |
| Lê Thành Thưởng (2A202600106) | Xây dựng Database & RAG | `scripts/init_db.py`, chuẩn hoá dữ liệu RAG, tích hợp ChromaDB |
| Đinh Thái Tuấn (2A202600360) | UI (Chainlit) & Eval Metrics | `app.py`, `.chainlit/config.toml`, `NhomX1-C401-Day06/spec-final.md` (Eval metrics) |
