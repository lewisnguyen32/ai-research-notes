[← Library README](../README.md) | [Glossary](../resources/glossary-ai-research-terms.md)

# AI Research & R&D Automation

> 📌 **Scope**: Synthesis across papers currently present in this user-curated repository.

Tổng hợp các nghiên cứu về tự động hóa quy trình R&D khoa học (Scientific AI R&D) và phương pháp kiểm thử năng lực tự chủ nghiên cứu của AI dựa trên các tài liệu có sẵn trong thư viện.

---

## 🗺️ Specialized Reading Path

👉 **[Autonomous AI Research Reading Path Map](autonomous-ai-research.md)** — Bản đồ đọc liên hoàn (01 ➔ 02 ➔ 03) giải đáp toàn diện câu hỏi *"AI có thể tự thực hiện nghiên cứu khoa học đến mức nào?"*.

---

## Key Concepts & Synthesis

- **Verifiable Benchmarks vs Shadow Evaluations**:
  - *Verifiable Benchmarks* (MLE-Bench, CORE-Bench): Đánh giá tác vụ hẹp đo bằng một chỉ số cố định.
  - *Shadow Evaluations*: Giao câu hỏi từ bài báo top-tier chưa công bố và nhờ chính tác giả gốc chấm điểm.
- **Tầng Kỹ thuật (Execution Layer) vs Tầng Định hướng (Direction Layer)**:
  - Agent hiện tại đã tự chủ 90-100% ở khâu kỹ thuật (coding, GPU execution, LaTeX compilation, điều khiển robot phòng lab).
  - Agent gặp khó khăn lớn ở khâu định hướng giả thuyết mở, thẩm định giá trị nghiên cứu thực sự và tự kiểm định lỗi.
- **Human-in-the-Loop R&D Model**:
  - Con người giữ vai trò *Navigator / Verifier* (định hướng giả thuyết, duyệt an toàn, chọn bài toán).
  - AI Agent làm *Executor* (viết mã, chạy thực nghiệm, tổng hợp tài liệu, vận hành quy trình).

---

## Relevant Papers in Library

| Paper | Key Contribution / Takeaway | Status |
| --- | --- | --- |
| [Towards end-to-end automation of AI research](../papers/towards-end-to-end-automation-of-ai-research/analysis.md) | Kiến trúc hệ thống *The AI Scientist* — tự động hóa khép kín 100% quy trình từ ý tưởng đến bài báo và tự phản biện với giá $15/bài. | ⭐ Must Read |
| [Can AI agents conduct open-ended AI research?](../papers/can-ai-agents-conduct-open-ended-ai-research/analysis.md) | Giới thiệu Shadow Evaluations và chỉ ra sự khác biệt giữa R&D Engineering và Open-ended Science. | ⭐ Must Read |
| [From AI for Science to Agentic Science](../papers/from-ai-for-science-to-agentic-science/analysis.md) | Bài khảo sát toàn cảnh định hình thang 4 cấp độ tự chủ và quy trình 4 giai đoạn trên các ngành Sinh, Hóa, Vật liệu, Vật lý. | ⭐ Must Read |

---

## Shared Resources
- 📖 [Thuật ngữ Chuyên ngành AI Research & Evaluation](../resources/glossary-ai-research-terms.md)
