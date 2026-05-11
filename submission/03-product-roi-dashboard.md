# Product ROI Dashboard — GlucuCare AI
---

# Part A — Adoption Context

| Trường                        | Nội dung                                                                                                                                           |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Product                       | GlucuCare AI — AI meal logging & caregiver reassurance system cho gia đình có bố mẹ mắc tiểu đường                                                 |
| Người dùng chính              | (1) Caregiver 25–50 tuổi sống ở đô thị  (2) Người cao tuổi mắc tiểu đường type 2                                                                   |
| Workflow 1                    | **Meal capture → AI recognition**                                                                                                                  |
| AI làm gì?                    | Nhận diện món ăn từ ảnh chụp, phân loại món ăn Việt, gợi ý meal tags                                                                               |
| Human review ở đâu?           | Khi confidence < 80% → người dùng chọn lại từ top 3 suggestions                                                                                    |
| Nếu AI sai thì xử lý thế nào? | User/caregiver sửa tag → log correction → update dataset                                                                                           |
| Workflow 2                    | **Caregiver daily reassurance check**                                                                                                              |
| AI làm gì?                    | Tóm tắt trạng thái bữa ăn + glucose + alert bất thường                                                                                             |
| Human review ở đâu?           | Caregiver quyết định có gọi điện/can thiệp không                                                                                                   |
| Nếu AI sai thì xử lý thế nào? | Fallback sang raw meal history + manual review                                                                                                     |
| Workflow 3                    | **Risk alert & escalation**                                                                                                                        |
| AI làm gì?                    | Detect thiếu dữ liệu hoặc pattern nguy cơ (meal bất thường + glucose cao)                                                                          |
| Human review ở đâu?           | Caregiver xác nhận escalation                                                                                                                      |
| Nếu AI sai thì xử lý thế nào? | Alert phải explainable + có manual dismiss                                                                                                         |
| Workflow 4                    | **Long-term personalization loop**                                                                                                                 |
| AI làm gì?                    | Correlate meal patterns với glucose history để cá nhân hóa gợi ý                                                                                   |
| Human review ở đâu?           | Không đưa medical advice tự động; chỉ hiển thị pattern confidence                                                                                  |
| Nếu AI sai thì xử lý thế nào? | Disable personalized recommendation nếu confidence thấp                                                                                            |
| Rào cản ADKAR chính           | **Ability + Reinforcement**: người cao tuổi khó duy trì habit logging hằng ngày; caregiver dễ mất trust nếu AI nhận diện sai nhiều lần             |
| 3 adoption tactics            | (1) Camera-first frictionless UX  (2) Human-in-the-loop correction flow  (3) Dashboard alert chỉ xuất hiện khi cần để tránh “notification fatigue” |

---

# Part B — Product ROI Dashboard 

| Layer                     | Metric                                           | Baseline |           Target | Data source               | Owner        | Red-team risk                                     | Fix                                   |
| ------------------------- | ------------------------------------------------ | -------: | ---------------: | ------------------------- | ------------ | ------------------------------------------------- | ------------------------------------- |
| Product / Activation      | % elderly users upload ≥1 meal/day               |      25% |              60% | App event log             | Product Lead | Upload không chứng minh habit bền vững            | Add weekly consistency metric         |
| Product / Engagement      | % caregiver check dashboard ≥1/day               |      40% |              65% | Dashboard analytics       | Growth Lead  | User mở app vì lo lắng chứ không phải reassurance | Pair với “reduced call frequency”     |
| Workflow 1 / Productivity | Median meal logging time                         |  ~90 sec |          <15 sec | UX analytics              | Mobile Lead  | User upload nhanh nhưng AI sai                    | Pair với correction rate              |
| Workflow 1 / Quality      | AI meal recognition correction rate              |      35% |             <10% | Correction log            | AI Lead      | Avg accuracy che mất món hiếm                     | Segment by meal category              |
| Workflow 1 / Trust        | % users accepting AI suggestion without override |      45% |              75% | Suggestion acceptance log | AI PM        | User accept vì lười sửa                           | Add random QA sampling                |
| Workflow 2 / Value        | % caregiver self-report giảm gọi điện kiểm tra   |       0% |             >30% | Weekly survey             | CX Lead      | Self-report bias                                  | Cross-check with call frequency diary |
| Workflow 2 / Trust        | “Peace-of-mind score” caregiver (1-5)            |      2.8 |             >4.0 | In-app survey             | CX Research  | Emotional metric khó verify                       | Pair với retention + reduced calls    |
| Workflow 3 / Quality      | False positive alert rate                        |      28% |             <10% | Alert audit log           | AI Ops Lead  | Suppress alerts để đẹp metric                     | Pair với missed-risk rate             |
| Workflow 3 / Productivity | Median escalation response time                  |       6h |              <1h | Alert response log        | Ops Lead     | Fast response nhưng không effective               | Pair với escalation resolution        |
| Workflow 4 / Value        | % users seeing stable glucose trend after 30d    |  unknown | exploratory only | Glucose history           | Data Lead    | Correlation ≠ causation                           | Mark as experimental metric only      |
| Workflow 4 / Trust        | % personalized insights manually dismissed       |      40% |             <15% | Insight interaction log   | AI Lead      | Users ignore vì confusing UX                      | Add explanation + confidence label    |
| Value                     | Retention Day 30                                 |      12% |             >35% | Cohort analytics          | Growth Lead  | Retention vì guilt/family pressure                | Pair với satisfaction metric          |
| Value                     | ARPU/month                                       |    0 VNĐ |         180k VNĐ | Billing                   | Finance Lead | Revenue tăng nhưng trust giảm                     | Pair với churn + NPS                  |
| Value                     | Support tickets related to AI misunderstanding   |  unknown |  <5% users/month | Support CRM               | CX Ops       | User không report issue                           | Add proactive QA outreach             |

