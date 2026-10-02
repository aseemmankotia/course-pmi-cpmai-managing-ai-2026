# Answer Key — Practice Test 2

**Q1. Correct: B**

Privacy by design requires assessing privacy risk from the earliest business understanding phase, and because AI projects are iterative, the PIA must be revisited whenever data sources, features, or use cases change throughout the lifecycle.

---

**Q2. Correct: D**

Equalized odds directly targets parity in true positive and false positive rates between groups, which is exactly the disparity described in the scenario.

---

**Q3. Correct: A**

RBAC with permissions scoped to each role's actual needs, plus audit logging, directly implements least privilege and supports accountability across the AI lifecycle.

---

**Q4. Correct: C**

Local interpretability methods like LIME and SHAP are designed specifically to explain individual predictions by attributing influence to specific input features, matching the per-decision explanation requirement.

---

**Q5. Correct: A**

GDPR Article 22 specifically addresses automated decision-making with legal or similarly significant effects, granting data subjects the right to obtain human intervention, express their view, and receive an explanation of the decision.

---

**Q6. Correct: B**

A version-controlled, traceable record of every transformation with rationale and ownership preserves chain of custody and data lineage, which is essential for reproducibility, audits, and accountability at the go/no-go gate.

---

**Q7. Correct: D**

CPMAI treats fairness and bias validation as an ongoing accountability obligation, not a one-time checkpoint. New evidence of bias in production requires re-invoking the go/no-go discipline: documenting the trigger, involving legal/compliance alongside technical teams, and recording the rationale for whatever action is taken, preserving the audit trail and chain of custody for the decision.

---

**Q8. Correct: C**

The need is to detect deviation from a known individual baseline (anomaly detection against an established pattern), which is precisely what the Patterns and Anomalies pattern addresses.

---

**Q9. Correct: B**

CPMAI feasibility evaluation requires honestly comparing AI against traditional alternatives; low volume, deterministic and stable rules with no ambiguity mean a rule-based/RPA solution is cheaper, more explainable, and equally effective.

---

**Q10. Correct: D**

CPMAI's risk assessment separates security, safety, and ethics; the dominant risk for resume screening is biased or discriminatory decision-making learned from historical hiring data, which is fundamentally an ethics concern with legal and reputational consequences.

---

**Q11. Correct: A**

CPMAI treats the scope statement as a control document; a new capability that introduces a new feasibility constraint (a missing prerequisite pipeline) requires formal change control and re-evaluation against go/no-go criteria, not silent absorption or blind execution.

---

**Q12. Correct: C**

Hyperpersonalization Patterns tailor experiences, content, and offers to a specific individual using their unique behavioral data, which is distinct from segment-based predictive modeling.

---

**Q13. Correct: C**

Unlike traditional software, AI models degrade over time due to data and concept drift and require continuous labeling, monitoring, and retraining; these recurring operational costs are the most commonly underestimated in TCO because teams tend to focus only on one-time build costs.

---

**Q14. Correct: B**

Classifying unstructured text into predefined categories is a pattern-recognition task — identifying patterns in data (here, textual patterns tied to topic labels) — which is the core definition of the Recognition Pattern in the Seven Patterns of AI.

---

**Q15. Correct: B**

Feasibility assessment evaluates data availability separately from compute — even with unlimited compute, 50 labeled examples of a rare defect are insufficient to train a reliable classifier. Data availability (quantity and quality of representative labeled examples) is the binding constraint here.

---

**Q16. Correct: B**

CPMAI risk assessment explicitly separates security, safety, and ethics as distinct risk categories. Differential error rates across demographic groups causing disparate treatment is a textbook ethical/fairness (bias) risk, even though it manifests as an operational access issue.

---

**Q17. Correct: B**

Out-of-scope boundaries explicitly call out capabilities or integrations deliberately excluded from the current phase so stakeholders don't assume they're included. Deferring ERP work-order integration to a future phase is a textbook out-of-scope statement.

