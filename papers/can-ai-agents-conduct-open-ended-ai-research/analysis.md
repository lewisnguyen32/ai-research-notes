[← Library README](../../README.md) | [Reading Path](../../topics/autonomous-ai-research.md) | [Glossary](../../resources/glossary-ai-research-terms.md)

# Can AI agents conduct open-ended AI research? Early evidence from two case studies

**Authors:** Peter Kirgis*, Sayash Kapoor*, Andrew Schwartz*, Stephan Rabanser* (*Equal contribution, †CRUX Core Team), Arvind Narayanan† et al. (Princeton University, Cornflower Labs, UK AISI, Univ. of Toronto, Stanford, UC Berkeley, Georgetown CSET, Johns Hopkins)  
**Year:** 2026 (arXiv:2607.27191v1, 29/07/2026)  
**Source:** [arXiv:2607.27191](https://arxiv.org/abs/2607.27191)  
**Paper:** [`paper.pdf`](paper.pdf) | 🇻🇳 [Bản Dịch Tiếng Việt](translation-vi.md)

---

## TL;DR

Nghiên cứu giới thiệu phương pháp **Shadow Evaluations** nhằm đánh giá khả năng tự chủ làm nghiên cứu AI mở (open-ended AI research) của Frontier AI Agents.

Thử nghiệm giao câu hỏi nghiên cứu từ 2 bài báo NeurIPS 2026 chưa công bố cho Agent thực hiện trong 6 ngày wall-clock time với $3,000 ngân sách API và GPU compute đầy đủ. Sau đó, chính các tác giả gốc của bài báo thẩm định sản phẩm theo tiêu chí phản biện kín của NeurIPS.

- **Main Experiment**: Base model `Claude Opus 4.8` (Anthropic, extra-high reasoning) chạy trên agent scaffold `OpenClaw`.
- **Robustness Check**: Base model `GPT-5.6 Sol` (OpenAI, reasoning level "ultra") chạy trên native scaffold `Codex`.

**Kết quả**: Cả 2 bài báo do Agent tạo ra đều **bị tác giả gốc từ chối hoàn toàn (Unambiguously Rejected)** với điểm số **2/6 (Reject)** cho bài *Personas* và **1/6 (Strong Reject)** cho bài *TabPFN*. Agent hoàn thành 100% công việc **Kỹ thuật R&D** (code, GPU, LaTeX, thực nghiệm), nhưng **thất bại nghiêm trọng ở tư duy nghiên cứu khoa học mở**.

---

## Why This Paper Matters

Bài báo này giội một gáo nước lạnh vào các tuyên bố lạc quan quá mức về việc AI Agent sắp tự nghiên cứu và tự cải thiện bản thân (Recursive Self-Improvement).

Nghiên cứu cho thấy sự phát triển của mô hình suy luận (reasoning LLMs) chỉ giúp AI làm tốt công việc "kỹ thuật viên R&D", chứ chưa giúp AI có được "tư duy thẩm định và sáng tạo của một nhà khoa học". Nó thiết lập một cột mốc quan trọng trong việc phân định ranh giới thực sự giữa kỹ năng lập trình/chạy pipeline và năng lực phát triển khoa học.

---

## The Problem

Các dự báo về sự phát triển vượt bậc của AI phụ thuộc vào việc AI Agent có thể tự động hóa công tác nghiên cứu và phát triển AI (AI R&D). Tuy nhiên, các phương pháp đánh giá agent hiện tại có nhược điểm lớn:

1. **Verifiable Benchmarks** (như MLE-Bench, RE-Bench, CORE-Bench): Chỉ kiểm tra tác vụ hẹp có thể đo bằng một chỉ số cố định, hoàn toàn bỏ qua bản chất khám phá của nghiên cứu mở.
2. **Blind Peer Review** (như AI Scientist): Gửi bài báo AI tạo ra đến các quy trình phản biện kín hội nghị vốn đang quá tải, mang tính ngẫu nhiên cao và phản biện nông.
3. **Data Contamination**: Agent có thể vô tình ghi nhớ dữ liệu/bài báo đã có trên internet.

Cần một phương pháp đánh giá thực chất năng lực nghiên cứu mở mà không bị rò rỉ dữ liệu và có sự phản biện khắt khe từ chuyên gia hàng đầu.

---

## Core Idea

Nhóm tác giả đề xuất **Shadow Evaluations (Đánh giá bóng)**:
- **Câu hỏi không rò rỉ (Uncontaminated Questions)**: Lấy từ các bài báo NeurIPS 2026 chưa công bố.
- **Thử nghiệm quy mô thực tế**: Cấp cho Agent 6 ngày thời gian thực, $3,000 ngân sách Anthropic API, GPU compute đầy đủ, VM Linux trên AWS và Open Web.
- **Chấm điểm trực tiếp từ Tác giả gốc**: Bài báo do Agent hoàn thành được gửi cho chính nhóm tác giả gốc của bài báo NeurIPS đó phản biện theo đúng tiêu chí NeurIPS (1-6 scale).

---

## How It Works

### Phân định Hệ thống & Mô hình (System Architecture)
- **Base Models**:
  - `Claude Opus 4.8` (Anthropic): Mô hình chính (extra-high reasoning).
  - `GPT-5.6 Sol` (OpenAI): Mô hình thử nghiệm độ bền (reasoning level "ultra").
  - `GPT-5.3 Codex` & `Claude Fable 5`: Mô hình thử nghiệm pilot / sửa lỗi scaffold.
  - `Qwen 2.5` (3B-14B) & `Llama 3`: Các mô hình do Agent gọi & huấn luyện trong thực nghiệm.
- **Agent Scaffolds**:
  - `OpenClaw`: Khung điều phối agent mã nguồn mở quản lý vòng lặp chạy, subagents, tools và GPU jobs.
  - `Codex`: Khung điều phối agent chính chủ của OpenAI dùng trong thử nghiệm robustness.
- **External AI Review Tools**: `Stanford Agentic Reviewer`, `CMU Paper Reviewer`, `refine.ink` ($60/lần).

### Hai Bài toán Thực nghiệm (Case Studies)
1. **Personas Paper** (hợp tác với UK AI Security Institute - UK AISI): Khảo sát điều hướng tính cách LLM trong không gian trọng số (weight-space intervention).
2. **TabPFN Paper** (hợp tác với University of Toronto): Xây dựng bộ phát hiện dịch chuyển phân phối (distribution shift detector) cho mô hình Prior-Fitted Networks (PFN).

---

## Key Results

### 1. Điểm số Phản biện từ Con người (NeurIPS 1-6 Scale)

| Case Study | Quality | Clarity | Significance | Originality | Overall Score | Confidence |
| --- | --- | --- | --- | --- | --- | --- |
| **Personas Paper** | 2/4 | 1/4 | 2/4 | 3/4 | **2/6 (Reject)** | 4/5 |
| **TabPFN Paper** | 1/4 | 2/4 | 2/4 | 2/4 | **1/6 (Strong Reject)** | 5/5 |

### 2. Định lượng Kỹ thuật vs Nghiên cứu

- **Kỹ thuật R&D (Engineering) — 100% Tự chủ**: Agent tự động tổng quan tài liệu, thiết lập môi trường Linux/GPU, tự sửa lỗi crash-loop, chạy thực nghiệm, gọi tool phản biện AI và biên dịch file LaTeX hoàn chỉnh.
- **Nghiên cứu Mở (Open-ended Research) — 0% Tiến triển**: Cả 2 bài báo đều bị bác bỏ hoàn toàn do thiếu đóng góp khoa học, chọn dữ liệu bừa bãi và lập luận kém.
- **Tái hiện trên Robustness Check**: Khi thay bằng `GPT-5.6 Sol` + `Codex` scaffold, Agent tiêu tốn toàn bộ $3,000 API budget trong >2 ngày nhưng vẫn tái hiện lại 100% các thất bại tương tự.

---

## What The Paper Actually Demonstrates

### Điều thực nghiệm chứng minh được:
- Agent hiện tại đã đạt mức tự chủ tuyệt đối ở **tầng thực thi kỹ thuật (Execution layer)**: coding, debugging, cluster management, LaTeX formatting.
- Tăng thời gian (6 ngày) và ngân sách ($3,000 API budget) **không tự động nâng cao chất lượng nghiên cứu** nếu thiếu năng lực định hướng và tự đánh giá.
- Tồn tại **5 Chế độ Thất bại Cốt lõi (Five Failure Modes)** ở mọi mô hình & scaffold:
  1. **Lack of Judgment**: Thiếu năng lực đánh giá tiêu chuẩn nghiên cứu (dùng synthetic data nhỏ; AI self-review quá lạc quan).
  2. **Lack of Creative Problem Solving**: Thiếu giải quyết vấn đề sáng tạo (khi giả thuyết bị bác bỏ, Agent chỉ hạ thấp tham vọng, viết bài báo kết quả tiêu cực).
  3. **Lack of Effective Backtracking**: Không bao giờ backtrack ở cấp độ dự án (ở bài TabPFN, sau 14h thất bại, Agent dành 110h còn lại chỉ để viết bài "kết quả tiêu cực").
  4. **Lack of Resource Awareness**: Thiếu nhận thức tài nguyên (dừng dự án sớm khi thừa >50% ngân sách và thời gian).
  5. **Instruction Drift**: Trôi dạt hướng dẫn do suy giảm ngữ cảnh (context rot), vi phạm quy định cứng (vượt 9 trang NeurIPS).

### Điều paper chỉ suggest hoặc chưa chứng minh:
- Chưa chứng minh được liệu các scaffold dạng Multi-Agent Debate hay Verifier Models chuyên biệt có thể khắc phục được 5 failure modes này hay không.
- Mẫu đánh giá mới dừng ở 2 case studies (tuy nhiên chất lượng đánh giá rất sâu từ tác giả gốc).

---

## Limitations

- **Số lượng mẫu nhỏ**: 2 case studies do chi phí tính toán và công sức đánh giá của tác giả gốc rất lớn.
- **Đánh giá không mù (Non-blind)**: Tác giả gốc biết bài báo do Agent tạo ra, dù họ sử dụng đúng tiêu chuẩn NeurIPS để chấm.
- **Scaffold overhang**: Rào cản có một phần đến từ khung điều phối agent (context compression / tool use limits), dù thử nghiệm trên Codex vẫn bị.

---

## My Interpretation

- **Biết làm nhưng không biết nghĩ**: AI Agent giống như một thực tập sinh kỹ thuật cực kỳ siêng năng (viết code nhanh, thức đêm sửa bug GPU), nhưng thiếu tư duy thẩm định giá trị nghiên cứu.
- **Khoảng cách Generator-Verifier (Generator-Verifier Gap)**: Sinh ra một bài báo nhìn giống thật thì dễ, nhưng tự nhận biết bài báo đó có giá trị khoa học thực sự hay không lại rất khó. AI bị mắc kẹt vào bế tắc nhận thức (epistemic lock-in) và tự đánh giá quá cao sản phẩm của mình.

---

## What This Means For AI

- **Human-in-the-loop R&D**: Trong 1–3 năm tới, mô hình tối ưu là **Con người làm Navigator/Verifier** (định hướng giả thuyết, chọn bài toán, quyết định backtrack) + **AI làm Executor** (chạy code, thực nghiệm, tổng hợp tài liệu).
- **Phát triển Verifier Models**: Cần huấn luyện các mô hình kiểm định (Verifier Models) độc lập có khả năng phản biện khắt khe ngang tầm chuyên gia để đồng hành cùng Generator Agent.
- **Thiết kế Scaffold tương lai**: Scaffold phải được bổ sung cơ chế **Backtracking cấp độ dự án** và hệ thống quản lý bộ nhớ chống trôi dạt ngữ cảnh (Context Rot mitigation).

---

## Questions / Things To Investigate

- Liệu cơ chế Multi-Agent Debate giữa 1 Generator Agent và 1 Reviewer Agent có giúp làm giảm hiện tượng lạm phát điểm tự chấm (AI self-review inflation) hay không?
- Các kỹ thuật Long-context Memory mới có giúp giải quyết triệt để Instruction Drift trên các dự án kéo dài 7–14 ngày không?

---

## Related Papers

- 🇻🇳 [Bản Dịch Tiếng Việt Đầy Đủ](translation-vi.md)
- 📖 [Thuật Ngữ Chuyên Ngành AI Research](../../resources/glossary-ai-research-terms.md)
- 🤖 Topic: [AI Research & Automation](../../topics/ai-research-automation.md) | [AI Agents](../../topics/ai-agents.md)