---

# Part C — Dashboard Mock

| **TILE 1: PRODUCT HEALTH** | **TILE 2: MEAL CAPTURE WORKFLOW** |
| --- | --- |
| **Metric:** Day-30 Retention | **Metric:** Meal logging time |
| **Current:** 12% | **Target:** >35% | **Current:** 90s | **Target:** <15s |
| **Status:** 🟡 AMBER | **Status:** 🟢 GREEN |
| **Action:** Improve onboarding | **Action:** Simplify UX flow |

| **TILE 3: CAREGIVER REASSURANCE** | **TILE 4: TRUST / QUALITY** |
| --- | --- |
| **Metric:** Reduced check-in calls | **Metric:** AI correction rate |
| **Current:** 18% | **Target:** >30% | **Current:** 35% | **Target:** <10% |
| **Status:** 🟡 AMBER | **Status:** 🔴 RED |
| **Action:** Improve summaries | **Action:** HITL + retraining |

| **TILE 5: VALUE** | **TILE 6: DECISION** |
| --- | --- |
| **Metric:** Peace-of-mind score | **Continue / Pivot / Kill:** **CONTINUE** |
| **Current:** 2.8/5 | **Target:** >4.0 | **Strongest metric:** Reduced calls |
| **Status:** 🟡 AMBER | **Before scale:** Improve trust layer |
| **Action:** Better alert tuning | **Owner:** Product + AI + CX Lead |


---

# Part D — Decision Memo

## 1. Continue / Pivot / Kill?

**Continue with guardrails.**

GlucuCare AI đang giải quyết một workflow có frequency rất cao (mọi bữa ăn hằng ngày) và emotional pain rõ ràng (“phải gọi điện kiểm tra bố mẹ”). Tuy nhiên, trust layer hiện chưa đủ mạnh để scale personalization hoặc autonomous recommendation.

---

## 2. Metric mạnh nhất là gì? Vì sao?

**Strongest metric: % caregiver giảm gọi điện kiểm tra hằng ngày.**

Đây là metric mạnh nhất vì:

* gắn trực tiếp với core pain;
* khó fake hơn DAU/prompt count;
* phản ánh behavioral change thật;
* chứng minh AI đang thay đổi workflow gia đình chứ không chỉ tạo novelty.

---

## 3. Metric nào đã thay sau red-team?

Ban đầu dùng:

* “số ảnh upload mỗi ngày”
* “AI recognition accuracy”

Thay bằng:

* reduced caregiver check-in calls;
* AI correction rate segmented by meal category;
* peace-of-mind score + retention pairing.

---

## 4. Trước khi scale, nhóm phải làm gì?

Trước khi scale:

1. Giảm AI correction rate xuống <10%.
2. Chứng minh retention >35% ở cohort 30 ngày.
3. Validate rằng “peace-of-mind” đi cùng reduced family tension chứ không chỉ novelty effect.
4. Giữ strict human-in-the-loop cho mọi health-related insight để tránh overtrust và medical hallucination.