---

**Q18. Correct: C**

CPMAI TCO methodology requires including the full lifecycle cost of AI, not just initial development — ongoing data labeling, retraining due to drift, and monitoring infrastructure are recurring costs unique to AI (compared to traditional software) that must be estimated in the business case.

---

**Q19. Correct: A**

CPMAI emphasizes that adoption and integration risk — including change management, user trust, and training — is a distinct and frequent cause of AI project failure even when technical model performance is strong. Underwriters ignoring a technically sound model points to a people/process adoption gap, not a technical defect.

---

**Q20. Correct: C**

CPMAI explicitly builds in a go/no-go decision point after data evaluation. When core predictive features are severely incomplete and the target class is critically underrepresented, the responsible action is to formally flag this to stakeholders and pursue additional data sourcing or scope renegotiation rather than silently absorbing the risk downstream — this is the defining discipline that separates AI projects from traditional software projects.

---

**Q21. Correct: A**

Identify Data Needs explicitly includes mapping data sources along with their ownership, access permissions, licensing, and compliance requirements. The correct practice is to surface and resolve these gating dependencies early and set realistic commitments based on confirmed access, rather than assuming approvals or skipping governance.

---

**Q22. Correct: B**

The Data Steward owns data quality standards, governance policy enforcement, and stewardship of data assets, and is the role CPMAI identifies as a required stakeholder to engage when identifying data needs and evaluating whether data meets governance and quality standards.

---

**Q23. Correct: C**

Coordinating the AI workspace and infrastructure is an explicit Identify Data Needs activity. High-velocity, high-volume streaming data requires elastic ingestion and storage provisioned for sustained throughput and burst capacity, identified up front so Data Preparation and later phases are not blocked by infrastructure limits.

---

**Q24. Correct: A**

Defining sampling requirements is an explicit Identify Data Needs activity. For extremely rare-event targets, requirements must call for stratified sampling that deliberately oversamples the minority class so downstream training and evaluation sets contain enough positive examples to build and validate a usable model.

---

**Q25. Correct: A**

CPMAI's core axiom is that AI projects are data projects — feasibility hinges on whether sufficient, quality, representative data actually exists to support the intended outcome. This is unlike traditional software, where once requirements are defined, functionality can generally be engineered regardless of data availability. The go/no-go decision exists specifically to test this data-dependent feasibility before committing further investment.

---

**Q26. Correct: C**

CPMAI explicitly calls for identifying and working through data stewards and governance teams as the authorities over data access, quality, and compliance; bypassing their process introduces legal and quality risk that undermines the data understanding phase.

---

**Q27. Correct: D**

CPMAI requires checking licensing, contractual, and compliance restrictions on data as part of identifying data needs; a usage restriction that legally prohibits repurposing the data for churn modeling is a blocking governance issue that must be resolved before proceeding, unlike quality or technical mismatches which are addressed in data understanding/preparation.

---

**Q28. Correct: B**

Identify Data Needs includes coordinating the AI workspace and infrastructure — provisioning storage, compute, and secure environments sized for the data being gathered — which must happen before data is even collected, distinct from model-development activities like architecture selection, tuning, or metric definition.

---

**Q29. Correct: C**

Completeness validation in the data gathering activity means confirming that what was extracted matches what landed at the destination — record counts, checksums, or row-level reconciliation are the standard techniques CPMAI expects for verifying transfer completeness, especially for recurring batch feeds.

---

**Q30. Correct: A**

CPMAI's data privacy, licensing, and compliance checks require that data use agreements be honored based on their stated purpose; a mismatch between the agreement's permitted use and the project's commercial intent is exactly the kind of blocking issue that must trigger the go/no-go decision and legal escalation, not a workaround.

---

**Q31. Correct: D**

