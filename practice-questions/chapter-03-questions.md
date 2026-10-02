## Chapter 3: AI Feasibility, Risk Assessment, and Scope Definition — Practice Questions

**Q1.** A retail company wants to reduce customer service costs by implementing an AI chatbot. Which is a technical feasibility question that should be evaluated first?

A) Whether employees will trust the chatbot's recommendations
B) Whether the chatbot will improve brand sentiment scores
C) Whether the company's cloud budget and infrastructure support GPU-based training and scaled inference
D) Whether competitors have already deployed similar chatbots

<details>
<summary>Answer</summary>

**Correct: C**

Technical feasibility evaluates whether the required compute, infrastructure, and integration capability exist to build and run the solution.

**Why the others are wrong:**
- Employee trust/adoption is an organizational feasibility concern, not technical.
- Sentiment improvement is a business outcome metric, not a feasibility question.
- Competitive analysis informs strategy, not technical feasibility.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A healthcare provider wants to build a predictive model for patient readmission. The legal team reveals that patient records prior to 2021 lack a unique identifier for linking across systems. Which feasibility category is primarily affected?

A) Organizational feasibility
B) Ethical risk
C) Technical feasibility
D) Data feasibility

<details>
<summary>Answer</summary>

**Correct: D**

Availability, quality, and linkability of source data are core data feasibility concerns.

**Why the others are wrong:**
- Organizational feasibility concerns culture and change readiness, not record linkage.
- Ethical risk concerns bias/fairness, not data structure gaps.
- Technical feasibility concerns compute/infrastructure, not data quality.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A manufacturing company has skilled engineers and executive sponsorship, but line workers fear the AI system will replace their jobs and are resisting pilot testing. Which feasibility dimension is most at risk?

A) Technical
B) Data
C) Financial
D) Organizational

<details>
<summary>Answer</summary>

**Correct: D**

Workforce resistance and change-management concerns fall under organizational feasibility.

**Why the others are wrong:**
- Technical feasibility is unrelated to worker sentiment.
- Data feasibility is not mentioned in the scenario.
- Financial feasibility is not addressed here; the issue is human/cultural.

</details>

---

**Q4.** A finance team calculates late-payment fees using a fixed set of business rules that rarely change. After an honest feasibility comparison, which approach should the project team recommend?

A) Use a deterministic rules engine, since ML adds no value for stable, deterministic logic
B) Deploy a machine learning model trained on historical payment data
C) Use a large language model to interpret payment policies at runtime
D) Build a deep learning model to detect late-payment patterns and auto-set fees

<details>
<summary>Answer</summary>

**Correct: A**

When logic is deterministic and stable, a rules-based approach is more explainable, cheaper, and easier to maintain than an AI model.

**Why the others are wrong:**
- ML introduces unnecessary complexity and maintenance for logic that doesn't change.
- An LLM introduces non-determinism and inconsistency for a task requiring fixed calculation.
- Deep learning is overengineering for a rule-based problem, mirroring option A's flaw.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A logistics company's regression-based demand forecasting model already achieves 95% accuracy and is well maintained. The project sponsor requests replacing it with a deep learning model. What should the feasibility assessment recommend?

A) Recommend against replacement unless the deep learning model demonstrates measurable improvement that justifies the added cost and complexity
B) Proceed with the replacement because deep learning is more modern
C) Replace immediately since deep learning always outperforms regression
D) Rebuild from scratch using deep learning without comparing it to the existing model

<details>
<summary>Answer</summary>

**Correct: A**

Feasibility assessment requires an honest, evidence-based comparison of AI versus existing alternatives; added complexity must be justified by measurable value.

**Why the others are wrong:**
- Novelty ('more modern') is never a valid feasibility justification.
- Deep learning does not always outperform simpler models — this is a false absolute.
- Skipping comparison contradicts the requirement for an honest feasibility evaluation.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** Which of the following pairs correctly reflects proper AI project scope statement content?

A) Success criteria: 'Team likes the model' / Out-of-scope: 'Documentation'
B) In-scope: 'Model will be retrained quarterly' / Out-of-scope: 'Real-time inference for the mobile app'
C) In-scope: 'Increase morale' / Success criteria: 'Model accuracy ≥ 90%'
D) Out-of-scope: 'Achieve business goals' / In-scope: 'Undefined future enhancements'

<details>
<summary>Answer</summary>

**Correct: B**

Both items are specific and measurable — a defined maintenance activity in-scope and a clearly excluded capability out-of-scope.

**Why the others are wrong:**
- 'Team likes the model' is not a measurable success criterion.
- 'Increase morale' is not a valid, quantifiable in-scope deliverable.
- 'Achieve business goals' is too broad for out-of-scope, and 'undefined future enhancements' should never be listed as in-scope.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** During a risk assessment for a hiring screening AI tool, the team discovers the model rejects qualified candidates from a specific demographic group at a much higher rate than others. This finding falls under which risk category?

A) Security risk
B) Safety risk
C) Financial risk
D) Ethical risk

<details>
<summary>Answer</summary>

**Correct: D**

Disparate outcomes across demographic groups represent a bias/fairness issue, classified as ethical risk in CPMAI's risk framework.

**Why the others are wrong:**
- Security risk concerns unauthorized access or breach, not disparate model outcomes.
- Safety risk concerns physical or systemic harm, not fairness in decision outcomes.
- Financial risk may be a downstream consequence but is not the primary classification tested here.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which best describes the primary difference between a safety risk and a security risk in AI risk assessment?

A) Safety risk concerns potential harm to people or physical systems from AI failure; security risk concerns unauthorized access, breaches, or malicious manipulation of the AI system
B) Safety risk concerns cost overruns; security risk concerns schedule delays
C) Safety and security risk are interchangeable terms in CPMAI risk assessment
D) Safety risk applies only to robotics; security risk applies only to cloud-based AI

<details>
<summary>Answer</summary>

**Correct: A**

This is the accepted CPMAI distinction: safety relates to harm from system failure, security relates to unauthorized access or manipulation.

**Why the others are wrong:**
- These are generic project management concerns (cost/schedule), not the AI risk categories tested.
- The two categories are explicitly distinct in the CPMAI risk framework, not interchangeable.
- Both risk types apply broadly across AI system types, not restricted to robotics or cloud alone.

</details>

---

