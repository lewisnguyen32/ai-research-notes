# 🗺️ Reading Path: Autonomous Scientific Research & AI Agents

> **Câu hỏi cốt lõi của Chủ đề:**  
> *"AI có thể tự thực hiện nghiên cứu khoa học đến mức nào mà không cần con người, hoặc có thể giảm sự phụ thuộc vào con người một cách đáng kể?"*

Lộ trình đọc này kết nối 3 bài báo quan trọng nhất đại diện cho các góc nhìn và giai đoạn phát triển khác nhau của tự động hóa nghiên cứu khoa học. Mục tiêu giúp người đọc hình thành một **bức tranh toàn cảnh về tiến trình khoa học (narrative progression)** thay vì đọc các bản tóm tắt rời rạc.

---

## 📍 Bản Đồ Đọc (Reading Map Flow)

```
[01. Can AI agents conduct open-ended AI research?] (Thực chứng & Ranh giới)
                         │
                         ▼ (Chuyển tiếp: Xây dựng quy trình tự động 100% như thế nào?)
[02. Towards end-to-end automation of AI research] (Kiến trúc & Tự động hóa Pipeline)
                         │
                         ▼ (Chuyển tiếp: Từ code AI mở rộng ra phòng lab thực tế Sinh/Hóa/Vật lý)
[03. From AI for Science to Agentic Science] (Khảo sát toàn cảnh & Khung lý thuyết)
```

---

## 📖 Chi Tiết Lộ Trình Đọc (Paper-by-Paper Progression)

### 🗺️ Mốc 01: Thực Chứng Ranh Giới Năng Lực AI trong Nghiên cứu Mở

📄 **[01. Can AI agents conduct open-ended AI research? Early evidence from two case studies](../papers/can-ai-agents-conduct-open-ended-ai-research/analysis.md)** (Kirgis et al., 2026)  
🔗 Links: 📝 [Analysis](../papers/can-ai-agents-conduct-open-ended-ai-research/analysis.md) | 🇻🇳 [Bản Dịch](../papers/can-ai-agents-conduct-open-ended-ai-research/translation-vi.md) | 📄 [PDF](../papers/can-ai-agents-conduct-open-ended-ai-research/paper.pdf)

- **Paper hỏi câu hỏi gì?**  
  Khi được cấp ngân sách tính toán thực tế ($3,000 API budget, GPU đầy đủ, 6 ngày làm việc) trên bài toán NeurIPS chưa công bố, liệu các AI Agent hàng đầu (Claude Opus 4.8, GPT-5.6 Sol) có thể tự chủ nghiên cứu khoa học mở hay không?
- **Nó chứng minh được gì?**  
  Chứng minh sự phân tách tuyệt đối giữa **Tầng Kỹ thuật R&D (Execution Layer)** và **Tầng Định hướng Nghiên cứu (Direction Layer)**. Agent đạt 100% tự chủ về kỹ thuật (coding, quản lý cluster, LaTeX, sửa lỗi build), nhưng thất bại 100% về mặt nghiên cứu khoa học mở (bị tác giả gốc từ chối hoàn toàn với điểm 1-2/6).
- **Nó chưa giải quyết được gì?**  
  Chưa tìm ra phương pháp giúp Agent vượt qua 5 Failure Modes (thiếu tư duy thẩm định, lạm phát điểm tự chấm, không biết backtrack cấp độ dự án, trôi dạt ngữ cảnh kéo dài).
- **Vì sao nên đọc paper tiếp theo?**  
  Paper #01 cho thấy AI thất bại ở bài toán mở không có hướng dẫn. Nhưng làm thế nào một hệ thống AI được thiết kế quy trình tự động 100% từ đầu đến cuối (end-to-end pipeline) lại có thể chạy thành công trong môi trường bài toán đóng? Đọc Paper #02 để hiểu kiến trúc của *The AI Scientist*.

---

### 🗺️ Mốc 02: Tự Động Hóa Toàn Diện Quy Trình Nghiên Cứu ML

📄 **[02. Towards end-to-end automation of AI research (The AI Scientist)](../papers/towards-end-to-end-automation-of-ai-research/analysis.md)** (Lu et al., Sakana AI / Nature 2026)  
🔗 Links: 📝 [Analysis](../papers/towards-end-to-end-automation-of-ai-research/analysis.md) | 🇻🇳 [Bản Dịch](../papers/towards-end-to-end-automation-of-ai-research/translation-vi.md) | 📄 [PDF](../papers/towards-end-to-end-automation-of-ai-research/paper.pdf)

- **Paper hỏi câu hỏi gì?**  
  Liệu có thể nối liền toàn bộ vòng đời nghiên cứu ML (từ phát sinh ý tưởng, tra cứu tài liệu, sửa code, chạy thực nghiệm, viết bài báo đến tự phản biện) thành một quy trình tự động 100% với chi phí thấp?
- **Nó chứng minh được gì?**  
  Chứng minh tính khả thi về mặt kiến trúc hệ thống: *The AI Scientist* tạo ra một bài báo khoa học đầy đủ cấu trúc với chi phí chỉ **~$15/bài**. Nó có thể tìm ra các cải tiến thuật toán nhỏ (learning rate schedule, loss function) trong các template mã nguồn có sẵn.
