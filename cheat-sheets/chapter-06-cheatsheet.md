## Chapter 6 Cheat Sheet: AI Workspace, Infrastructure & Data Gathering
**Domain:** Identify Data Needs (26%)

### Compute Provisioning Decision Table
| Workload | Best Compute Choice | Why |
|---|---|---|
| Deep learning (images, NLP, video) | GPU cluster | Parallel matrix ops |
| Classical ML (small/medium tabular) | CPU instance(s) | Sufficient throughput, lower cost |
| Variable/bursty demand | Elastic on-demand cloud compute | Scales down between sprints, avoids idle cost |
| Steady, predictable, high-security workload | Fixed on-prem/dedicated cluster | Predictable cost, full control |

### Secure Dev Environment Checklist
- Isolate sandbox from production systems
- Use de-identified/masked/synthetic data for exploration
- Enforce least-privilege, role-based access
- Log and audit all data access
- Never allow uncontrolled local copies of sensitive data

### Storage Architecture Comparison
| Store | Data Type | Schema | Best For |
|---|---|---|---|
| Data Lake | Structured + unstructured, native format | Schema-on-read | AI/ML training data staging |
| Data Warehouse | Structured only | Schema-on-write | BI reporting, curated analytics |
| Flat file server | Any, unmanaged | None | Small-scale, not exam-recommended at scale |

### Collaboration & Version Control Tooling
| Need | Tool Category | Notes |
|---|---|---|
| Code changes | Git | Standard SCM |
| Large data/model files | DVC / Git LFS | Prevents repo bloat, tracks large binaries |
| Experiment tracking | MLflow (or similar) | Tracks runs, params, metrics |
| Shared exploration | Notebook/workspace platforms | Team collaboration on data prep |

### Data Extraction, Transfer & Refresh
- **ETL**: transform before load — traditional, structured targets
- **ELT**: load raw, transform after — common with modern data lakes
- **Batch refresh**: periodic (nightly/weekly) — for reporting, retraining cycles
- **Streaming refresh**: continuous — required for real-time scoring (fraud, live recs)
- Refresh cadence must match **business latency requirement**, not convenience

### Completeness Validation Techniques
1. Record count reconciliation (source vs. destination)
2. Checksum/hash comparison
3. Field-level null/missing-value rate check against threshold
4. Range/value validation against source system
- Perform validation **before** feature engineering or modeling starts

### Key Stat to Remember
- Industry surveys commonly cite **~80% of data scientist time spent on data preparation**, only ~20% on modeling — the rationale behind this domain's 26% exam weight.

### Exam Traps
- Confusing **completeness** (all data present) with **accuracy/validity** (data is correct) or **security** (data is protected) — these are separate quality dimensions.
- Choosing fixed/on-prem compute for clearly "variable/bursty" workloads (should be elastic).
- Committing large datasets directly into Git instead of using DVC/Git LFS.
