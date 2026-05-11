## B. Case Comparison — Nhóm

| Trường | Case thành công / tín hiệu tốt | Case cảnh báo / thất bại |
| --- | --- | --- |
| **Case** | Morgan Stanley + OpenAI AI Assistant | JPMorgan AI Usage Dashboard |
| **Workflow có AI** | Tư vấn tài chính (Tìm kiếm tri thức nội bộ, tóm tắt họp, chuẩn bị tài liệu khách hàng). | Lập trình phần mềm (Theo dõi việc sử dụng Copilot, Claude, ChatGPT). |
| **Metric chính** | Tỷ lệ adoption (98%), tỷ lệ truy cập tài liệu (tăng từ 20% → 80%), thời gian tìm kiếm giảm. | Số lần tương tác với AI, phân loại tần suất sử dụng (Heavy/Light users). |
| **Metric đó chứng minh được gì?** | AI thực sự khớp với quy trình làm việc, tạo ra thói quen sử dụng hàng ngày và tăng hiệu suất tra cứu. | Công ty đang quyết liệt ép tiến độ áp dụng AI và nhân viên có tương tác với công cụ. |
| **Metric đó chưa chứng minh được gì?** | Doanh thu tăng trực tiếp bao nhiêu hay mức độ hài lòng của khách hàng cuối. | Hiệu suất thực tế của kỹ sư có tăng hay chất lượng sản phẩm có tốt hơn không. |
| **Thiếu metric nào?** | Doanh thu trên mỗi tư vấn viên, tỷ lệ giữ chân khách hàng, tỷ lệ sai sót/ảo giác (hallucination). | Thời gian tiết kiệm thực tế, tốc độ bàn giao dự án, chất lượng code. |
| **Bài học cho dashboard nhóm** | Tập trung vào việc giảm ma sát trong quy trình và tạo ra sự phụ thuộc tích cực (behavioral dependency). | Tránh việc đo đạc hời hợt dẫn đến việc nhân viên "đối phó" với các chỉ số ảo (vanity metrics). |

---

## Câu chốt

**Case thành công dạy nhóm tôi rằng:**
AI chỉ thực sự được đón nhận khi nó giải quyết được các điểm nghẽn trong công việc hàng ngày, giúp người dùng làm việc nhàn hơn nhưng hiệu quả hơn, từ đó tạo ra sự gắn kết tự nhiên thay vì ép buộc.

**Case cảnh báo / thất bại dạy nhóm tôi rằng:**
Các chỉ số về hoạt động (activity metrics) rất dễ bị thao túng. Nếu dashboard chỉ tập trung vào "số lượng" mà bỏ qua "chất lượng" và "kết quả", nó sẽ dẫn đến sự lãng phí nguồn lực và báo cáo sai lệch về giá trị thực tế của AI.

**Vì vậy dashboard nhóm tôi phải:**

* Loại bỏ việc dùng số lượng prompt/login làm KPI chính.
* Phân biệt rõ ràng giữa "Hoạt động AI" (Activity) và "Giá trị AI" (Value).
* Ưu tiên các chỉ số gắn liền với kết quả công việc (Outcome) và độ chính xác của quy trình.
* Tập trung đo lường mức độ giảm thiểu gánh nặng công việc (friction reduction) cho người dùng.

---

**Tự kiểm tra:**

* [x] Không chỉ kể chuyện case.
* [x] Có nêu metric cụ thể (98% adoption, 20% -> 80% document access, Light/Heavy classification).
* [x] Có nói metric chứng minh được gì và chưa chứng minh được gì.
* [x] Có bài học áp dụng trực tiếp cho thiết kế dashboard.


##  Sources

### Morgan Stanley

* [OpenAI x Morgan Stanley case study](https://openai.com/customer-stories/morgan-stanley)
* [Morgan Stanley AI Debrief launch](https://www.morganstanley.com/press-releases/ai-at-morgan-stanley-debrief-launch)
* [Morgan Stanley AI productivity survey](https://www.morganstanley.com/insights/articles/ai-adoption-accelerates-survey-find)

* [Morgan Stanley wealth advisors are about to get an OpenAI-powered assistant to do their grunt work
](https://www.cnbc.com/2024/06/26/morgan-stanley-openai-powered-assistant-for-wealth-advisors.html)
### JPMorgan
* [Inside the dashboards JPMorgan is using to track and rank engineers' AI use](https://www.businessinsider.com/jpmorgan-track-software-engineers-ai-use-dashboards-2026-4)
* [JPMorgan Chase to Track Employee AI Usage With New Dashboard](https://www.wsj.com/articles/jpmorgan-chase-to-track-employee-ai-usage-with-new-dashboard-9c8e1b9b)