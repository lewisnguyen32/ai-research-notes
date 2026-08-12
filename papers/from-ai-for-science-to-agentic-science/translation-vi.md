[← Library README](../../README.md) | [Reading Path](../../topics/autonomous-ai-research.md) | [Glossary](../../resources/glossary-ai-research-terms.md)

# Từ AI cho Khoa học đến Khoa học Agentic: Khảo sát về Khám phá Khoa học Tự chủ

**Tác giả:** Jiaqi Wei*, Yuejin Yang*, Xiang Zhang*, Yuhan Chen*, Xiang Zhuang*, Zhangyang Gao*, Dongzhan Zhou*, Siqi Sun†, Lei Bai†, Bowen Zhou† et al. (Phòng thí nghiệm AI Thượng Hải, Đại học Chiết Giang, Đại học Phục Đán, Đại học Thanh Hoa, CUHK, Đại học Giao thông Thượng Hải)  
**Mã bài báo:** arXiv:2508.14111v2 (20/10/2025)  
**Tài liệu gốc:** [arXiv:2508.14111](https://arxiv.org/abs/2508.14111) | [GitHub Repository](https://github.com/AgenticScience/Awesome-Agent-Scientists)  
**File PDF:** [`paper.pdf`](paper.pdf) | 📝 [Bản Phân Tích Chuyên Sâu](analysis.md)

---

## Tóm tắt nội dung (Abstract)

Trí tuệ nhân tạo (AI) đang tái thiết lập phương thức nghiên cứu khoa học, tiến hóa từ các công cụ tính toán chuyên biệt thành các đối tác nghiên cứu tự chủ. Chúng tôi định hình **Agentic Science (Khoa học Agentic)** là một giai đoạn bản lề trong mô hình *AI for Science*, nơi các hệ thống AI phát triển từ hỗ trợ một phần sang đạt được năng lực tự chủ khoa học toàn diện (full scientific agency).

Được thúc đẩy bởi các mô hình ngôn ngữ lớn (LLMs), hệ thống đa phương thức (multimodal systems) và các nền tảng nghiên cứu tích hợp, AI agent thể hiện các năng lực tự chủ bao gồm:
- Tự sinh giả thuyết (hypothesis generation).
- Thiết kế thực nghiệm (experimental design).
- Thực thi và phân tích (execution & analysis).
- Tự điều chỉnh lặp đi lặp lại (iterative refinement).

Bài khảo sát này cung cấp một cái nhìn tổng quan theo miền ứng dụng (domain-oriented review) về khám phá khoa học tự chủ trên các lĩnh vực: Khoa học sự sống, Hóa học, Khoa học vật liệu và Vật lý. Chúng tôi thống nhất 3 góc nhìn trước đây vốn bị phân tán — **hướng quy trình (process-oriented), hướng tự chủ (autonomy-oriented), và hướng cơ chế (mechanism-oriented)** — thông qua một khung lý thuyết toàn diện.

---

## 1. Sự Tiến hóa của AI for Science: Từ Công cụ đến Đối tác Tự chủ

Bài báo chia lịch sử ứng dụng AI trong nghiên cứu khoa học thành **4 Cấp độ Tự chủ (Four Levels of Autonomy)**:

### Cấp độ 1: Computational Oracle (Công cụ Tính toán Chuyên biệt)
- AI đóng vai trò như một cỗ máy trả lời câu hỏi tính toán hẹp (ví dụ: AlphaFold dự đoán cấu trúc 3D của protein, ESMFold).
- Con người đảm nhận 100% việc đặt câu hỏi, thiết kế thí nghiệm và phân tích ý nghĩa.

### Cấp độ 2: Automated Research Assistant (Trợ lý Nghiên cứu Tự động hóa Một phần)
- AI có thể thực hiện một chuỗi công việc tự động dưới sự chỉ dẫn trực tiếp của con người (ví dụ: chạy đường ống bioinformatic, tổng hợp tài liệu tự động).
- Quyết định chiến lược vẫn hoàn toàn do con người nắm giữ.

### Cấp độ 3: Autonomous Scientific Partner (Đối tác Khoa học Tự chủ)
- AI vận hành vòng lặp thực nghiệm khép kín (closed-loop discovery): Tự đưa ra giả thuyết ➔ Lập kế hoạch ➔ Thực thi thực nghiệm (gọi robot phòng lab hoặc simulation) ➔ Phân tích dữ liệu ➔ Tự cập nhật tri thức.
- Con người đóng vai trò giám sát an toàn và xác minh định hướng (Navigator/Verifier).

### Cấp độ 4: Generative Architect (Kiến trúc sư Phát minh)
- AI đạt mức tự chủ tuyệt đối, có khả năng đề xuất các lý thuyết khoa học mới vượt ngoài tầm hiểu biết hiện tại của con người và tự vận hành các mạng lưới nghiên cứu toàn cầu.

---

## 2. Quy trình Khám phá 4 Giai đoạn (Dynamic 4-Stage Workflow)

Mọi hệ thống Agentic Science đều vận hành dựa trên quy trình 4 bước liên hoàn:

1. **Quan sát & Đặt Giả thuyết (Observation & Hypothesis Generation)**: Quét toàn bộ kho văn bản khoa học, phát hiện các mâu thuẫn hoặc khoảng trống tri thức để đề xuất giả thuyết mới.
2. **Lập kế hoạch & Thực thi Thực nghiệm (Experimental Planning & Execution)**: Chuyển đổi giả thuyết thành các lệnh thực thi phần mềm hoặc mã điều khiển robot phòng lab (Self-Driving Labs).
3. **Phân tích Dữ liệu & Kết quả (Data & Result Analysis)**: Tự động xử lý dữ liệu thô từ các thiết bị phân tích (như quang phổ, kính hiển vi, máy giải trình tự gen).
4. **Tổng hợp & Tiến hóa Khoa học (Synthesis, Validation, & Evolution)**: Đánh giá giả thuyết dựa trên dữ liệu thu được, cập nhật bộ nhớ dài hạn (memory) để chuẩn bị cho chu kỳ nghiên cứu tiếp theo.

---

## 3. Tổng quan Ứng dụng theo Miền Khoa học (Domain Applications)

### 3.1. Khoa học Sự sống (Agentic Life Sciences)
- **Thiết kế Thuốc & Protein**: Agent phối hợp các mô hình sinh phân tử để tối ưu hóa cấu trúc kháng thể và tự động dự đoán độc tính.
- **Phân tích Đa Omics**: Agent tự động kết nối dữ liệu bộ gen (genomics) và dữ liệu biểu hiện gen (transcriptomics) để phát hiện mục tiêu điều trị bệnh mới.

### 3.2. Hóa học (Agentic Chemistry)
- **Tổng hợp Hữu cơ Tự chủ**: Các hệ thống như **ChemCrow** hay **RoboRXN** cho phép LLM agent kết nối trực tiếp với tay máy robot để pha chế và tổng hợp các hợp chất hóa học theo kế hoạch tự chọn.
- **Tối ưu hóa Phản ứng**: Agent tự điều chỉnh nhiệt độ, áp suất, dung môi trong thời gian thực để đạt hiệu suất phản ứng cao nhất.

### 3.3. Khoa học Vật liệu (Agentic Materials Science)
- **Phòng Thí nghiệm Tự lái (Self-Driving Labs - SDLs)**: Điển hình là **A-Lab** — kết hợp LLM với robot nung và máy đo nhiễu xạ tia X (XRD) để tổng hợp hàng chục vật liệu vô cơ chưa từng tồn tại.

### 3.4. Vật lý & Thiên văn học (Agentic Physics & Astronomy)
- **Xử lý Dữ liệu Quy mô Lớn**: Agent tự động lọc nhiễu dữ liệu từ kính viễn vọng không gian, phát hiện các hiện tượng thiên văn kỳ lạ hoặc hỗ trợ mô phỏng động lực học chất lưu (CFD).

---

## 4. Thử thách & Rào cản Cốt lõi (Core Challenges)

1. **Tính tái lặp của Agent (Agentic Reproducibility)**: Do tính chất không định hằng (non-deterministic) của mô hình LLM, hai lần chạy agent có thể đưa ra hai quy trình thực nghiệm khác nhau.
2. **Xác minh Tính mới (Novelty Validation)**: Rất khó để một AI agent biết chắc chắn ý tưởng của nó là "mới hoàn toàn" hay chỉ là sự lặp lại của một nghiên cứu cũ bị lãng quên.
3. **Tính Minh bạch trong Lập luận Khoa học**: Khi các hệ thống Multi-Agent trao đổi hàng ngàn tin nhắn, con người rất khó truy xuất nguồn gốc lập luận (traceability).
4. **An toàn & Đạo đức (Safety & Dual-Use Risks)**: Rủi ro agent tự động tạo ra các độc tố hóa học hoặc tác nhân sinh học nguy hiểm mà không có sự kiểm duyệt.

---

## 5. Triển vọng Tương lai: Bài kiểm tra Nobel-Turing (Nobel-Turing Test)

Bài báo kết luận bằng việc đưa ra tầm nhìn về **Bài kiểm tra Nobel-Turing (Nobel-Turing Test)**: Cột mốc đánh giá thời điểm một hệ thống AI tự chủ có thể tạo ra một phát minh khoa học độc lập đạt tầm vóc giải Nobel mà không cần sự can thiệp của con người.

Agentic Science không phải là sự thay thế nhà khoa học con người, mà là sự nâng tầm mối quan hệ cộng sinh (symbiotic partnership): Con người đưa ra tầm nhìn, giá trị và sự thẩm định; AI cung cấp khả năng mở rộng quy mô thực nghiệm và khám phá không giới hạn.
