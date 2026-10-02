# Chapter 3 Cheat Sheet: AI Feasibility, Risk, and Scope

## Feasibility Assessment — 3 Dimensions
| Dimension | Assesses | Key Question | Common Trap |
|---|---|---|---|
| Technical | Compute, infrastructure, integration, skills | Can we build/host/scale this? | Confusing with organizational readiness |
| Data | Availability, quality, access, linkage | Do we have clean, labeled, accessible data? | Assuming more data = automatically feasible |
| Organizational | Culture, change management, buy-in | Will people adopt/trust it? | Treating workforce fear as a technical issue |

**Rule:** All three dimensions must pass. Technical + Data feasible but Organizational infeasible means the project should not proceed without a change-management plan.

## Risk Assessment — 3 Categories
| Category | Focus | Example | Keyword Cue |
|---|---|---|---|
| Security | Unauthorized access, breach, adversarial manipulation | Model inversion attack exposes training data | "breach," "access," "attack" |
| Safety | Physical or systemic harm | Autonomous system misclassifies an obstacle | "harm," "injury," "failure" |
| Ethics | Bias, fairness, transparency | Model rejects one demographic group more often | "disparity," "demographic," "bias" |

## AI vs Non-AI: Honest Comparison Checklist
- Is the logic deterministic/stable? → Favor a rules engine over ML.
- Is the ROI/accuracy gain measurable and does it justify the cost? → If no, don't replace a working traditional system.
- Is there enough quality data to justify ML? → If no, feasibility fails regardless of business desire.
- Novelty is NOT justification. "AI is more modern" is always a wrong-answer distractor.

## AI Project Scope Statement — Required Elements
| Element | Must Include | Wrong-Answer Pattern |
|---|---|---|
| Objective | Business problem + AI approach | Vague mission statements |
| Success Criteria | Measurable metrics (accuracy ≥ X%, cost reduction %) | "Team satisfaction," "stakeholders happy" |
| In-Scope | Specific deliverables/features | Undefined future enhancements |
| Out-of-Scope | Explicit exclusions | "Achieve business goals" (too broad) |
| Assumptions/Constraints | Data, budget, timeline limits | Omitted entirely |

## Exam Notes
- Feasibility ≠ Desirability. A project can be wanted by leadership but still infeasible.
- Scope creep scenarios: any new unlisted requirement mid-project routes through change control, not silent inclusion.
- Ethical risk is the most frequently tested risk category — watch for "disparate impact" and "demographic" language.
- When comparing solutions, the exam rewards the simplest, most explainable, lowest-risk option that still meets requirements — not the most advanced AI technique.

## Memory Tricks
- Feasibility = **TDO**: Technical, Data, Organizational.
- Risk = **SSE**: Security, Safety, Ethics — check all three before recommending a model.
