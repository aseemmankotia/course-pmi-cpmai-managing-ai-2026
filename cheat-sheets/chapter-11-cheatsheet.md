## Chapter 11 Cheat Sheet — Production Governance, Monitoring, Closing the Loop

### Drift Types
| Type | What Changes | Symptom |
|---|---|---|
| Data drift | Input feature distribution | Inputs look different from training data |
| Concept drift | Relationship between features and target | Inputs look normal, but predictions become wrong |
| Training-serving skew | Pipeline inconsistency between train and prod | Sudden performance drop right after deployment |

### Retraining Governance
- Prefer **threshold/drift-triggered** retraining over fixed calendar cycles for volatile domains.
- Every retraining event must pass through **change control** (review + approval) before promotion.
- Maintain **version lineage**: data version, code version, model artifact, hyperparameters.

### Dashboard Design
- Combine **business KPIs** (revenue, churn, fraud losses) + **model metrics** (precision, recall, latency).
- Set explicit **alert thresholds** — don't rely on manual review.
- Avoid collapsing everything into a single composite score — obscures root cause.

### Degradation Analysis & Reporting
Report to stakeholders must include:
1. Root cause (drift type, pipeline issue, external factor)
2. Business impact (quantified)
3. Remediation plan with timeline
Do NOT report raw metrics alone or jump straight to "decommission."

### Deployment Safety Patterns
| Pattern | Use Case |
|---|---|
| Shadow deployment | Compare new model output vs. current, no user impact |
| Canary rollout | Gradual traffic shift to new model with rollback ready |
| Full replacement | Higher risk — avoid without parallel validation |

### Contingency Planning — Order of Activation
1. **Incident Response** — immediate detect, contain, communicate.
2. **Disaster Recovery** — restore infrastructure/data after major failure.
3. **Business Continuity** — sustain critical operations during extended disruption; validated via periodic BC testing.
Escalation paths must be pre-defined with clear ownership and time limits.

### Closing the Loop — Transition Checklist
- Final report: objectives vs. actual outcomes, lessons learned, open risks.
- Knowledge transfer: runbooks, model documentation, monitoring/alerting guides.
- Formal handoff meeting — never rely on verbal-only transfer.
- Ops team confirms ownership of monitoring, retraining governance, and incident response before project team disbands.

### Common Exam Traps
- Confusing data drift with concept drift when symptoms look identical.
- Choosing calendar-based retraining as the 'best practice' default (threshold-based is preferred).
- Treating incident response and disaster recovery as interchangeable.
- Skipping stakeholder root-cause reporting in favor of raw metrics.
- Assuming project closeout ends with go-live rather than full knowledge transfer.
