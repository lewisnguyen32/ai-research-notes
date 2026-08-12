[← Library README](../../README.md) | [Reading Path](../../topics/autonomous-ai-research.md) | [Glossary](../../resources/glossary-ai-research-terms.md)

# From AI for Science to Agentic Science: A Survey on Autonomous Scientific Discovery

**Authors:** Jiaqi Wei*, Yuejin Yang*, Xiang Zhang*, Yuhan Chen*, Xiang Zhuang*, Zhangyang Gao*, Dongzhan Zhou*, Siqi Sun†, Lei Bai†, Bowen Zhou† et al. (Shanghai AI Laboratory, Zhejiang Univ, Fudan Univ, Tsinghua Univ, CUHK, Jiao Tong Univ)  
**Year:** 2025/2026 (arXiv:2508.14111v2, 20 Oct 2025)  
**Source:** [arXiv:2508.14111](https://arxiv.org/abs/2508.14111) | [GitHub Repository](https://github.com/AgenticScience/Awesome-Agent-Scientists)  
**Paper:** [`paper.pdf`](paper.pdf) | 🇻🇳 [Bản Dịch Tiếng Việt](translation-vi.md)

---

## TL;DR

Bài báo tổng quan (survey) toàn diện đầu tiên định hình sự chuyển dịch lịch sử từ **AI for Science** (AI làm công cụ tính toán hẹp) sang **Agentic Science** (AI làm đối tác nghiên cứu tự chủ). Paper xây dựng khung lý thuyết thống nhất gồm **4 cấp độ tự chủ** (Level 1 ➔ Level 4), quy trình khám phá **4 giai đoạn** (Workflow), và khảo sát chuyên sâu ứng dụng agent trên 4 ngành khoa học tự nhiên lớn: **Khoa học sự sống (Life Sciences), Hóa học (Chemistry), Khoa học vật liệu (Materials Science), và Vật lý / Thiên văn học (Physics)**.

---

## Why This Paper Matters

Nếu như hai bài báo trước (*Can AI agents conduct open-ended AI research?* và *The AI Scientist*) chỉ tập trung vào tự động hóa nghiên cứu trong lĩnh vực Khoa học máy tính (AI tự nghiên cứu AI qua code), thì bài khảo sát này mở rộng góc nhìn ra toàn bộ **Khoa học tự nhiên thực nghiệm**. 

Nó cung cấp một khung phân loại hệ thống (taxonomy) giúp giới nghiên cứu thoát khỏi các tuyên bố chung chung, đồng thời tổng hợp hàng trăm hệ thống agentic thực tế kết hợp LLM với robot phòng thí nghiệm (Self-driving labs), thiết bị đo đạc và giả lập vật lý.

---

## The Problem

Khám phá khoa học đang đối mặt với "cuộc khủng hoảng độ phức tạp" (complexity bottleneck): lượng dữ liệu thực nghiệm bùng nổ, không gian hợp chất Hóa/Sinh/Vật liệu vô tận (10^60 phân tử nhỏ), trong khi năng lực xử lý của con người bị giới hạn.

Các mô hình AI truyền thống (như AlphaFold, Graph Neural Networks) chỉ đóng vai trò là "Oracle" — trả lời một phép tính hẹp. Chúng thiếu năng lực **tự chủ hành động (agency)**: không thể tự đưa ra giả thuyết mới, không thể tự lập kế hoạch thí nghiệm nhiều bước, và không thể tự điều chỉnh khi thí nghiệm thất bại.

---

## Core Idea & Framework

Bài báo đề xuất khung lý thuyết thống nhất cho **Agentic Science** dựa trên 3 trụ cột:

### 1. Thang đo 4 Cấp độ Tự chủ Khoa học (Autonomy Levels)

```
Level 1: Computational Oracle ➔ Level 2: Automated Assistant ➔ Level 3: Autonomous Partner ➔ Level 4: Generative Architect
(AlphaFold, specialized tools)   (Partial workflow, human-led)    (Full closed-loop discovery)   (Superintelligent scientific AI)
```

- **Level 1 — Computational Oracle (Công cụ tính toán chuyên biệt)**: AI giải một bài toán hẹp do con người giao (ví dụ: AlphaFold dự đoán cấu trúc protein).
- **Level 2 — Automated Research Assistant (Trợ lý tự động hóa một phần)**: AI tự chạy một chuỗi tác vụ nhỏ dưới sự giám sát chặt chẽ của con người.
- **Level 3 — Autonomous Scientific Partner (Đối tác khoa học tự chủ)**: AI vận hành vòng lặp khép kín: Đặt giả thuyết ➔ Thiết kế thí nghiệm ➔ Gọi robot/code thực thi ➔ Phân tích dữ liệu ➔ Tự điều chỉnh giả thuyết. *(Đây là mục tiêu trọng tâm hiện tại)*.
- **Level 4 — Generative Architect (Kiến trúc sư phát minh)**: AI vượt tầm trí tuệ con người, tự định hình các lý thuyết khoa học hoàn toàn mới (viễn cảnh tương lai).

### 2. Quy trình Khám phá 4 Giai đoạn (Dynamic 4-Stage Workflow)

```
[ Stage 1: Observation & Hypothesis ] ➔ [ Stage 2: Planning & Execution ]
                  ⬆                                       │
                  └────── [ Stage 4: Synthesis & Evolution ] ◄────── [ Stage 3: Data & Analysis ]
```

1. **Quan sát & Tạo Giả thuyết (Hypothesis Generation)**: Tổng hợp tri thức từ hàng triệu paper, phát hiện khoảng trống tri thức.
2. **Lập kế hoạch & Thực thi (Planning & Execution)**: Biên dịch kế hoạch thành mã điều khiển robot phòng lab (Robotic Workstations) hoặc mã chạy simulation.
3. **Phân tích Dữ liệu & Kết quả (Data Analysis)**: Xử lý phổ phổ khối (mass spec), hình ảnh kính hiển vi, dữ liệu cảm biến.
4. **Tổng hợp & Tiến hóa (Synthesis & Evolution)**: Đánh giá xem giả thuyết đúng hay sai để cập nhật bộ nhớ agent.

---

## Ranh Giới Năng Lực AI: Phân Biệt Thực Tế vs Claim

| Cấp độ | Phân loại Năng lực | Chi tiết trong *Agentic Science* |
| --- | --- | --- |
| 🟢 **AI làm được** | **Tự động hóa phòng lab đóng** | Tổng hợp quy trình hóa học tiêu chuẩn (retrosynthesis), chạy đường ống sinh tin học (bioinformatics pipelines), điều khiển tay máy robot thực hiện thao tác hút/trộn mẫu theo giao thức cố định. |
| 🟡 **AI làm được trong môi trường giới hạn** | **Vận hành Self-Driving Labs (SDLs)** | Các hệ thống như **A-Lab** (vật liệu) hoặc **RoboRXN** (hóa học): AI tự chọn phối hợp nguyên liệu, chạy robot nung/phân tích XRD, và tìm ra cấu trúc tinh thể/hợp chất mới trong không gian tìm kiếm xác định. |
| 🟠 **Cần Human Verification** | **Xác minh an toàn & Kiểm chứng thực tế** | Kiểm tra độ an toàn sinh học/hóa học (ngăn AI tự tạo ra độc tố hoặc chất nổ); xác minh tính tái lặp của thực nghiệm vật lý; đánh giá ý nghĩa sinh học thực sự của các mục tiêu thuốc (drug targets). |
| 🔵 **Thực sự chứng minh khả năng tự chủ** | **Vòng lặp đóng Level 3 tại phòng lab** | Chứng minh các hệ thống robot + LLM agent có thể vận hành liên tục nhiều ngày không cần người trực để tối ưu hóa phản ứng hóa học hoặc tổng hợp vật liệu mới. |
| 🔴 **Claim chưa được chứng minh** | **Vượt qua bài kiểm tra Nobel-Turing** | Tuyên bố AI có thể tự tạo ra các khám phá mang tính cách mạng nhận thức (paradigm shift) hoặc tự đề xuất lý thuyết vật lý mới mà con người chưa từng hình dung. |

---

## Key Results & Domain Breakdown

### 1. Khoa học Sự sống (Life Sciences)
- **Ứng dụng**: Tự động hóa thiết kế protein, phát triển thuốc (drug discovery), và phân tích đa omics (genomics/transcriptomics).
- **Hệ thống tiêu biểu**: Agent kết hợp với mô hình sinh phân tử để thiết kế kháng thể và tự động kiểm thử độc tính.

### 2. Hóa học (Chemistry)
- **Ứng dụng**: Tổng hợp hữu cơ (organic synthesis), tối ưu hóa phản ứng Hóa học.
- **Hệ thống tiêu biểu**: **ChemCrow**, **RoboRXN** — LLM agent gọi các công cụ tính toán hóa học và điều khiển robot tổng hợp phân tử mục tiêu.

### 3. Khoa học Vật liệu (Materials Science)
- **Ứng dụng**: Khám phá vật liệu bán dẫn, hợp kim, pin năng lượng mới.
- **Hệ thống tiêu biểu**: **A-Lab** (Lawrence Berkeley Lab) — tự động tổng hợp và phân tích hàng chục vật liệu vô cơ mới trong vài tuần.

### 4. Vật lý & Thiên văn học (Physics & Astronomy)
- **Ứng dụng**: Phân tích dữ liệu kính viễn vọng, mô phỏng động lực học chất lưu (CFD), tính toán lượng tử.

---

## Failure Modes & Challenges

1. **Khủng hoảng Tính tái lặp (Agentic Reproducibility)**: Thí nghiệm do Agent chạy khó tái lặp do sự thay đổi ngẫu nhiên của mô hình ngôn ngữ (non-deterministic LLM sampling).
2. **Nghẽn cổ chai Phần cứng / Robot (Physical Bottlenecks)**: Robot phòng lab dễ gặp sự cố cơ khí, nghẽn đường ống, hỏng mẫu mà LLM không thể nhận biết nếu thiếu cảm biến thị giác.
3. **Thẩm định Tính mới (Novelty Validation)**: Khó phân biệt giữa ý tưởng thực sự mới và việc AI tái phát minh lại (reinventing the wheel) những kiến thức đã có nhưng ẩn sâu trong tài liệu cũ.
4. **An toàn Sinh học & Đạo đức (Dual-use & Safety Risks)**: Agent tự chủ có nguy cơ vô tình thiết kế các tác nhân sinh học nguy hiểm hoặc độc tố hóa học.

---

## Paper này khác gì so với 2 Paper trước?

| Tiêu chí | 01 — Can AI agents conduct open-ended AI research? | 02 — Towards end-to-end automation of AI research | 03 — From AI for Science to Agentic Science |
| --- | --- | --- | --- |
| **Bản chất Paper** | Thực nghiệm đánh giá (Empirical Benchmark). | Kiến trúc hệ thống (System Architecture). | **Bài khảo sát tổng quan (Survey & Framework)**. |
| **Phạm vi Nghiên cứu** | Nghiên cứu AI mở (ML Research). | Nghiên cứu AI khép kín (ML Research). | **Toàn bộ Khoa học tự nhiên** (Sinh, Hóa, Vật liệu, Vật lý). |
| **Giao tiếp Thế giới thực** | Thuần túy phần mềm / GPU / Code. | Thuần túy phần mềm / GPU / Code. | **Kết hợp Phần mềm + Robot / Phòng thí nghiệm vật lý**. |
| **Mức độ Tự chủ** | Đánh giá thất bại ở Level 3. | Thực thi thành công Level 2-3 đóng. | **Phân loại toàn bộ từ Level 1 đến Level 4**. |

---

## Đóng góp vào câu hỏi "Autonomous Scientific Research"

Paper #03 cung cấp **bản đồ toàn cảnh (master roadmap)** giúp trả lời câu hỏi cốt lõi: 
AI không chỉ tự động hóa việc viết code hay báo cáo, mà đang từng bước làm chủ **vòng lặp thực nghiệm vật lý (physical closed-loop discovery)**. 

Tuy nhiên, paper khẳng định chúng ta hiện mới chỉ ở ngưỡng chuyển giao từ **Level 2 (Trợ lý tự động)** sang **Level 3 (Đối tác tự chủ trong môi trường hẹp)**. Sự hiện diện của con người ("Human-in-the-loop") vẫn là bắt buộc để đảm bảo an toàn, định hướng giá trị và xác minh tính đúng đắn khoa học.

---

## Câu hỏi tự suy nghĩ sau khi đọc

1. Khi AI kết hợp với robot phòng lab tự động hóa (Self-driving labs), làm thế nào để đảm bảo an toàn sinh học/hóa học mà không làm giảm tính tự chủ của agent?
2. Bài kiểm tra Nobel-Turing (Nobel-Turing Test) cần được thiết kế như thế nào để đo đạc chính xác thời điểm AI đạt Level 4?

---

## Concept / Paper tiếp theo đáng đọc

- 📖 **Reading Map**: [`topics/autonomous-ai-research.md`](../../topics/autonomous-ai-research.md) — Xem tổng hợp liên kết toàn bộ 3 paper để nắm trọn vẹn lộ trình phát triển của tự động hóa nghiên cứu khoa học.
