## Version 1.0
# Mẫu 00 — Bảng So Sánh Case Thành Công / Thất Bại

Mục tiêu của bài này: đọc case thật để biết chỉ số nào chứng minh được giá trị (value), chỉ số nào chỉ tạo cảm giác tốt.

## Chọn Case

| Nhóm case                 | Gợi ý              |
| ------------------------- | ------------------ |
| Thành công / tín hiệu tốt | Morgan Stanley     |
| Thất bại / cảnh báo       | JPMorgan dashboard |

---

## Bảng Điền

| Trường                             | Case thành công                                                                                                                                               | Case thất bại/cảnh báo                                                                                                                                                            |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Case                               | Morgan Stanley + OpenAI AI Assistant                                                                                                                          | JPMorgan AI Usage Dashboard                                                                                                                                                       |
| AI được dùng trong quy trình nào?  | Financial advisors dùng AI để search internal knowledge, summarize meeting, retrieve documents, prep trước meeting với khách hàng                             | Theo dõi mức độ dùng AI của engineers: GitHub Copilot, Claude, ChatGPT trong coding workflow                                                                                      |
| Người dùng chính là ai?            | Financial advisors / wealth management teams                                                                                                                  | Software engineers / technology division managers                                                                                                                                 |
| Họ đo chỉ số gì?                   | - 98% advisor teams adoption  <br> - Document access tăng từ 20% → 80%  <br> - Search time giảm  <br> - Advisors spend more time with clients                 | - Số lần dùng Copilot/Claude  <br> - AI activity frequency  <br> - “Light / Heavy / Non-user” classification  <br> - Active AI user count                                         |
| Chỉ số đó thuộc lớp nào?           | - Adoption → Engagement  <br> - Retrieval efficiency → Productivity  <br> - More client time → Value  <br> - Daily usage → Trust                              | <br> - Activation  <br> - Engagement                                                                                                                                 |
| Chỉ số đó chứng minh được gì?      | - AI fit workflow thật  <br> - Advisors quay lại dùng hằng ngày  <br> - Knowledge retrieval hiệu quả hơn  <br> - AI giúp tiết kiệm thời gian và tăng leverage | - Nhân viên có mở AI tools  <br> - Công ty đang push adoption mạnh  <br> - Có visibility về mức độ dùng AI                                                                        |
| Chỉ số đó chưa chứng minh được gì? | - Chưa chứng minh trực tiếp revenue tăng bao nhiêu  <br> - Chưa chứng minh client satisfaction tăng bao nhiêu  <br> - Chưa đo quality investment advice       | - Không chứng minh productivity tăng  <br> - Không chứng minh code quality tốt hơn  <br> - Không chứng minh business outcome tăng  <br> - Không chứng minh AI usage là meaningful |
| Thiếu chỉ số nào?                  | - Revenue/advisor  <br> - Client retention  <br> - Accuracy / hallucination rate  <br> - Trust score theo workflow                                            | - Time saved per task  <br> - Bug reduction  <br> - PR review speed  <br> - Code acceptance rate  <br> - Engineering throughput  <br> - Quality metrics                           |
| Rủi ro lớn nhất                    | Over-reliance vào AI retrieval hoặc hallucination trong advisory workflow nếu trust vượt quá verification                                                     | Goodhart’s Law: nhân viên optimize để “trông như đang dùng AI” thay vì tạo value thật; dễ sinh performative adoption                                                              |
| Bài học cho dashboard nhóm         |             | Không dùng prompt count / AI sessions làm KPI chính. Nếu đo activity metric thì phải gắn với outcome metric để tránh vanity adoption.                                             |

---

## Câu Chốt Của Nhóm

```markdown
Case thành công dạy nhóm tôi rằng:


Case thất bại/cảnh báo dạy nhóm tôi rằng:


Vì vậy dashboard nhóm tôi phải tránh:
-
```

---

## Tự kiểm tra

* [x] Không chỉ kể chuyện case.
* [x] Có nêu chỉ số cụ thể.
* [x] Có nói chỉ số chứng minh được gì và không chứng minh được gì.
* [x] Có ít nhất 1 bài học áp dụng vào dashboard nhóm.
