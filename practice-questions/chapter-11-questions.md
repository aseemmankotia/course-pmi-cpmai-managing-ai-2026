## Chapter 11: Production Governance, Monitoring, and Closing the Loop — Practice Questions

**Q1.** A deployed credit-risk model's precision has dropped 12 points over two months, but the input feature distributions remain statistically unchanged compared to training data. Which condition BEST explains this?

A) Data drift — the incoming feature values have shifted
B) Concept drift — the relationship between features and the target outcome has changed
C) Training-serving skew from a bug in the feature pipeline
D) Model overfitting that was never caught in validation

<details>
<summary>Answer</summary>

**Correct: B**

When feature distributions are stable but the underlying relationship between inputs and the label changes (e.g., customer behavior shifts), that is concept drift, not data drift.

**Why the others are wrong:**
- Data drift specifically refers to a shift in input feature distributions, which the scenario says did NOT happen.
- Training-serving skew would typically show up immediately after deployment, not as a gradual two-month decline, and would usually also affect feature distributions.
- Overfitting would show as poor performance from the start, not a decline after two stable months in production.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A project team wants to define when a production model should be retrained. Which governance approach BEST balances cost and responsiveness for a model operating in a rapidly changing market?

A) Retrain on a fixed calendar schedule regardless of performance
B) Retrain only when a stakeholder formally requests it
C) Retrain based on drift and performance-metric thresholds crossing a defined tolerance
D) Never retrain; redeploy the original model if issues arise

<details>
<summary>Answer</summary>

**Correct: C**

Threshold-triggered retraining tied to monitored drift and performance metrics ensures the model is refreshed when it actually needs it, avoiding both unnecessary cost and stale-model risk in volatile environments.

**Why the others are wrong:**
- A fixed calendar schedule ignores actual model health and can retrain too early or too late in a fast-changing environment.
- Waiting for informal stakeholder requests lacks governance rigor and delays detection of degradation.
- Never retraining guarantees the model will eventually fail to meet business needs as the environment changes.

</details>

---

**Q3.** A CPMAI practitioner is designing a production monitoring dashboard for a churn-prediction model. Which combination of elements should the dashboard include to satisfy governance requirements?

A) Only technical model metrics such as AUC and F1 score
B) Only business KPIs such as churn rate and revenue impact
C) Both business KPIs and model performance metrics with defined alert thresholds
D) A single composite score combining all metrics into one number

<details>
<summary>Answer</summary>

**Correct: C**

Effective governance dashboards must connect technical model health to business outcomes and include threshold-based alerting so degradation is caught before it harms the business.

**Why the others are wrong:**
- Technical metrics alone don't show stakeholders the business impact of model degradation.
- Business KPIs alone can mask a technically failing model whose downstream effects haven't yet surfaced.
- A single composite score obscures root cause and makes degradation analysis and alerting less actionable.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** During degradation analysis, the team finds that a recommendation model's click-through rate has fallen sharply after a marketing campaign changed customer segments. What should the team report to stakeholders?

A) The root cause (segment shift), business impact, and a remediation plan with timeline
B) Only the current performance metrics, without further explanation
C) A recommendation to immediately decommission the model
D) A request for more budget without diagnostic detail

<details>
<summary>Answer</summary>

**Correct: A**

Stakeholder reporting during degradation must connect the diagnosed root cause to business impact and present a concrete, time-bound remediation plan to maintain trust and enable decision-making.

**Why the others are wrong:**
- Metrics alone without root cause leave stakeholders unable to make informed decisions.
- Decommissioning is premature before root cause and remediation options are evaluated.
- Requesting budget without diagnostics fails governance transparency requirements.

</details>

---

**Q5.** Which statement BEST distinguishes model versioning from change control in production AI governance?

A) Versioning tracks distinct model artifacts and their lineage; change control governs the approval process for promoting a new version to production
B) Versioning and change control are the same process with different names
C) Versioning applies only to code, while change control applies only to data
D) Change control is only needed during initial deployment, not afterward

<details>
<summary>Answer</summary>

**Correct: A**

Versioning is the technical practice of tracking model artifacts, parameters, and lineage; change control is the governance process (review, approval, sign-off) required before a new version replaces the current production model.

**Why the others are wrong:**
- They serve related but distinct purposes — one is technical tracking, the other is a governance/approval workflow.
- Both versioning and change control apply to models, data, and code collectively, not split along that line.
- Change control is an ongoing requirement throughout the model's operational lifecycle, especially for retraining and rollback decisions.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A production AI system used for medical triage suddenly starts returning erroneous outputs due to an upstream data feed outage. Which plan should be activated FIRST?

A) The business continuity plan to relocate operations to another facility
B) The disaster recovery plan to restore infrastructure from backups
C) The incident response plan to detect, contain, and communicate the issue immediately
D) The retraining schedule to build a new model version

<details>
<summary>Answer</summary>

**Correct: C**

Incident response is the immediate, first-line process for detecting, containing, and communicating an active operational issue; DR and BCP are invoked only if the incident escalates to infrastructure loss or extended outage.

**Why the others are wrong:**
- Business continuity plans address sustaining critical operations during extended disruptions, not the initial response to a single incident.
- Disaster recovery addresses restoring IT infrastructure after major failure, which is not yet established here.
- Retraining addresses model quality issues over time, not an active data-feed outage requiring immediate containment.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A team is deciding how to roll out a newly retrained fraud-detection model with minimal business risk. Which deployment approach BEST supports safe governance and rollback capability?

A) Full replacement of the production model with no parallel run
B) Deploying directly to all users based solely on offline test accuracy
C) Skipping monitoring since the model passed validation testing
D) Canary or shadow deployment that compares new model outputs against the current model before full cutover

<details>
<summary>Answer</summary>

**Correct: D**

Canary or shadow deployment allows the new model to be evaluated against live traffic or run in parallel with the current model, enabling safe validation and quick rollback if issues arise — a core governance practice for production changes.

**Why the others are wrong:**
- Full replacement without a parallel run removes the ability to detect problems before they affect all users.
- Offline validation accuracy does not guarantee real-world performance under production conditions.
- Skipping monitoring violates governance requirements regardless of validation results.

</details>

---

**Q8.** As a CPMAI project nears closeout, which activity is MOST critical to ensure a smooth transition from the project team to operational support staff?

A) Delivering a final report, lessons learned, and runbooks as part of formal knowledge transfer
B) Deleting project documentation to reduce storage costs
C) Disbanding the team immediately after go-live with no handoff meeting
D) Relying on informal verbal explanations only

<details>
<summary>Answer</summary>

**Correct: A**

A structured transition requires a final report, documented lessons learned, and operational runbooks so support staff can maintain, monitor, and troubleshoot the solution without the original project team.

**Why the others are wrong:**
- Deleting documentation destroys the knowledge base needed for ongoing operations and governance audits.
- Disbanding without handoff creates operational risk and loss of institutional knowledge.
- Verbal-only explanations are not repeatable, auditable, or sufficient for governance compliance.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

