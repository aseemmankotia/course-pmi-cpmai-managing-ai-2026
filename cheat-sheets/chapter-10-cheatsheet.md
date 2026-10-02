# Chapter 10: Deployment Planning and Execution — Cheat Sheet

**Exam Domain:** Operationalize AI Solution (17% of exam)
**Heavily tested:** deployment strategy/rollback planning, cross-team coordination, post-deployment validation

## Deployment Strategy Comparison

| Strategy | Real traffic uses new model? | Rollback speed | Risk level | Best for |
|---|---|---|---|---|
| Big-bang | Yes, 100% at once | Slow/hard | Highest | Rarely recommended for AI |
| Blue-green | Yes, after cutover | Instant (route back) | Low-medium | Fast, safe full cutover |
| Canary | Yes, small % subset | Fast (stop routing) | Low | Validating real-world performance gradually |
| Shadow | NO — outputs only compared | N/A (no live impact) | Very low | Validating model before any live exposure |
| Rolling | Yes, as instances update | Slower (per-instance) | Medium | Infrastructure-level gradual replacement |

**Key exam trap:** Canary vs. Shadow — Canary's outputs affect real decisions; Shadow's outputs never do.

## Deployment Checklist — Core Categories
1. Infrastructure readiness (compute, scaling, network)
2. Access & permissions (service accounts, API keys, security) — provisioned AND tested
3. Data pipeline connectivity (source-to-model data flow verified)
4. Rollback trigger criteria (documented thresholds, defined BEFORE deployment)
5. Monitoring & alerting configured and live
6. Stakeholder sign-off obtained

## Rollback vs. Contingency Plan

| Item | Purpose | Timing decided |
|---|---|---|
| Rollback plan | Revert to last stable state | Trigger criteria set pre-deployment |
| Contingency plan | Broader fallback (manual process, degraded mode) | Prepared pre-deployment |

**Rule:** Rollback/contingency decisions must NEVER be improvised during a live incident — criteria and steps are pre-documented.

## Cross-Team Coordination
- **IT/Operations:** infrastructure, network, security provisioning
- **Data science team:** model artifact readiness, performance baselines
- **Business stakeholders:** sign-off, acceptance criteria
- **Project/PM lead:** coordinates issue escalation and resolution across all groups during go-live

## Post-Deployment Verification Checklist
- [ ] Model receiving correct production data
- [ ] Output format/range matches expectations
- [ ] Monitoring dashboards active and reporting
- [ ] Initial results validated by stakeholders
- [ ] Intensive monitoring window active (first 24-48 hrs post go-live)

## Common Exam Traps
- Choosing "proceed and fix access later" instead of halting for unresolved provisioning gaps
- Confusing canary (live decisions) with shadow (comparison only)
- Treating rollback as an in-the-moment decision instead of a pre-defined, criteria-driven procedure
- Assuming data science team alone owns deployment — IT/Ops and cross-team coordination are required
