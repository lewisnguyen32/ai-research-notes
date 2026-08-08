# AI Research & R&D Automation

Tổng hợp các nghiên cứu về tự động hóa quy trình R&D khoa học (Scientific AI R&D), phương pháp kiểm thử năng lực tự chủ nghiên cứu của AI.

---

## Key Concepts & Synthesis

- **Verifiable Benchmarks vs Shadow Evaluations**:
  - *Verifiable Benchmarks* (MLE-Bench, CORE-Bench): Đánh giá tác vụ hẹp đo bằng một chỉ số cố định.
  - *Shadow Evaluations*: Giao câu hỏi từ bài báo top-tier chưa công bố và nhờ chính tác giả gốc chấm điểm.
- **Tầng Kỹ thuật (Execution Layer) vs Tầng Định hướng (Direction Layer)**:
  - Agent hiện tại đã tự chủ 100% ở khâu kỹ thuật (coding, GPU execution, LaTeX compilation).
  - Agent hoàn toàn thất bại ở khâu định hướng giả thuyết, chọn bài toán và phản biện chuyên sâu.
- **Human-in-the-Loop R&D Model**:
  - Con người giữ vai trò *Navigator / Verifier* (định hướng giả thuyết, chọn phương pháp).
  - AI Agent làm *Executor* (viết mã, chạy thực nghiệm, tổng hợp tài liệu).

---

## Relevant Papers in Library

| Paper | Key Contribution / Takeaway | Status |
| --- | --- | --- |
| [Can AI agents conduct open-ended AI research?](../papers/can-ai-agents-conduct-open-ended-ai-research/analysis.md) | Giới thiệu Shadow Evaluations và chỉ ra sự khác biệt giữa R&D Engineering và Open-ended Science. | ⭐ Must Read |

---

## Shared Resources
- 📖 [Thuật ngữ Chuyên ngành AI Research & Evaluation](../resources/glossary-ai-research-terms.md)
