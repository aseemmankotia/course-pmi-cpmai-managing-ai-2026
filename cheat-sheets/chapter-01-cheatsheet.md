# Responsible AI Foundations Cheat Sheet

## Privacy Compliance Numbers
| Regulation | Key Trigger/Limit |
|---|---|
| GDPR DPIA | Required for high-risk processing (automated decisions w/ legal effect, large-scale sensitive data) |
| GDPR max fine | €20M or 4% global turnover, whichever is HIGHER |
| CCPA disclosure window | 12 months look-back on consumer request |
| Four-fifths rule | Selection rate ratio < 0.8 = potential disparate impact |

## Bias Mitigation Stage Map
| Stage | When Applied | Example Techniques |
|---|---|---|
| Pre-processing | Before training | Reweighting, resampling, data augmentation |
| In-processing | During training | Fairness constraints, adversarial debiasing |
| Post-processing | After training | Threshold adjustment, equalized-odds calibration |

## Fairness Metrics
| Metric | Definition |
|---|---|
| Demographic parity | Equal positive prediction rate across groups |
| Equalized odds | Equal TPR & FPR across groups (outcome-aware) |
| Disparate impact ratio | Min group rate ÷ max group rate; flag if < 0.8 |

## Explainability Tools
| Tool | Scope | Best For |
|---|---|---|
| SHAP | Local + global | Consistent, theoretically grounded attributions |
| LIME | Local only | Fast, simple surrogate explanation of one prediction |
| Global feature importance | Global | Explaining overall model drivers |

## Governance Artifacts
| Artifact | Purpose |
|---|---|
| DPIA/PIA | Legal privacy risk assessment before high-risk processing |
| Model card | Documents intended use, subgroup performance, limitations |
| Go/no-go log | Records sign-off from risk/legal/technical leads before deployment |
| Chain-of-custody record | Tracks access/modification history with timestamps & approvals |
| Data/model version control | Enables reproducibility for audits |

## Access Control Rules
- Apply **RBAC + least privilege** to all PII training data.
- Log **every access** to PII fields individually (never shared credentials).
- Encrypt **at rest AND in transit** — encryption alone ≠ accountability; logging is separate.

## Exam Traps
- Choosing overall accuracy instead of subgroup metrics for bias detection.
- Confusing interpretability (model's inherent structure) with explainability (post-hoc technique).
- Assuming vendor certification replaces internal fairness testing/documentation.
- Missing that DPIA is required BEFORE deployment, not after.
- Forgetting version/lineage tracking is required for regulator reproducibility requests.
