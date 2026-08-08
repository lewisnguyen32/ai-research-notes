# Thuật Ngữ Chuyên Ngành AI Research & Agentic Evaluation (Glossary)

Tài liệu này tổng hợp các thuật ngữ chuyên ngành Machine Learning, AI Agents và Đánh giá Tự động hóa R&D (AI R&D Automation) trích xuất từ bài báo *Can AI agents conduct open-ended AI research? Early evidence from two case studies* ([arXiv:2607.27191v1](https://arxiv.org/abs/2607.27191)).

---

## 1. Phương pháp & Khái niệm Đánh giá AI (AI Evaluation Concepts)

| Thuật ngữ Tiếng Anh | Khái niệm Tiếng Việt | Giải thích / Ngữ cảnh trong Bài báo |
| :--- | :--- | :--- |
| **Open-ended AI Research** | Nghiên cứu AI mở | Nghiên cứu khoa học không có câu hỏi đóng hay chỉ số đo đạc cố định, đòi hỏi tự đưa ra giả thuyết, thiết kế thực nghiệm và đánh giá đóng góp khoa học. |
| **Verifiable Tasks / Benchmarks** | Tác vụ có thể kiểm chứng | Các bài test tự động đánh giá Agent bằng một chỉ số duy nhất (ví dụ: điểm số Kaggle trong MLE-Bench, tỷ lệ tái hiện trong CORE-Bench). |
| **Blind Peer Review** | Phản biện kín / Phản biện độc lập | Quy trình đánh giá bài báo khoa học mà người phản biện không biết tác giả là ai (và ngược lại). |
| **Shadow Evaluations** | Đánh giá bóng | Phương pháp đánh giá mới: Giao câu hỏi nghiên cứu của một bài báo chưa công bố cho Agent thực hiện, sau đó nhờ chính tác giả gốc phản biện sản phẩm. |
| **Uncontaminated Questions** | Câu hỏi không bị rò rỉ dữ liệu | Câu hỏi nghiên cứu hoàn toàn mới, chưa từng xuất hiện trên internet hay tập dữ liệu huấn luyện của AI. |
| **Generator-Verifier Gap** | Khoảng cách sinh - kiểm chứng | Khoảng cách giữa khả năng tạo ra sản phẩm (sinh mã, viết bài báo) và khả năng tự kiểm tra, nhận biết chất lượng sản phẩm đó. |
| **Scaffold / Agent Scaffold** | Khung điều phối Agent | Khung phần mềm quản lý vòng lặp chạy của Agent, phối hợp công cụ (tools), subagents và môi trường tính toán (như OpenClaw, Codex). |
| **Scaffold Overhang** | Dư thừa năng lực mô hình | Hiện tượng năng lực thực sự của mô hình AI bị kìm hãm do khung điều phối (scaffold) bị lỗi hoặc thiếu công cụ/hướng dẫn phù hợp. |

---

## 2. Các Chế độ Thất bại của Agent (Agent Failure Modes)

| Thuật ngữ Tiếng Anh | Khái niệm Tiếng Việt | Giải thích / Ngữ cảnh trong Bài báo |
| :--- | :--- | :--- |
| **Failure Modes** | Chế độ / Mô hình thất bại | Các kiểu hành vi hoặc điểm yếu lặp đi lặp lại dẫn đến thất bại của Agent trong quá trình nghiên cứu. |
| **Lack of Judgment** | Thiếu năng lực đánh giá tiêu chuẩn | AI không có nhận thức đúng đắn về chuẩn mực của một bài báo khoa học chất lượng cao (chấp nhận kết quả yếu, dữ liệu kém). |
| **Lack of Creative Problem Solving** | Thiếu giải quyết vấn đề sáng tạo | AI không biết đổi mới hướng đi hoặc tái cấu trúc thực nghiệm khi các giả thuyết ban đầu bị bác bỏ. |
| **Backtracking / Effective Backtracking** | Quay đầu / Lùi bước khôi phục | Khả năng từ bỏ hướng đi bế tắc để quay lại bước trước đó hoặc thử nghiệm một phương pháp hoàn toàn mới từ đầu. |
| **Context Rot / Compaction** | Suy giảm ngữ cảnh / Nén ngữ cảnh | Hiện tượng Agent quên hoặc làm trôi dạt thông tin/hướng dẫn quan trọng sau nhiều vòng lặp nén lịch sử trò chuyện. |
| **Instruction Drift** | Trôi dạt hướng dẫn | Hiện tượng Agent bắt đầu tuân thủ hướng dẫn ban đầu nhưng dần bỏ qua các quy định cứng theo thời gian chạy kéo dài. |
| **Epistemic Lock-in** | Bế tắc nhận thức / Cố chấp giả thuyết | Agent bị mắc kẹt vào giả thuyết ban đầu và không thể thoát ra để nhìn nhận vấn đề theo góc nhìn khác. |
| **Proof by Example Fallacy** | Ngụy biện chứng minh bằng ví dụ | Ngụy biện quy nạp vội vàng: thử thất bại một vài trường hợp nhỏ rồi kết luận chung rằng toàn bộ phương pháp là vô hiệu. |
| **Post Hoc Choices** | Lựa chọn diễn giải sau | Đưa ra các quyết định thực nghiệm hoặc giải thích phương pháp một cách bừa bãi sau khi đã có kết quả, thiếu căn cứ khoa học ban đầu. |

---

## 3. An toàn AI & Liêm chính Thực nghiệm (AI Safety & Empirical Integrity)

| Thuật ngữ Tiếng Anh | Khái niệm Tiếng Việt | Giải thích / Ngữ cảnh trong Bài báo |
| :--- | :--- | :--- |
| **Reward Hacking** | Trục lợi phần thưởng | Hành vi AI tìm cách gian lận hoặc khai thác kẽ hở của hệ thống chấm điểm để đạt điểm cao mà không giải quyết đúng bản chất bài toán. |
| **Emergent Misalignment** | Mất cân bằng / Lệch lạc phát sinh | Hiện tượng tinh chỉnh (fine-tuning) mô hình trên các dữ liệu phong cách lệch lạc nhỏ dẫn đến sự lệch lạc hành vi trên diện rộng. |
| **P-hacking** | Thao tác giá trị p | Hành vi cố tình thử nghiệm nhiều lần hoặc thay đổi cách tính toán cho đến khi thu được kết quả có ý nghĩa thống kê ($p < 0.05$). |
| **Cherry-picking** | Chọn lọc dữ liệu có lợi | Chỉ báo cáo những kết quả tốt/phù hợp với giả thuyết và lờ đi các kết quả thất bại hoặc trái ngược. |
| **Negative-results Paper** | Bài báo báo cáo kết quả tiêu cực | Bài báo tập trung chứng minh một phương pháp/giả thuyết không hoạt động (thay vì tìm ra giải pháp tích cực mới). |

---

## 4. Thuật ngữ Kỹ thuật & Mô hình (Technical & Model Terms)

| Thuật ngữ Tiếng Anh | Khái niệm Tiếng Việt | Giải thích / Ngữ cảnh trong Bài báo |
| :--- | :--- | :--- |
| **LLM Persona** | Tính cách / Đặc tính định hình LLM | Mẫu hành vi, văn phong hoặc đặc tính ổn định của mô hình ngôn ngữ lớn sau khi tinh chỉnh hoặc điều hướng. |
| **Weight-Space Interventions** | Can thiệp không gian trọng số | Phương pháp điều chỉnh trực tiếp các trọng số (weights) của mô hình (ví dụ: hiệu trọng số $W_{finetuned} - W_{base}$). |
| **Activation Steering** | Điều hướng kích hoạt | Phương pháp can thiệp vào các vectơ kích hoạt (activations) trong quá trình lan truyền tiến (forward pass) để lái hành vi LLM. |
| **Trait Space** | Không gian đặc tính | Tọa độ đại diện cho các thuộc tính/tính cách khác nhau trong không gian trọng số hoặc kích hoạt của mô hình. |
| **Prior-Fitted Networks (PFNs)** | Mạng khớp phân phối tiên nghiệm | Dòng mô hình nền tảng dữ liệu bảng (như TabPFN) học suy luận trong ngữ cảnh (in-context) qua một lần lan truyền tiến mà không cần cập nhật trọng số. |
| **Distribution Shift Detector** | Bộ phát hiện dịch chuyển phân phối | Thuật toán phát hiện xem dữ liệu triển khai thực tế có bị trượt/khác biệt so với dữ liệu huấn luyện ban đầu hay không. |
| **Covariate Shift $p(x)$** | Dịch chuyển biến độc lập / Hiệp biến | Phân phối đầu vào $p(x)$ thay đổi nhưng mối quan hệ $p(y\|x)$ giữ nguyên. |
| **Concept Shift $p(y\|x)$** | Dịch chuyển khái niệm | Mối quan hệ giữa đầu vào và nhãn $p(y\|x)$ thay đổi (ví dụ: định nghĩa nhãn bị thay đổi). |
| **In-context Support Set** | Tập hỗ trợ trong ngữ cảnh | Tập dữ liệu có dán nhãn được đưa vào ngữ cảnh làm ví dụ cho mô hình PFN học tại thời điểm suy luận. |
| **Wall-clock Time** | Thời gian thực / Thời gian đồng hồ | Thời gian trôi qua thực tế theo đồng hồ (phân biệt với thời gian tính toán của GPU hay số lượt token). |
