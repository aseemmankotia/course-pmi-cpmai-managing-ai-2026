# Practice Test 2: PMI-CPMAI Certification Exam Prep Masterclass

- **Questions:** 46
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-2.md`. Track results in `score-tracker.md`.

---

**Q1.** A healthcare organization is planning to deploy an AI system that analyzes patient imaging data to predict disease risk. The system will process large volumes of PII and protected health information. According to responsible AI practices, at which point in the AI project lifecycle should the Privacy Impact Assessment (PIA) be conducted?

A) After the model is deployed to production, to assess real-world privacy impacts
B) Starting in the business understanding phase and continuously as data sources and use cases evolve
C) During the data preparation phase, before the model development phase, to identify and mitigate privacy risks early
D) Only when a regulator specifically requests documentation of privacy safeguards

---

**Q2.** A financial institution builds an AI model to predict loan default risk. During bias testing, the team finds that overall accuracy is nearly identical across two demographic groups, but the false negative rate (approving loans that later default) is significantly higher for Group A, while the false positive rate (denying loans that would not have defaulted) is significantly higher for Group B. Which fairness metric should the team prioritize to address this specific disparity?

A) Demographic parity (equal proportion of positive outcomes across groups)
B) Overall accuracy equality across groups
C) Individual fairness (similar individuals receive similar predictions)
D) Equalized odds (equal true positive and false positive rates across groups)

---

**Q3.** An AI project team is designing access controls for a shared training data repository containing sensitive customer records. Data scientists need to query and transform data, data engineers need to modify pipeline configurations, business analysts need only aggregate reports, and external auditors need read-only access to audit logs but not raw data. Which access control configuration BEST supports least privilege while enabling project execution?

A) Implement role-based access control (RBAC) with granular permissions scoped to each role's specific data needs, combined with audit logging of all access events
B) Grant all internal team members administrator-level access to avoid project delays, and restrict only external auditors
C) Provide all users the same read/write access to the raw data repository and rely on data masking to prevent misuse
D) Encrypt the entire repository and treat encryption as sufficient to satisfy access control and privacy requirements

---

**Q4.** A team must choose an interpretability approach for a complex deep learning fraud-detection model. Regulators require an explanation for each individual denied transaction, identifying which specific features drove that particular decision, without requiring a full explanation of the model's overall internal logic. Which type of interpretability method BEST satisfies this requirement?

A) Global interpretability methods that summarize overall feature importance across the entire model
B) Reducing model complexity by switching to a simpler algorithm regardless of performance impact
C) Local interpretability methods (e.g., LIME, SHAP) that explain individual predictions
D) Post-hoc aggregate reporting of overall model accuracy metrics

---

**Q5.** A multinational company deploys an AI-based credit scoring system used by customers in both the European Union and California. A rejected EU applicant requests details on how the automated decision was made and asks for human review of the decision. Which regulatory requirement specifically compels the company to provide this right?

A) GDPR Article 22's provisions on automated individual decision-making, including the right to human intervention and an explanation
B) CCPA's right to opt out of the sale of personal information
C) CCPA's right to request deletion of personal information
D) GDPR's general data minimization principle under Article 5

---

**Q6.** During the data preparation phase of an AI project, the team makes multiple transformations to the training dataset, including removing outliers, imputing missing values, and re-labeling records after discovering annotation errors. Before proceeding to the model development go/no-go gate, which documentation practice is MOST critical for maintaining accountability and supporting future audits?

A) Documenting only the final, cleaned dataset version, since intermediate transformation steps are not relevant once model development begins
B) Maintaining a version-controlled log of each transformation, its rationale, who performed it, and the ability to trace data lineage back to the original source
C) Verbally briefing the model development team on the changes made, without formal written records, to save project time
D) Relying on the data engineering team's personal notes, to be produced only if a regulator later raises a specific inquiry

---

**Q7.** A bank's AI credit-scoring model passed all fairness and demographic parity checks during pre-deployment validation, with results signed off at the model's go/no-go gate. Six months post-deployment, continuous monitoring detects a statistically significant disparate impact against a protected group that was not present at launch, traced to gradual data drift in applicant demographics. Per CPMAI responsible AI and accountability practices, what is the BEST next step?

A) Immediately retrain the model on the latest production data and redeploy without additional review, since the drift itself proves the original fairness sign-off is now invalid
B) Leave the model in production unchanged, since it already passed a documented fairness gate and that approval remains valid for the life of the model
C) Have the data science team quietly adjust the model's decision threshold to reduce the disparate impact metric, since this is a technical tuning issue that does not require governance sign-off
D) Formally log the drift and bias evidence in the model's audit trail, convene a new go/no-go review with legal, compliance, and business stakeholders, and document the decision to retrain, adjust, or retire the model in the accountability record

---

**Q8.** A retail bank wants to identify unusual credit card transactions that deviate from an individual cardholder's historical spending behavior in real time, flagging them for fraud review. Which of the Seven Patterns of AI BEST matches this business need?

A) Predictive Analytics and Decision Support Patterns
B) Recognition Patterns
C) Patterns and Anomalies Patterns
D) Goal-Driven Systems Patterns

---

**Q9.** During Business Understanding, a CPMAI-certified project manager evaluates automating invoice approval for a finance department that processes 40 invoices per week under three stable, well-documented approval rules that rarely change. Which feasibility conclusion is MOST appropriate?

A) Recommend deferring the decision until a large historical dataset of invoice decisions is collected for training
B) Recommend a traditional rule-based/RPA solution, since AI is not justified given low volume, stable rules, and no ambiguous judgment required
C) Recommend an autonomous goal-driven AI agent to fully replace the approval process end-to-end
D) Recommend a machine learning classification model since any manual process is an automation opportunity for AI

---

**Q10.** An HR team wants to deploy an AI tool to automatically screen and rank job applicant resumes before a recruiter reviews them. During the risk assessment, which risk category should be given the HIGHEST priority for this specific use case?

A) Performance risk, because the model may run slower than the manual process
B) Safety risk, because incorrect screening could physically harm applicants
C) Security risk, because resumes contain applicant contact information
D) Ethics risk, because the model may encode and amplify demographic bias present in historical hiring data, leading to discriminatory outcomes

---

**Q11.** Midway through Business Understanding, after the AI project scope statement has been drafted and approved, the executive sponsor requests adding real-time streaming inference capability that was not part of the original scope, and the data governance team confirms the required real-time data pipeline does not yet exist. According to CPMAI scope discipline, what should the project manager do?

A) Document the request as an out-of-scope item for the current phase, run it through formal change control, and re-evaluate feasibility and go/no-go criteria before deciding whether it becomes a future phase
B) Cancel the entire project since the sponsor changed requirements after scope was approved
C) Immediately add the new capability to the current phase since sponsor requests take priority over the documented scope
D) Silently ignore the request and continue with the original plan without informing the sponsor

---

**Q12.** An e-commerce company wants each customer to see a uniquely tailored homepage layout, product bundle, and pricing offer generated specifically from that individual's own behavior, rather than a segment-level recommendation shared across similar customers. Which of the Seven Patterns of AI does this use case represent?

A) Conversation and Human Interaction Patterns
B) Recognition Patterns
C) Hyperpersonalization Patterns
D) Predictive Analytics and Decision Support Patterns

---

**Q13.** When building the total cost of ownership (TCO) estimate for an AI initiative during Business Understanding, which cost component is MOST frequently underestimated or omitted entirely by organizations new to AI projects?

A) One-time cost of the kickoff workshop with stakeholders
B) Software licensing fees for the development IDE
C) Ongoing data labeling, model monitoring, drift detection, and periodic retraining costs after deployment
D) Initial cloud compute costs for model training

---

**Q14.** A retailer wants to automatically route inbound customer emails into one of twelve predefined topic categories (billing, shipping, returns, etc.) before they reach a human agent. Using the CPMAI Seven Patterns of AI framework, which pattern does this use case map to?

A) Goal-Driven Systems Pattern
B) Recognition Pattern
C) Hyperpersonalization Pattern
D) Autonomous Systems Pattern

---

**Q15.** A manufacturing team has a fully provisioned GPU cluster and unlimited compute budget approved, but the rare product defect they want a computer vision model to catch occurs in only 50 historical images out of 2 million units inspected. During the initial feasibility assessment, which factor is the PRIMARY blocker to proceeding?

A) Compute constraints
B) Data availability
C) Organizational readiness
D) Technical viability of the algorithm

---

**Q16.** An organization plans to deploy a facial recognition system to grant employees building access. During risk assessment, the team discovers the training dataset underrepresents certain demographic groups, causing higher false-rejection rates for those groups. How should this specific finding be classified in the CPMAI risk assessment?

A) A security risk, since unauthorized access could result
B) An ethical and fairness risk, since biased treatment of a demographic group results
C) A safety risk, since physical access controls are involved
D) An operational risk, since it will increase help desk tickets

---

**Q17.** A project team is drafting the AI project scope statement for Phase 1 of a predictive maintenance initiative. Which of the following statements belongs correctly under the OUT-OF-SCOPE section, rather than as a success criterion or in-scope deliverable?

A) The model must achieve at least 85% precision on the held-out validation set
B) Integration with the legacy ERP system's work-order module is deferred to a future phase
C) Unplanned equipment downtime must be reduced by 20% within six months of go-live
D) The project must remain within the approved Q3 budget allocation

---

**Q18.** A company built an internal churn-prediction model and presented a business case based solely on the data science team's development cost estimate. Six months after launch, leadership rejects continued funding, citing costs far exceeding the original business case. Data drift required frequent retraining, and a dedicated labeling team had to be hired to keep ground-truth data current. What was the flaw in the original business case?

A) The success criteria for the model were set too low
B) The team failed to include a security risk assessment before deployment
C) The TCO calculation omitted ongoing operational costs such as retraining, relabeling, and monitoring
D) The in-scope and out-of-scope boundaries were never documented

---

**Q19.** An AI model for prioritizing high-risk loan applications for manual review achieves 96% accuracy in testing and is deployed. Three months later, adoption data shows underwriters are manually overriding or ignoring the model's recommendations in most cases, and the expected efficiency gains have not materialized. What is the MOST likely root cause from a CPMAI project management perspective?

A) Insufficient change management and training left underwriters distrustful of the model's recommendations
B) The model's accuracy metric was measured incorrectly
C) The model was deployed using the wrong AI pattern for the use case
D) The data used for training was not representative of production data

---

**Q20.** A CPMAI project team is building a fraud-detection model. During Identify Data Needs, exploratory data analysis on two years of historical transaction data reveals 0.3% fraud cases (severe class imbalance) and 40% missing values in the three features SMEs identified as most predictive of fraud. The team must decide whether to proceed to Data Preparation on schedule. Per the CPMAI go/no-go discipline, what is the BEST course of action?

A) Proceed to Data Preparation immediately and rely on imputation and SMOTE-style resampling techniques to fix the gaps during modeling
B) Move directly into model development since the data volume across two years is large enough to compensate for missing values statistically
C) Issue a documented no-go decision, and work with data SMEs and stewards to source supplemental data or redefine feature availability before proceeding
D) Deprioritize the three predictive features from scope and proceed with only the complete fields to keep the schedule on track

---

**Q21.** During Identify Data Needs for a customer churn model, the required internal data lives in a finance-owned data warehouse that requires governance council approval to access, and a needed third-party behavioral dataset requires a licensing and compliance review before use. The project sponsor wants a firm 3-week delivery commitment for the training dataset. What should the CPMAI-trained project lead do?

A) Initiate the governance access request and the licensing/compliance review in parallel immediately, and set the delivery commitment only after both are confirmed
B) Commit to the 3-week timeline and begin building extraction pipelines now, assuming both approvals will be granted
C) Bypass the governance council since the warehouse data will only be used internally for an internal project
D) Substitute both data sources with publicly available datasets to avoid the approval delays entirely

---

**Q22.** Which role is PRIMARILY responsible for defining acceptable data quality thresholds and enforcing organizational data governance policies during the Identify Data Needs sub-phase of a CPMAI project?

A) Data Scientist
B) Data Steward
C) ML Engineer
D) Business Sponsor

---

**Q23.** A predictive maintenance project ingests continuous IoT sensor data streaming at several gigabytes per hour from manufacturing equipment. During Identify Data Needs, what infrastructure characteristic must be specified to prevent bottlenecks once Data Preparation begins?

A) A single on-premises relational database configured for nightly batch reporting
B) A shared spreadsheet workbook updated manually by plant operators each shift
C) Elastic, scalable streaming ingestion and storage capacity sized for sustained high-velocity data with headroom for peak loads
D) A monthly manual file export process coordinated by IT

---

**Q24.** A team is defining data requirements for a model predicting rare equipment failures, where the historical failure rate is under 0.1% of all records. To ensure the eventual training and evaluation sets adequately represent failure events, what sampling approach should be specified in the Identify Data Needs data requirements?

A) Stratified sampling with deliberate oversampling of the minority failure-event class
B) Simple random sampling proportional to the overall population distribution
C) Convenience sampling limited to the most recent month of operational data
D) Systematic sampling that selects every 10th record chronologically

---

**Q25.** Why does CPMAI treat the data go/no-go decision as fundamentally distinct from a requirements sign-off in a traditional software development project?

A) Because the go/no-go decision validates whether real, available data can actually support the intended predictive use case, whereas traditional requirements assume functionality can be built as specified once resourced
B) Because AI projects have no formal requirements documentation, unlike traditional software projects
C) Because the go/no-go decision is only a budgeting checkpoint with no bearing on technical feasibility
D) Because traditional software projects never require stakeholder approval before development begins

---

**Q26.** A CPMAI project team is building a fraud-detection model. The data science lead wants direct access to transaction records, but the records are governed by the finance department's chief data steward, who requires a formal data-sharing agreement and masking of PII before release. The AI project manager pushes to skip the agreement to meet a deadline. What is the CORRECT CPMAI-aligned action?

A) Escalate to the sponsor to override the steward since the project manager owns the timeline
B) Have the data scientist request a temporary personal export directly from the source system administrator
C) Follow the data steward's governance process, including the sharing agreement and PII masking, before granting access
D) Proceed using a synthetic dataset that mimics the transaction schema until the agreement is finalized

---

**Q27.** During data source mapping for a customer churn model, the team discovers that the CRM data is owned by the sales operations department, but a third-party marketing analytics vendor holds a supplemental engagement dataset under a contract that restricts use to marketing purposes only. Which finding should the AI project team flag as a BLOCKING issue during the Identify Data Needs domain, not just a note for later?

A) The CRM data uses a different customer ID format than the vendor dataset
B) The CRM system was last upgraded two years ago
C) The vendor dataset has more null values in the engagement score field than expected
D) The vendor dataset's contractual usage restriction may prohibit its use for churn modeling

---

**Q28.** An AI project requires training a computer vision model on high-resolution video feeds. The team must coordinate the AI workspace and infrastructure before data gathering begins. Which requirement is MOST specific to this domain's infrastructure coordination activity, as opposed to later model development activities?

A) Selecting the neural network architecture appropriate for video classification
B) Provisioning sufficient secure storage and compute capacity to ingest and stage the raw video volume
C) Tuning hyperparameters for the video model's training pipeline
D) Choosing the evaluation metric to assess video classification accuracy

---

**Q29.** A CPMAI team is gathering data from a legacy mainframe system via nightly batch extracts feeding a cloud data lake for an ongoing AI initiative. Which practice BEST satisfies the CPMAI requirement to validate completeness of gathered data during this phase?

A) Reviewing the mainframe vendor's published system uptime SLA
B) Confirming the data lake storage tier is set to hot access for faster queries
C) Comparing record counts and key checksums between the source extract and the landed data lake files after each transfer
D) Verifying that the data scientists have read permissions on the new lake files

---

**Q30.** While evaluating data for a healthcare risk-prediction AI initiative, the team finds that a portion of the patient dataset originates from a research repository whose data use agreement permits use only for 'internal quality improvement studies,' not commercial product development. The AI initiative is intended to become a commercial product. What should the project team do?

A) Treat this as a go/no-go blocking issue and escalate for legal review or renegotiation of the data use agreement before proceeding
B) Proceed with model development but exclude the restricted data only from the final production training set
C) De-identify the restricted patient records further and treat them as compliant for commercial use
D) Continue using the data since de-identified healthcare data is generally exempt from use restrictions

---

**Q31.** An AI project manager must convey the results of the data evaluation phase to non-technical executive sponsors before the go/no-go decision. The data team found significant class imbalance and moderate missingness in a key feature, but nothing severe enough to halt the project. Which communication approach BEST fits CPMAI's guidance for conveying data understanding to leadership?

A) Present the full statistical distribution tables and missingness heatmaps generated by the data scientists without modification
B) Withhold the data quality findings from leadership since the recommendation is to proceed anyway
C) Send the raw exploratory data analysis Jupyter notebook to the sponsors for their own review
D) Summarize the findings in business terms, explain the practical risk and mitigation plan, and state a recommendation to proceed with conditions

---

**Q32.** A project team is preparing to move from data preparation into model development. During final data quality review, the team discovers that 15% of records in the training dataset have missing values in a feature identified as highly predictive during business understanding, and the missingness is not random but correlates strongly with a specific customer segment. What is the BEST course of action regarding the go/no-go gate decision?

A) Halt the gate decision, investigate the root cause of the non-random missingness, and remediate the bias risk before proceeding
B) Proceed to the model development gate since 85% completeness meets typical data quality thresholds
C) Proceed but flag the issue for the data scientists to handle with simple mean imputation during training
D) Reject data preparation entirely and restart the project from the business understanding phase

---

**Q33.** During final evaluation for the operationalization go/no-go gate, a model achieves 94% accuracy on the held-out test set, meeting the primary success criterion set during business understanding. However, on a stress-test dataset representing seasonal variation and rare edge cases, performance drops to 61%. The sponsor is eager to deploy immediately given the headline accuracy figure. What should the team recommend?

A) Approve for operationalization since the primary success criterion of 94% test accuracy has been satisfied
B) Approve for operationalization but have the sponsor sign a documented waiver acknowledging the risk
C) Withhold approval; the model has not demonstrated adequate robustness and generalization across representative real-world conditions, so it fails the operationalization gate despite the headline accuracy
D) Approve for a narrow initial deployment restricted to conditions matching the training distribution, with no further evaluation required

---

**Q34.** A logistics company wants a system to determine optimal delivery route sequencing. There is no historical dataset of 'correct' routes, and the system only receives feedback (total fuel cost and delivery time) after an entire day's route sequence is completed in a simulated environment. Which category of technique is MOST appropriate for this use case?

A) Supervised learning, using historical route completion times as the prediction label
B) Unsupervised clustering to group delivery locations by geographic proximity
C) Semi-supervised learning combining a small set of labeled optimal routes with a larger unlabeled dataset
D) Reinforcement learning, where an agent learns a routing policy through trial-and-error interaction with the simulated environment to optimize delayed cumulative reward

---

**Q35.** A data science team ran 40 experiments over three weeks, adjusting hyperparameters and feature sets. The AI project manager later asks why experiment version 27 outperformed version 34 despite similarly reported metrics, but no one can reconstruct what data snapshot, code version, or hyperparameters were used for version 34. Which practice should the project manager have enforced from the start to prevent this?

A) Weekly status meetings where the team verbally reports experiment progress
B) Requiring every experiment to use identical hyperparameters so results remain directly comparable
C) Capping the team at a maximum of 10 experiments to reduce overall complexity
D) A rigorous experiment tracking and data/model versioning system that logs the data snapshot, code commit, hyperparameters, and evaluation metrics for every training run

---

**Q36.** During a peer review of model development artifacts, a senior data scientist discovers that the team performed hyperparameter tuning and feature selection using the same held-out test set that was later used to report the model's final performance metrics. What is the MOST significant risk this introduces, and what should the reviewer recommend?

A) No significant risk exists, since test set reuse is standard practice as long as the test set is sufficiently large
B) The team should simply reduce the number of hyperparameter combinations evaluated to compensate for the reuse
C) The team should apply cross-validation exclusively on the test set to correct for the bias introduced
D) This constitutes data leakage; the reviewer should recommend re-splitting the data into distinct train, validation (for tuning), and test (for final unbiased evaluation) sets, and re-running the evaluation

---

**Q37.** A healthcare AI project is developing a model to support clinical treatment recommendations, and regulatory requirements mandate that clinicians be able to understand the reasoning behind each recommendation. A deep neural network ensemble achieves 96% accuracy, while a rule-based decision tree achieves 89% accuracy but produces human-readable decision paths. According to CPMAI principles on technique selection trade-offs, what should guide the final model selection?

A) Always select the highest-accuracy model regardless of other factors, since business value depends primarily on predictive performance
B) Deploy the deep neural network and address interpretability afterward using post-hoc marketing materials aimed at clinicians
C) Average the outputs of both models to arrive at a compromise between accuracy and interpretability
D) Weigh the interpretability requirement imposed by the use case and regulatory context alongside performance; here, the accuracy gap likely does not justify sacrificing the mandated explainability, favoring the more interpretable model

---

**Q38.** An AI project team presents results for the operationalization go/no-go gate. The model achieves 98% accuracy on the training set, but accuracy drops to 76% on the held-out test set, and 5-fold cross-validation shows accuracy ranging from 68% to 91% across folds. The success criteria defined during business understanding required at least 85% accuracy with consistent performance across data segments. The team argues the training accuracy proves the model is ready and requests approval to proceed to deployment. As the AI project manager applying CPMAI gate discipline, what is the correct decision?

A) Approve the gate because the training accuracy exceeds the 85% threshold, and deployment monitoring will catch any real-world performance issues
B) Deny the gate; the gap between training and test performance combined with high cross-validation variance indicates overfitting and poor generalization, so the model does not meet documented readiness criteria
C) Approve the gate but require the team to retrain using a larger number of epochs before the next sprint, since more training will resolve the accuracy gap
D) Deny the gate and immediately restart the project from business understanding, since the model's failure indicates the original business problem was not well defined

---

**Q39.** A fraud-detection model has been deployed to production for six months. The model's precision has dropped from 0.91 to 0.68, but investigation shows the input feature distributions remain statistically unchanged from training data. The relationship between transaction patterns and fraud outcomes has shifted due to new fraud tactics. Which phenomenon is occurring, and what governance action is MOST appropriate?

A) Data drift is occurring; the team should re-validate the data pipeline for schema errors before taking further action
B) Concept drift is occurring; the team should trigger scheduled retraining with updated labeled data reflecting the new fraud patterns
C) Model decay from infrastructure latency is occurring; the team should scale up compute resources serving the model
D) Label leakage occurred during original training; the team should roll back to a previous model version immediately

---

**Q40.** An organization is deploying a new AI-powered loan-approval model to replace a legacy rules engine. Leadership wants to validate the model's real-world behavior on live production traffic without exposing customers to any risk if the model performs poorly. Which deployment strategy BEST satisfies this requirement?

A) Blue-green deployment, cutting over 100% of traffic to the new model at a scheduled release window
B) Canary deployment, routing 5% of live customer traffic to the new model and monitoring outcomes
C) A/B testing, randomly splitting all customers 50/50 between the legacy engine and new model for final decisions
D) Shadow deployment, running the new model in parallel on live traffic while the legacy engine continues making all actual decisions

---

**Q41.** A CPMAI practitioner is finalizing the model governance plan for a production churn-prediction model. Which trigger condition should be explicitly configured to initiate an unscheduled retraining cycle, rather than waiting for the next scheduled retraining interval?

A) Monitoring dashboards detect that a performance metric has crossed a predefined degradation threshold indicating drift
B) The model's serving infrastructure completes a routine security patch with no downtime
C) A new engineer joins the MLOps team and requests access to the model repository
D) The quarterly stakeholder report is due for submission to the steering committee

---

**Q42.** During post-deployment monitoring, an AI-driven inventory-forecasting model begins producing recommendations that lead to significant stockouts across multiple warehouses within 48 hours of a new version release. The contingency plan for this solution defines an incident response procedure. What should the team do FIRST, according to CPMAI contingency planning best practices?

A) Immediately notify the executive steering committee and schedule a lessons-learned retrospective meeting
B) Begin retraining a new model version from scratch using the most recent 90 days of inventory data
C) Execute the predefined rollback procedure to revert to the last known-stable model version while the incident is investigated
D) Update the final project report to document the incident for future reference

---

**Q43.** As a project transitions from the project delivery team to operational support (BAU), the CPMAI transition plan must define clear ownership. Six weeks after go-live, a model's prediction latency begins exceeding SLA thresholds. No one on the support team acted for two days because it was unclear who owned infrastructure-level performance monitoring versus who owned model-quality monitoring. What gap does this scenario BEST illustrate?

A) An absence of clearly defined roles and responsibilities (e.g., RACI) in the transition plan for ongoing operational ownership
B) A failure to configure automated threshold alerting on the monitoring dashboard
C) An insufficient data preparation phase that failed to account for latency requirements
D) A missed opportunity to include the issue in the final project report and lessons learned

---

**Q44.** An organization's AI governance framework requires quarterly disaster recovery (DR) testing for all production AI solutions classified as business-critical. During a scheduled DR test, the team simulates a full outage of the model-serving endpoint. Which outcome would indicate the contingency plan is functioning as intended?

A) The fallback mechanism (e.g., cached predictions or rules-based backup) activates automatically and business operations continue within the defined recovery time objective
B) The test is postponed because simulating an outage on a live business-critical system is too risky to attempt
C) The model automatically retrains itself using synthetic data generated during the outage simulation
D) The incident is logged for the annual audit but no failover action occurs during the test itself

---

**Q45.** A production customer churn model is retrained quarterly per its governance schedule. Six weeks after the most recent retraining, monitoring dashboards show that predicted churn probabilities remain well-calibrated against actual outcomes, but the distribution of the top predictive features (contract length, support ticket volume) has shifted significantly because of a new pricing plan launched last month. Overall accuracy metrics have not yet degraded. According to CPMAI production governance practices, what is the MOST appropriate action at this point?

A) Immediately roll back to the previous model version and initiate incident response, since drift has been detected in production
B) Take no action until accuracy or calibration metrics actually degrade, since predictions remain well-calibrated
C) Retrain the model on the shifted feature distribution using the same algorithm and redeploy immediately without a go/no-go gate review
D) Flag the detected input/data drift for closer monitoring and evaluate whether the next scheduled retraining cycle should be moved earlier, without treating it as a production incident

---

**Q46.** An AI project team has completed deployment of a predictive maintenance model and produced the final project report and lessons-learned document. Which of the following BEST reflects a properly executed transition from the project team to operational support, per CPMAI's closing-the-loop practices?

A) The project sponsor signs off on the final report and closes the project, with production monitoring, escalation, and retraining handled by the original data scientists on an as-needed basis
B) A documented transition plan is executed that assigns specific operational roles (monitoring, escalation, retraining ownership) to the operations/support team, includes formal knowledge transfer sessions, and defines the contingency and incident response procedures the support team is responsible for periodically testing
C) The solution is handed over via the deployment runbook only, since the runbook already contains all the technical configuration the operations team needs to manage the model going forward
D) The project team retains ownership of production monitoring indefinitely to preserve continuity of expertise, deferring formal transition to operations until a major model retraining occurs

---

