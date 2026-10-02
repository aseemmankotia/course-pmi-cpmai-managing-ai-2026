# Answer Key — Practice Test 1

**Q1. Correct: D**

A Privacy Impact Assessment (PIA) is the formal, documented process for identifying privacy risks to individuals, evaluating necessity/proportionality of processing, and defining mitigations before data use begins — a core CPMAI responsible AI practice tied to GDPR/CCPA compliance.

---

**Q2. Correct: B**

Bias checks must examine not just direct protected attributes but proxy variables (e.g., zip code, school name) that correlate with them; this is a well-documented cause of disparate outcomes even when protected fields are removed, and CPMAI requires bias analysis across data, model, and algorithm.

---

**Q3. Correct: A**

Per-decision explainability tools (e.g., SHAP/LIME-style feature attribution) directly answer 'why did the model decide this for this individual,' which is the AI/ML transparency requirement CPMAI emphasizes for auditable algorithmic decisions.

---

**Q4. Correct: C**

Role-based access control with least privilege and audit logging enforces data governance for PII, supports secure data handling, and creates the audit trail needed for accountability and regulatory reporting — directly matching CPMAI's privacy and security plan expectations.

---

**Q5. Correct: A**

CPMAI distinguishes chain of custody (an auditable record of data handling, access, and transfer to prove data integrity and provenance) from version control (tracking iterative changes to models, code, and training runs) — both are required for accountability but serve different purposes.

---

**Q6. Correct: A**

CPMAI requires ongoing monitoring of evolving AI regulation and coordination with legal teams so that accountability documentation (disclosures, impact assessments) can be prepared proactively before enforcement, reducing compliance risk.

---

**Q7. Correct: B**

CPMAI's bias-check discipline requires diagnosing the source of disparate impact (data representation, feature proxies, or algorithmic weighting) through formal fairness testing, then applying targeted mitigation before continuing to use the model — this addresses root cause while preserving accountability documentation.

---

**Q8. Correct: C**

Classifying unstructured text into predefined categories based on recognizing patterns in the content (words, phrases, structure) is the core definition of the Recognition Pattern, which covers recognizing patterns in images, sound, and text — including text classification tasks like this one.

---

**Q9. Correct: C**

CPMAI feasibility evaluation requires honestly comparing AI against traditional alternatives; when data volume and quality are insufficient for reliable model training, a traditional rule-based approach paired with a plan to build the labeled dataset over time is the responsible recommendation rather than forcing an AI solution prematurely.

---

**Q10. Correct: C**

CPMAI's Identify phase requires risk assessment across security, safety, AND ethics before proceeding. For an AI system influencing hiring decisions, evaluating bias and disparate impact potential — and documenting mitigations — is essential given the high-stakes, legally sensitive nature of employment decisions.

---

**Q11. Correct: C**

CPMAI teaches that AI project scope statements must include measurable success criteria and performance thresholds while also acknowledging the iterative, experimental nature of model development — unlike traditional software, exact final performance cannot be guaranteed upfront, so assumptions and refinement expectations must be documented.

---

**Q12. Correct: B**

CPMAI emphasizes that AI TCO differs from traditional software TCO because AI models degrade over time (data/concept drift) and require ongoing retraining, monitoring, data labeling, and MLOps support — costs that are frequently underestimated when only one-time development costs are considered.

---

**Q13. Correct: B**

CPMAI identifies change management, user involvement, training, and transparency/explainability as key adoption risk mitigations that must be planned during the Identify phase — technical accuracy alone does not guarantee adoption, and involving end users builds the trust needed for AI recommendations to be accepted and acted upon.

---

**Q14. Correct: D**

Hyperpersonalization ('patterns of patterns') is the pattern used when an AI system layers multiple data patterns about an individual to create a unique, one-to-one experience, which is exactly what individualized recommendation engines do.

---

**Q15. Correct: B**

CPMAI's iterative go/no-go discipline calls for pausing at the feasibility gate when data is insufficient, remediating the data problem, and re-evaluating rather than proceeding blindly or killing the project outright.

---

**Q16. Correct: A**

Resume-screening AI directly affects employment decisions about people, making bias, fairness, and discrimination against protected classes the primary ethical and legal risk that CPMAI's risk assessment across security, safety, and ethics is designed to surface early.

---

**Q17. Correct: D**

Explicit out-of-scope boundaries manage stakeholder expectations up front and give the project team a clear reference point to push back against scope creep as the project evolves.

---

**Q18. Correct: C**

Unlike traditional software, AI models degrade over time due to data and concept drift, requiring ongoing monitoring, retraining, and continued data labeling — costs teams routinely underestimate when they focus only on build-phase expenses.

---

**Q19. Correct: B**

Missing machine learning modeling expertise (as opposed to data engineering expertise) is a personnel/skills gap, which CPMAI's resource identification step requires addressing through hiring, upskilling, or contracting before advancing the project.

---

**Q20. Correct: B**

CPMAI's go/no-go gate discipline requires that when data does not meet the volume, coverage, or quality needed for the solution, the team issue a no-go decision and cycle back to reassess business objectives or find additional/alternate data sources rather than pushing forward on unfit data.

---

**Q21. Correct: A**

CPMAI explicitly calls for identifying data SMEs and data stewards who hold authoritative knowledge of field definitions, schema history, and data lineage within source systems like a CRM — critical input for scoping data requirements accurately.

---

**Q22. Correct: A**

CPMAI's Identify Data Needs domain includes coordinating the AI workspace and infrastructure — provisioning compute (including GPU where needed), secure storage, and collaboration/version-control tooling — before data gathering and preparation begin.