CPMAI emphasizes translating technical data findings into business language for leadership — describing risk in terms of business impact, proposed mitigations, and a clear recommendation — rather than exposing raw technical artifacts or omitting relevant findings.

---

**Q32. Correct: A**

Non-random (MNAR) missingness correlated with a segment risks introducing systematic bias into the model. The gate discipline requires the root cause be investigated and remediated, not merely accepted or deferred, before advancing past the data quality go/no-go checkpoint.

---

**Q33. Correct: C**

The operationalization gate explicitly requires evaluating performance against success criteria AND robustness/generalization AND deployment readiness with documented approval. A large performance drop on edge cases and seasonal variation fails the robustness criterion, so the gate should not pass regardless of the headline test-set number.

---

**Q34. Correct: D**

Sequential decision-making with delayed, cumulative feedback and no ground-truth labels is the defining characteristic of a reinforcement learning problem, where an agent learns a policy via trial-and-error interaction with an environment.

---

**Q35. Correct: D**

Experiment tracking and data/model versioning that captures data snapshots, code versions, hyperparameters, and metrics for every run is the core practice for managing training reproducibility and enabling apples-to-apples comparison across experiments.

---

**Q36. Correct: D**

Using the test set for tuning decisions is a form of data leakage that invalidates the final performance metric as an unbiased estimate of real-world performance. Correct remediation is a proper train/validation/test split, where the test set is untouched until final evaluation, followed by re-evaluation.

---

**Q37. Correct: D**

CPMAI's complexity-performance-interpretability trade-off principle requires evaluating technique selection against the specific use case and regulatory context, not accuracy alone. When explainability is a hard regulatory requirement and the accuracy gap is modest, the more interpretable model is generally the appropriate choice.

---

**Q38. Correct: B**

The operationalization go/no-go gate requires verifying performance against documented success criteria AND robustness/generalization, not just training performance. A large train-test gap plus high cross-validation variance is a textbook overfitting signature meaning the model has memorized training data rather than learned generalizable patterns. CPMAI methodology requires the project manager to deny the gate until generalization and stability are demonstrated on unseen data, with documented justification for the decision.

---

**Q39. Correct: B**

When input feature distributions are stable but the underlying relationship between inputs and the target outcome has changed, this is concept drift, not data drift. The correct governance response is retraining with fresh, representative labeled data capturing the new pattern.

---

**Q40. Correct: D**

Shadow deployment runs the new model alongside the incumbent system on real production inputs, generating predictions for comparison without those predictions ever driving actual customer-facing decisions, eliminating customer risk entirely.

---

**Q41. Correct: A**

Threshold-based alerting tied to monitored performance metrics is the correct configuration for triggering unscheduled, event-driven retraining, ensuring the model is refreshed as soon as measurable degradation is detected rather than waiting on a fixed calendar.

---

**Q42. Correct: C**

Contingency plans for AI incidents should define an immediate mitigation step—typically rollback to a known-stable version—to halt business harm first, before root-cause analysis, retraining, or reporting activities proceed.

---

**Q43. Correct: A**

The delay resulted from ambiguity about who was responsible for acting on the alert, not a lack of detection. This is a classic gap in the transition plan's role definitions (RACI), which CPMAI stresses must be explicit when handing off from project team to operational support.

---

**Q44. Correct: A**

A successful DR test validates that predefined failover mechanisms (backup rules engine, cached results, redundant endpoints, etc.) activate and restore business continuity within the recovery time objective, which is the actual purpose of regular contingency plan testing.

---

**Q45. Correct: D**

CPMAI treats detected covariate/data drift as an early warning signal even when performance metrics haven't degraded. The correct governance response is heightened monitoring and reassessing the retraining cadence, escalating action only if performance actually declines.

---

**Q46. Correct: B**

CPMAI requires a formal, documented transition plan with clearly assigned operational roles, structured knowledge transfer, and defined contingency/incident-response procedures that are tested on a recurring basis — not an informal or purely technical handoff.

---

