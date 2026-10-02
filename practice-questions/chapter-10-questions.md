## Chapter 10: Deployment Planning and Execution — Practice Questions

**Q1.** An organization is deploying a new AI fraud-detection model to production and requires minimal downtime with the ability to instantly revert if issues arise. Which deployment strategy BEST meets this requirement?

A) Big-bang deployment to all users at once
B) Manual deployment restricted to a low-traffic maintenance window
C) Deploy to 100% of traffic and monitor logs afterward
D) Blue-green deployment with a parallel standby environment

<details>
<summary>Answer</summary>

**Correct: D**

Blue-green deployment maintains a full parallel production environment, allowing traffic to be cut over instantly and reverted instantly by routing back to the old environment — satisfying both minimal downtime and fast rollback.

**Why the others are wrong:**
- Big-bang deployment maximizes risk exposure and offers no gradual validation or easy rollback path.
- A maintenance window reduces user impact timing but does nothing to enable fast rollback if the model misbehaves.
- Deploying to 100% of traffic without a rollback mechanism violates deployment planning best practice of validating before full exposure.

</details>

---

**Q2.** During final deployment coordination, IT discovers that the required service-account API credentials for the AI model were never provisioned to production. What is the correct action per deployment checklist practice?

A) Halt the deployment until access is provisioned and validated
B) Proceed with deployment and provision the credentials afterward
C) Have a developer temporarily share their personal login credentials
D) Skip the access validation step since it will likely work

<details>
<summary>Answer</summary>

**Correct: A**

Deployment checklists exist specifically to catch gaps like missing access provisioning before go-live; the deployment must be halted and the gap remediated and re-verified before proceeding.

**Why the others are wrong:**
- Proceeding without required access risks deployment failure or partial functionality in production.
- Sharing personal credentials violates security and access-control governance principles tested in this domain.
- Skipping validation defeats the purpose of the checklist and increases production risk.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** Within 24 hours of go-live, a newly deployed AI model's production predictions show significant drift from validation-phase results. According to a well-formed contingency plan, what should happen?

A) Wait a week to see if the drift stabilizes on its own
B) Immediately retrain the model directly in the production environment
C) Ignore the drift since some variance is always expected
D) Execute the predefined rollback based on documented trigger criteria

<details>
<summary>Answer</summary>

**Correct: D**

A contingency/rollback plan must define measurable trigger criteria in advance; when those thresholds are met, the predefined rollback procedure is executed rather than made up on the spot.

**Why the others are wrong:**
- Waiting without acting risks compounding harm from a model producing degraded results in production.
- Retraining directly in production without validation bypasses the model lifecycle and introduces additional uncontrolled risk.
- Dismissing significant drift ignores the entire purpose of post-deployment monitoring and validation.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** Which deployment approach routes a small percentage of REAL live traffic to a new AI model while the majority of users continue using the existing model, in order to validate real-world performance before full rollout?

A) Canary deployment
B) Blue-green deployment
C) Shadow deployment
D) Rolling deployment

<details>
<summary>Answer</summary>

**Correct: A**

Canary deployment exposes a limited subset of real user traffic to the new model's live decisions, allowing risk-limited validation before scaling to 100%.

**Why the others are wrong:**
- Blue-green performs a full environment cutover rather than a gradual traffic subset.
- Shadow deployment runs the new model in parallel but its outputs are NOT used for real decisions — the key distinguishing exam trap.
- Rolling deployment gradually replaces infrastructure instances, not a percentage-based live traffic split for validation.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which deployment approach runs the new AI model on live production data in parallel with the existing model, comparing outputs, WITHOUT using the new model's outputs to make actual decisions?

A) Canary deployment
B) Shadow deployment
C) A/B testing
D) Rolling deployment

<details>
<summary>Answer</summary>

**Correct: B**

Shadow deployment is specifically defined by comparing model outputs against production data without those outputs affecting live decisions — this is the exact distinction the exam tests against canary.

**Why the others are wrong:**
- Canary deployment DOES use the new model's outputs to make real decisions for a subset of users.
- A/B testing compares two live decision-making variants, both of which affect real outcomes.
- Rolling deployment is an infrastructure replacement pattern, not an output-comparison validation technique.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A deployment checklist for an AI solution should explicitly verify which of the following BEFORE go-live?

A) Only the final accuracy metric reported during model evaluation
B) The marketing plan for promoting the AI-enabled product
C) The long-term retraining schedule for the data science team
D) Model access permissions, data pipeline connectivity, rollback trigger criteria, and monitoring readiness

<details>
<summary>Answer</summary>

**Correct: D**

A production readiness checklist must confirm operational and technical readiness across access, data flow, rollback definitions, and monitoring — not just model quality metrics.

**Why the others are wrong:**
- Accuracy metrics belong to the model evaluation phase and don't confirm operational deployment readiness.
- Marketing plans are business activities unrelated to technical deployment validation.
- Retraining schedules are a post-deployment lifecycle concern, not a pre-deployment checklist item.

</details>

---

**Q7.** Which cross-functional role is PRIMARILY responsible for coordinating infrastructure readiness, network access, and security provisioning during AI solution deployment?

A) Data scientist
B) Business stakeholder
C) End user
D) IT/Operations team

<details>
<summary>Answer</summary>

**Correct: D**

IT/Operations owns infrastructure provisioning, network configuration, and security access controls, working in coordination with the AI project team during deployment.

**Why the others are wrong:**
- Data scientists focus on model development and validation, not infrastructure/security provisioning.
- Business stakeholders define requirements and priorities but do not execute technical provisioning.
- End users consume the deployed solution but have no provisioning responsibility.

</details>

---

**Q8.** What is the primary purpose of a rollback plan in AI solution deployment?

A) To document lessons learned after project closure
B) To eliminate the need for testing before deployment
C) To schedule the model's future retraining cadence
D) To define predefined criteria and steps to revert to a previous stable state if deployment issues occur

<details>
<summary>Answer</summary>

**Correct: D**

A rollback plan exists to specify measurable trigger conditions and concrete reversal steps agreed upon BEFORE deployment, minimizing decision-making risk during an active incident.

**Why the others are wrong:**
- Lessons learned documentation is a project closure activity, not a deployment contingency mechanism.
- Rollback plans supplement, not replace, pre-deployment testing.
- Retraining cadence is a model maintenance concern separate from deployment reversal procedures.

</details>

---