- **Nó chưa giải quyết được gì?**  
  Chưa giải quyết được hiện tượng trích dẫn ảo giác (hallucinated references), lạm phát chất lượng bài báo, và rủi ro agent "nịnh" mô hình LLM Reviewer. Khả năng phát minh bị giới hạn trong không gian template sẵn có.
- **Vì sao nên đọc paper tiếp me?**  
  Cả Paper #01 và #02 đều giới hạn phạm vi trong lĩnh vực Nghiên cứu AI (mã nguồn phần mềm). Nhưng làm thế nào tự động hóa nghiên cứu được áp dụng ra toàn bộ các ngành Khoa học tự nhiên thực nghiệm (Sinh học, Hóa học, Vật liệu, Vật lý) với sự xuất hiện của robot phòng thí nghiệm? Đọc Paper #03 để mở rộng tầm nhìn toàn cảnh.

---

### 🗺️ Mốc 03: Khảo Sát Toàn Cảnh & Khung Lý Thuyết Agentic Science

📄 **[03. From AI for Science to Agentic Science: A Survey on Autonomous Scientific Discovery](../papers/from-ai-for-science-to-agentic-science/analysis.md)** (Wei et al., 2025/2026)  
🔗 Links: 📝 [Analysis](../papers/from-ai-for-science-to-agentic-science/analysis.md) | 🇻🇳 [Bản Dịch](../papers/from-ai-for-science-to-agentic-science/translation-vi.md) | 📄 [PDF](../papers/from-ai-for-science-to-agentic-science/paper.pdf)

- **Paper hỏi câu hỏi gì?**  
  Sự chuyển dịch từ AI làm công cụ (*AI for Science*) sang AI làm đối tác tự chủ (*Agentic Science*) diễn ra như thế nào trên toàn bộ các ngành khoa học tự nhiên, và đâu là khung phân loại chuẩn cho tiến trình này?
- **Nó chứng minh được gì?**  
  Xây dựng thang đo **4 Cấp độ Tự chủ** (Oracle ➔ Assistant ➔ Partner ➔ Generative Architect) và quy trình **4 Giai đoạn**. Tổng hợp hàng loạt ứng dụng thực tế của Self-Driving Labs (như A-Lab, RoboRXN) kết hợp LLM agent với robot phòng thí nghiệm trong Sinh, Hóa, Vật liệu, Vật lý.
- **Nó chưa giải quyết được gì?**  
  Chưa giải quyết được thách thức về tính tái lặp thực nghiệm (agentic reproducibility), rào cản cảm biến cơ khí của robot, thẩm định tính mới thực sự, và nguy cơ an toàn sinh học/hóa học.
- **Tổng kết lộ trình đọc**:  
  Paper #03 cung cấp khung lý thuyết tổng thể để soi chiếu lại các phát hiện thực chứng của Paper #01 và Paper #02.

---

## 🎯 Bức Tranh Tổng Hợp: Trả Lời Câu Hỏi Cốt Lõi

Qua việc phân tích liên hoàn 3 bài báo, chúng ta rút ra câu trả lời trực tiếp cho câu hỏi: **"AI có thể tự nghiên cứu khoa học đến mức nào?"**

| Khía cạnh Nghiên cứu | Mức độ Tự chủ Hiện tại của AI | Bằng chứng từ Reading Path |
| --- | --- | --- |
| **1. Kỹ thuật & Thực thi (Execution)** | 🟢 **90% - 100% Tự chủ** | AI viết code, sửa lỗi traceback, vận hành script, điều khiển robot phòng lab, biên dịch LaTeX cực kỳ xuất sắc (*Paper #01 & #02*). |
| **2. Tối ưu hóa hẹp (Bounded Search)** | 🟡 **60% - 80% Tự chủ** | AI tự tìm các biến tấu thuật toán hoặc công thức vật liệu mới trong không gian template/tham số được con người thiết lập sẵn (*Paper #02 & #03*). |
| **3. Định hướng Giả thuyết Mở (Open Ideation)** | 🔴 **0% - 20% Tự chủ** | AI thất bại hoàn toàn khi tự định hình bài toán mở chưa có hướng dẫn, thiếu tư duy phản biện khắt khe và dễ rơi vào bế tắc tự đánh giá cao sản phẩm của mình (*Paper #01*). |
| **4. Mô hình Hợp tác Tối ưu** | 🤝 **Human-in-the-Loop** | Con người giữ vai trò **Navigator / Verifier** (Định hướng giả thuyết, duyệt an toàn, chọn bài toán) + AI đóng vai trò **Executor** (Viết code, chạy thí nghiệm, tổng hợp dữ liệu). |

---

## 📚 Liên kết Hệ thống & Tài liệu Tra cứu

- 📖 [Glossary - Thuật ngữ Chuyên ngành AI Research](../resources/glossary-ai-research-terms.md)
- 🤖 Topic liên quan: [AI Research & R&D Automation](ai-research-automation.md) | [AI Agents](ai-agents.md)