---

**Q23. Correct: D**

CPMAI requires checking privacy, licensing, compliance, and access rights for all data sources — especially third-party data — before use, to ensure the data can be legally and ethically used for the specific AI application intended.

---

**Q24. Correct: D**

Completeness, as a core data quality dimension in CPMAI's data evaluation activities, is measured by the extent to which required fields/records contain valid (non-null/non-missing) values relative to what the solution needs.

---

**Q25. Correct: B**

CPMAI emphasizes conveying data understanding to leadership in business language — framing data quality, gaps, and readiness as risks and opportunities tied to business outcomes so leadership can make informed go/no-go and investment decisions.

---

**Q26. Correct: B**

Data stewards own governance responsibilities such as approving access, defining lineage documentation standards, and enforcing policy over specific data assets — distinct from SMEs who provide business context on data meaning.

---

**Q27. Correct: A**

CPMAI requires checking licensing and usage rights during data identification; a conflict between intended use and license terms must be resolved (renegotiate or exclude) before the data is used further, preventing legal and compliance exposure downstream.

---

**Q28. Correct: C**

CPMAI's Identify Data Needs phase includes coordinating the AI workspace and infrastructure — provisioning appropriate compute (GPU for deep learning workloads) and establishing collaboration/version-control tooling proactively, before development, to avoid delays and rework.

---

**Q29. Correct: A**

CPMAI requires establishing ongoing feeds with defined refresh procedures and completeness validation whenever the use case depends on near-real-time or frequently updated data, ensuring the pipeline reliably delivers usable data at the required cadence.

---

**Q30. Correct: C**

CPMAI mandates checking privacy, licensing, and compliance before data use; when consent or lawful basis for the specific AI use case is undocumented, the team must resolve this through proper consent, legal basis, or de-identification/compliance controls prior to proceeding.

---

**Q31. Correct: C**

CPMAI's data go/no-go decision requires that data gaps materially affecting solution scope be explicitly addressed — either by narrowing the use case, sourcing additional data, or pausing the project (no-go) until the gap is resolved, rather than proceeding on incomplete coverage.

---

**Q32. Correct: B**

The CPMAI data preparation go/no-go gate requires documented evidence that data quality dimensions meet thresholds appropriate to the use case before proceeding to modeling.

---

**Q33. Correct: D**

The operationalization gate requires evidence of robustness and generalization, not just training performance; the large train/test/out-of-time gap indicates overfitting that must be addressed before deployment.

---

**Q34. Correct: B**

With no predefined labels and a goal of discovering natural groupings, unsupervised techniques such as clustering are the appropriate match per CPMAI technique-selection guidance.

---

**Q35. Correct: C**

CPMAI's guidance on managing training emphasizes experiment tracking and data versioning as the mechanism for reproducible comparison across runs.

---

**Q36. Correct: A**

CPMAI explicitly frames complexity-performance-interpretability as a trade-off; in regulated domains, choosing a less interpretable model despite comparable accuracy risks conflicts with explainability and responsible AI obligations.

---

**Q37. Correct: D**

CPMAI's data transformation and preparation guidance stresses reproducibility; unversioned, inconsistent transformation steps break the ability to trace results back to specific data preparation decisions.

---

**Q38. Correct: D**

The operationalization go/no-go gate requires more than matching accuracy targets on the test set. CPMAI methodology explicitly requires verifying performance against success criteria AND robustness/generalization (how the model performs on varied, unseen, real-world data conditions) AND deployment readiness, with documented approval before proceeding. Close test/train accuracy alone does not confirm the model will generalize to production data drift or edge cases.

---

**Q39. Correct: B**

A gradual accuracy decline with no pipeline errors is a classic signature of drift; the correct first step in production governance is to diagnose the type and cause of drift (data drift vs. concept drift) before deciding on remediation such as retraining or rollback.

---

**Q40. Correct: D**

Deployment planning under CPMAI explicitly requires a rollback and contingency procedure with clear triggers (e.g., error rate thresholds) and a validated fallback so the team can quickly revert or mitigate when production issues occur, minimizing business disruption.

---

**Q41. Correct: D**

Model governance in production requires a documented lifecycle management plan that assigns clear ownership (often via a RACI matrix) for retraining approval, drift monitoring, and version control — this is central to the transition from project delivery to sustained operations.

---

**Q42. Correct: D**

Overseeing solution metrics requires dashboards that connect model performance indicators (precision, recall, drift) to business KPIs (churn reduction, revenue impact) so stakeholders can assess ongoing business value, not just technical health.

---

**Q43. Correct: A**

Effective threshold alerting requires a defined, statistically meaningful performance metric and threshold (such as sustained MAPE degradation) tied to an escalation path to the accountable governance owner, enabling timely intervention before business impact grows.

---

**Q44. Correct: A**

Closing the loop requires formal knowledge transfer, a documented final report with lessons learned, and a clear transition plan specifying which roles on the operations side own monitoring, incident response, and retraining going forward — ensuring continuity after the project team disengages.

---

**Q45. Correct: A**

CPMAI requires monitoring dashboards with defined degradation thresholds; when a threshold is breached, the governed response is to confirm against policy, alert stakeholders, and diagnose root cause (data drift, concept drift, or other) before deciding on retraining or other remediation — not to act reflexively or ignore the signal.

---

**Q46. Correct: C**

CPMAI's closing-the-loop phase explicitly requires a final report with lessons learned, formal knowledge-transfer documentation, and a defined transition plan that assigns ongoing operational roles (monitoring, retraining, support, escalation) before the project team disbands, ensuring accountability persists after project closure.

---

