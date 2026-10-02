## Chapter 11: Production Governance, Monitoring, and Closing the Loop — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Data drift vs. concept drift — what's the difference? | Data drift = input feature distributions change. Concept drift = the relationship between inputs and target output changes even if inputs look stable. Exam tip: same symptom (falling accuracy) can have two very different causes. |
| 2 | What triggers retraining in a mature governance model — calendar or thresholds? | Threshold-based triggers tied to drift/performance metrics are preferred over fixed calendar schedules. Calendar-only retraining ignores actual model health. |
| 3 | Model versioning vs. change control — key distinction | Versioning = tracking artifacts, parameters, lineage of each model build. Change control = the approval/governance workflow required before promoting a version to production. |
| 4 | Incident response vs. disaster recovery vs. business continuity — order of activation | Incident response (immediate detect/contain/communicate) → Disaster recovery (restore infrastructure/data after major failure) → Business continuity (sustain critical operations during extended disruption). |
| 5 | What should a production AI dashboard always combine? | Business KPIs (e.g., revenue, churn) AND model performance metrics (e.g., accuracy, precision) with defined alert thresholds — technical health alone hides business impact. |
| 6 | Canary/shadow deployment — why used for model rollout? | Runs the new model alongside the current one on live or mirrored traffic to validate performance before full cutover, enabling safe rollback if issues appear. |
| 7 | Degradation analysis stakeholder report — required components | Root cause of degradation, business impact, and a time-bound remediation plan — not metrics alone. |
| 8 | Final project report at closeout — must include | Performance against original objectives, lessons learned, outstanding risks, and knowledge transfer materials (runbooks, model docs) for the operations team. |
| 9 | Transition plan from project team to operations — key artifact | Documented runbooks and monitoring/escalation procedures; informal verbal handoff is insufficient for governance compliance. |
| 10 | Business continuity testing — purpose | Validates that critical AI-dependent business processes can continue operating during a prolonged disruption, distinct from technical DR testing which restores infrastructure. |
| 11 | Escalation path in contingency planning — why formalize it? | Ensures incidents are routed to the right decision-makers within defined time limits, preventing delayed response to model or system failures. |
| 12 | Change control board role in model governance | Reviews and approves proposed model changes (retraining, version upgrade, config change) before production promotion, ensuring accountability and auditability. |
