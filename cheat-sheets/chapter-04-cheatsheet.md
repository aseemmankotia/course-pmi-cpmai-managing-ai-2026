## Chapter 4 Cheat Sheet — Business Case, ROI/TCO, Architecture, Resourcing
**Domain:** Identify Business Needs and Solutions (26%)

### ROI Formula
| Formula | Notes |
|---|---|
| ROI = (Net Benefit − Cost) / Cost | Benefit MUST tie to a measurable business KPI, not just model accuracy |

### TCO Components Checklist
| Category | Includes | Exam Trap |
|---|---|---|
| Compute/Infrastructure | Training + inference compute, cloud/on-prem hosting | Often the only cost estimated upfront |
| Labor | Data scientists, data engineers, ML/DevOps engineers, business analysts | Non-modeling roles frequently omitted |
| Data Acquisition | Sourcing, licensing, labeling/annotation | Ongoing labeling for retraining often forgotten |
| Maintenance | Monitoring, drift detection, retraining, model updates | **#1 most commonly omitted TCO category — heavily tested** |

### Build vs. Buy Comparison Rule
Compare ALL TCO categories (compute, labor, data, integration, maintenance) over the **same time horizon** for both options — never compare only upfront cost.

### KPI Design Rule
Every technical metric (accuracy, F1, latency) must map to a **business outcome metric** (cost reduction %, revenue lift, cycle-time reduction). A model can hit its technical target and still fail the business case if this link is missing.

### Change Management — ADKAR Model
| Stage | Meaning | Signal of Failure |
|---|---|---|
| Awareness | Understand why change is happening | "Why are we doing this?" |
| Desire | Personal motivation to support it | "I get it, but I don't want it" (fear of job loss) |
| Knowledge | Know how to use the new tool | "I don't know how to operate this" |
| Ability | Can actually perform with new tool | Struggles despite training |
| Reinforcement | Sustained adoption over time | Reverts to old process after go-live |

### High-Level AI Architecture — Required Blocks
Data Sources → Ingestion → Storage/Prep → Model Training → Model Serving/API → Application → **Monitoring & Feedback Loop** (drift detection, retraining trigger)
> Missing the feedback loop is the #1 flagged gap in architecture review questions.

### Resource/Skill Gap Categories (assess all 3)
1. **Team/Skills** — data engineer vs. data scientist vs. ML/DevOps engineer roles
2. **Hardware/Infrastructure** — GPU capacity, storage, environment readiness
3. **Contractors/Vendors** — labeling vendors, specialized consultants for short-term gaps

### Quick Role Comparison
| Role | Owns |
|---|---|
| Data Engineer | Pipelines, data infrastructure |
| Data Scientist | Model building, evaluation |
| ML/DevOps Engineer | Deployment, monitoring, retraining automation |
| Business Analyst | KPI definition, adoption, change management support |
