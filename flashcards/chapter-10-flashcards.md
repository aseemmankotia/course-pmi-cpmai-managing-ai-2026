## Chapter 10: Deployment Planning and Execution — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | When should intensive post-deployment monitoring of an AI model begin? | Immediately at go-live, with heightened monitoring during the first 24-48 hours to catch early production failures before broad impact. Exam tip: 'monitor later' answers are always wrong. |
| 2 | When must rollback trigger criteria be documented? | BEFORE deployment begins — never decided ad hoc during an active incident. Exam tip: a missing predefined rollback trigger is a classic deployment-planning gap tested on the exam. |
| 3 | Canary deployment vs. Shadow deployment — key difference? | Canary: new model's outputs ARE used to make real decisions for a subset of live traffic. Shadow: new model runs in parallel, outputs are compared but NEVER used for real decisions. |
| 4 | Blue-green deployment vs. Rolling deployment? | Blue-green: two full parallel environments, instant traffic cutover and instant rollback. Rolling: instances replaced gradually one-by-one — no single instant rollback point. |
| 5 | Big-bang deployment vs. phased/gradual deployment for AI models? | Big-bang: full cutover to all users at once — highest risk, no early validation. Phased (canary/rolling): gradual exposure — lower risk, catches issues before full-scale impact. CPMAI favors phased for production AI. |
| 6 | What must a deployment checklist verify about access BEFORE go-live? | That all required service accounts, API keys, and permissions are PROVISIONED AND TESTED — not merely assumed to exist. |
| 7 | Who owns infrastructure and access-provisioning coordination during AI deployment? | The IT/Operations team, working closely with the AI project team. Exam tip: CPMAI emphasizes cross-team coordination, not a solo data-science responsibility. |
| 8 | What triggers execution of a rollback plan? | Predefined, measurable criteria set BEFORE deployment (e.g., error-rate threshold, prediction-drift threshold) — never ad hoc judgment made during the incident itself. |
| 9 | What are the core categories of a deployment checklist? | Infrastructure readiness; access/permissions; data pipeline connectivity; rollback trigger criteria; monitoring/alerting setup; stakeholder sign-off. |
| 10 | What steps make up post-deployment verification? | Confirm the model receives correct input data, outputs match expected format/range, monitoring dashboards are active, and stakeholders validate initial production results. |
| 11 | What is a 'contingency plan' in AI deployment, distinct from a rollback plan? | A broader plan covering how to handle deployment failure beyond simple reversal — e.g., fallback to a manual process or degraded-mode operation — prepared BEFORE deployment. |
| 12 | Why must production infrastructure capacity/scaling be planned before deployment? | Production AI workloads typically need different compute/scaling profiles than dev/test; underestimating this causes performance issues immediately post-launch — plan capacity ahead of go-live rather than reacting afterward. |
