# Chapter 7 Cheat Sheet: Data Evaluation, Compliance & Go/No-Go

## Domain
Identify Data Needs — 26% of exam weight. Heavily tested: quality dimensions, EDA, go/no-go gate, privacy/licensing checks.

## Data Quality Dimensions ("ACCT")
| Dimension | Definition | Exam Trap |
|---|---|---|
| Accuracy | Value matches real-world truth | Unnatural clustering/rounding = accuracy issue, not consistency |
| Completeness | No missing values/fields | Missing ≠ wrong value; it's absence |
| Consistency | Same entity represented uniformly across records/sources | Renamed codes for same entity = consistency issue |
| Timeliness | Data is current/available when needed | Complete but stale data still fails timeliness |

## Compliance Pre-Check (Before Any Data Use)
| Check | What to Verify |
|---|---|
| Privacy | Consent obtained? PII handled per GDPR/CCPA/HIPAA? |
| Licensing | Terms of Service allow AI/ML training use? Copyright cleared? |
| Regulatory | Sector-specific rules (finance, healthcare) satisfied? |

**Rule:** Public availability ≠ legal permission. Always verify ToS and consent even for scraped/open data.

## EDA Technique Order
1. Profile — summary stats (mean, median, std dev, min/max)
2. Visualize — histograms, box plots, scatter plots, missing-value heatmaps
3. Distribution analysis — check for skew, outliers, unnatural clustering
4. Bias/gap analysis — compare subgroup distributions and outcomes for disparity
5. Document findings before proceeding to Data Preparation

## Go/No-Go Decision Framework
| Signal | Decision |
|---|---|
| Data quality strong, compliant, low bias | **Go** — proceed to Data Preparation |
| Minor gaps, fixable quality issues | **Conditional Go** — remediate first (impute, re-source subset) |
| Major bias, stale data, undocumented consent, missing licensing | **No-Go** — halt, redefine scope, or find alternate source |

**Exam trap:** "No-Go" rarely means permanently cancel the project — it usually means pause/redefine/re-source.

## Communicating to Leadership
- Translate technical findings → business risk/cost language
- Example: "40% missing data limits accurate prediction for 1/3 of customers" (NOT p-values/correlation matrices)
- Always tie data issues to project risk, timeline, and cost impact
- Never withhold known data issues to speed approval

## Quick Memory Tricks
- **ACCT** = Accuracy, Completeness, Consistency, Timeliness
- **Bias check** = compare subgroups, not overall averages
- **Go/No-Go** = gate at end of Data Understanding phase, before Data Preparation
- **Public ≠ Permitted** = compliance check is mandatory regardless of data visibility
