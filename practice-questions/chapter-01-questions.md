## Chapter 1: Responsible AI Foundations: Privacy, Bias, and Governance — Practice Questions

**Q1.** A company is testing a facial-recognition model used in hiring before production deployment. Which approach BEST detects bias across demographic groups?

A) Compute the disparate impact ratio (four-fifths rule) and compare subgroup performance metrics (TPR/FPR) across protected groups
B) Measure overall model accuracy on the full test set only
C) Accept the vendor's third-party fairness certification without internal testing
D) Survey a sample of employees about their perception of fairness

<details>
<summary>Answer</summary>

**Correct: A**

Fairness testing requires quantitative subgroup analysis (selection rate ratios, TPR/FPR by group) — overall accuracy can mask disparities hidden within aggregate numbers.

**Why the others are wrong:**
- Aggregate accuracy hides subgroup disparities — a model can be 95% accurate overall while failing badly for one demographic.
- Vendor certification is not a substitute for the deploying organization's own documented bias testing and accountability.
- Perception surveys are qualitative and don't satisfy quantitative fairness testing or audit requirements.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** An organization plans to deploy an AI model trained on EU customer data that will make automated decisions with legal effects on individuals. Which document must be completed BEFORE deployment under GDPR?

A) A Data Protection Impact Assessment (DPIA)
B) A model card summarizing training data
C) A SOC 2 Type II audit report
D) A business continuity and disaster recovery plan

<details>
<summary>Answer</summary>

**Correct: A**

GDPR Article 35 mandates a DPIA whenever processing — including automated decision-making with legal or significant effects — is likely to result in high risk to individuals' rights.

**Why the others are wrong:**
- A model card documents the model but has no legal standing under GDPR.
- SOC 2 addresses security controls, not GDPR-specific privacy risk assessment.
- A BCDR plan addresses operational resilience, not data protection risk.

</details>

---

**Q3.** A business stakeholder wants to understand why a specific customer was denied a loan by a gradient-boosting model. Which explainability technique BEST provides this individual-level explanation?

A) Global feature importance from the training log
B) A confusion matrix from the validation set
C) The model's ROC curve
D) SHAP (Shapley Additive Explanations)

<details>
<summary>Answer</summary>

**Correct: D**

SHAP produces per-instance attributions showing how much each feature contributed to that specific prediction, ideal for individual decision explanations.

**Why the others are wrong:**
- Global feature importance explains overall model behavior, not one customer's outcome.
- A confusion matrix summarizes aggregate classification performance, not individual predictions.
- An ROC curve evaluates overall discrimination threshold performance, not a single decision.

</details>

---

**Q4.** A regulator asks a team to reproduce results from a model deployed six months ago. The team cannot identify which dataset snapshot was used for that training run. What governance control was missing?

A) API rate limiting configuration
B) Load balancer failover settings
C) Network firewall rule documentation
D) Data and model versioning with lineage tracking

<details>
<summary>Answer</summary>

**Correct: D**

Reproducibility for audits requires versioned datasets, models, and training runs with lineage linking each to a specific artifact and timestamp.

**Why the others are wrong:**
- Rate limiting is a performance/security control unrelated to reproducibility.
- Load balancer settings concern infrastructure availability, not data/model traceability.
- Firewall rules govern network access, not artifact versioning.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A team applies sample reweighting to correct demographic parity issues before training begins. At which stage of bias mitigation does this technique belong?

A) In-processing
B) Pre-processing
C) Post-processing
D) Monitoring after deployment

<details>
<summary>Answer</summary>

**Correct: B**

Reweighting modifies the training data distribution before the model is trained, which defines it as a pre-processing mitigation technique.

**Why the others are wrong:**
- In-processing modifies the learning algorithm itself (e.g., fairness constraints, adversarial debiasing) during training.
- Post-processing adjusts model outputs or decision thresholds after training is complete.
- Deployment monitoring detects drift after the model is live, not before training.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** Which access control practice for training data containing PII BEST satisfies both least-privilege and audit trail requirements?

A) Shared administrator credentials used by the entire data science team
B) Role-based access control (RBAC) with individual logging of every access to PII fields
C) Public read access to the dataset combined with encryption at rest
D) Unencrypted storage accessible only through a VPN connection

<details>
<summary>Answer</summary>

**Correct: B**

RBAC restricts access to only what each role needs, and individual logging creates the audit trail required to trace who accessed PII and when.

**Why the others are wrong:**
- Shared credentials make it impossible to attribute access to a specific individual, breaking audit accountability.
- Public access violates least privilege regardless of encryption at rest.
- VPN-only access without encryption at rest fails to protect data confidentiality and doesn't provide field-level access logging.

</details>

---

**Q7.** What is the primary distinction between explainability and interpretability in AI governance?

A) The two terms are interchangeable with no practical difference
B) Explainability applies only to deep learning models, interpretability only to linear models
C) Interpretability is a legal requirement while explainability is optional
D) Interpretability describes how a model's internal logic works; explainability provides a post-hoc justification for a specific output

<details>
<summary>Answer</summary>

**Correct: D**

Interpretability is an intrinsic property of a model's structure (e.g., a decision tree is inherently interpretable), while explainability refers to techniques (like SHAP/LIME) that generate after-the-fact justifications for outputs of any model, including black boxes.

**Why the others are wrong:**
- They describe distinct concepts tested separately on the exam.
- Both terms apply across model types — explainability tools are especially used FOR black-box deep learning but aren't exclusive to it.
- Neither term alone is a defined universal legal requirement; requirements depend on jurisdiction and risk level.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** A regulatory audit requires an organization to demonstrate a documented chain-of-custody for a high-risk AI model, including who approved it for production. Which artifact BEST satisfies this requirement?

A) A marketing press release announcing the model launch
B) A go/no-go decision log with sign-off from risk, legal, and technical leads, linked to the model version and test results
C) The README file in the model's source code repository
D) A project management ticket with no recorded approvals

<details>
<summary>Answer</summary>

**Correct: B**

A formal go/no-go log with named approvers, tied to the specific model version and test evidence, provides the accountability and traceability regulators require.

**Why the others are wrong:**
- A press release is a public communication artifact, not a governance record.
- A README describes code usage, not approval accountability.
- A ticket without recorded approvals fails to establish who authorized deployment.

</details>

---

