# Practice Test 1: PMI-CPMAI Certification Exam Prep Masterclass

- **Questions:** 46
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-1.md`. Track results in `score-tracker.md`.

---

**Q1.** A healthcare AI vendor is building a model to predict patient readmission risk using historical EHR data that includes protected health information. Before data collection begins, the project team wants to identify and mitigate privacy risks to individuals whose data will be used, and document the legal basis for processing. Which activity BEST accomplishes this within the CPMAI Responsible AI practices?

A) Wait until model deployment and then publish a privacy policy on the company website
B) Apply column-level encryption to the EHR database after the model is trained
C) Ask the data science team to informally review the dataset for sensitive fields
D) Conduct a Privacy Impact Assessment (PIA) covering data flows, risks to individuals, and mitigation measures

---

**Q2.** During model evaluation, a hiring-recommendation model shows a 78% approval rate for one demographic group compared to 52% for another with similar qualifications, despite race and gender being excluded as direct model features. What is the MOST likely explanation the team should investigate first?

A) The model architecture is too complex to be explainable
B) Proxy variables correlated with the protected attribute are driving the disparity
C) The training data was encrypted incorrectly, corrupting feature values
D) The model's version control log was not updated before evaluation

---

**Q3.** A regulator asks an AI project team to explain why a loan-denial decision was made by their machine learning model for a specific applicant. Which capability should the team have built into the AI system from the outset to satisfy this request?

A) A model interpretability/explainability tool that generates per-decision feature attribution
B) A dashboard showing overall model accuracy across the test dataset
C) A data lineage diagram showing where the training data originated
D) A service-level agreement guaranteeing 99.9% system uptime

---

**Q4.** An AI team is designing access controls for a shared data lake containing training data for multiple models, some of which include sensitive customer attributes. Which configuration approach BEST supports both privacy compliance and AI/ML transparency requirements?

A) Grant all data scientists read/write access to the entire data lake to accelerate experimentation
B) Store all data in a single unencrypted shared folder with a password known to the whole team
C) Implement role-based access control (RBAC) with least-privilege permissions and log all data access for audit purposes
D) Allow access based on manager approval given verbally, with no system-level enforcement

---

**Q5.** Which statement BEST distinguishes 'chain of custody' documentation from 'model version control' in the context of CPMAI accountability practices?

A) Chain of custody tracks who accessed, modified, or transferred data across the lifecycle, while version control tracks changes to model code, parameters, and training artifacts over time
B) Chain of custody and version control are interchangeable terms describing the same artifact
C) Chain of custody only applies to physical evidence in legal cases and has no relevance to AI projects
D) Version control applies exclusively to data, while chain of custody applies exclusively to models

---

**Q6.** A company operating AI-driven credit scoring in multiple countries learns that a new AI-specific regulation is being finalized in one jurisdiction that will require algorithmic impact disclosures. What is the MOST appropriate CPMAI-aligned response for the AI project team?

A) Coordinate with legal/compliance teams to monitor the regulation's progress and prepare accountability documentation in advance of enforcement
B) Ignore the pending regulation until it is officially enacted and enforced
C) Immediately shut down the AI system in all jurisdictions to avoid any risk
D) Delegate all regulatory tracking to the data science team without legal involvement

---

**Q7.** An organization's AI-based resume screening tool is monitored post-deployment. Analytics reveal the model recommends male candidates for technical roles at a significantly higher rate than female candidates with comparable qualifications. Following CPMAI responsible AI practices, which action BEST addresses this finding?

A) Retrain the model using only the most recent batch of resumes to improve overall accuracy
B) Conduct a fairness analysis to identify the root cause of the disparate impact and apply bias mitigation techniques such as reweighting, adversarial debiasing, or threshold adjustment before redeployment
C) Remove the gender field from the training data and redeploy the model without further bias validation
D) Immediately and permanently shut down the AI tool, revert to fully manual screening, and close the investigation without documentation

---

**Q8.** A retail company wants an AI system that automatically routes incoming customer emails into categories like 'billing', 'shipping', and 'returns' based on the text content of each message. Which of the Seven Patterns of AI best matches this business need?

A) Goal-Driven Systems / Optimization Pattern
B) Hyperpersonalization Pattern
C) Recognition Pattern
D) Autonomous Systems Pattern

---

**Q9.** During the Identify phase, a project team wants to build a fraud-detection model but discovers only 500 labeled fraud examples exist across three years of transaction history. According to CPMAI feasibility evaluation practices, what should the team recommend?

A) Proceed immediately with a deep learning model since fraud detection always requires neural networks
B) Outsource the entire project to a vendor without further internal review
C) Recommend a traditional rule-based or heuristic approach as an interim solution while a data collection and labeling plan is developed
D) Lower the accuracy requirements so the small dataset becomes acceptable

---

**Q10.** An HR department wants to deploy an AI tool that screens job applicant resumes and ranks candidates before human review. As part of the Identify phase risk assessment, what should the project team prioritize before approving this project to move forward?

A) Skip fairness and bias testing since the vendor claims the tool is unbiased
B) Only assess IT security risks such as data encryption, since HR data is the main concern
C) Conduct an ethical and safety risk assessment evaluating potential disparate impact or bias against protected groups, with documented mitigation steps
D) Defer all risk assessment until after the tool is deployed and monitor for complaints

---

**Q11.** A team drafting an AI project scope statement for a demand-forecasting initiative wants it to properly reflect the exploratory nature of AI development, distinguishing it from a traditional software scope statement. Which element should the scope statement explicitly include?

A) A guarantee of a specific final model accuracy percentage that will not change during development
B) Only the technical architecture diagram, since AI scope is determined entirely by infrastructure
C) Defined success criteria and acceptable performance thresholds, along with documented assumptions about data and iterative refinement expectations
D) No out-of-scope boundaries, since AI projects should remain open-ended to allow flexibility

---

**Q12.** A finance director is building the business case for a new AI-driven expense-anomaly-detection system and estimates total cost of ownership based solely on the one-time development and initial deployment cost of $150,000. What is the MOST significant gap in this TCO estimate from a CPMAI perspective?

A) The estimate should also include the cost of a marketing campaign to announce the new system
B) The estimate omits ongoing costs such as model retraining, data labeling, infrastructure monitoring, and MLOps support required to sustain model performance over time
C) The estimate is too high and should be reduced to attract executive approval
D) The estimate should only include hardware costs and exclude all software licensing

---

**Q13.** Warehouse staff are resisting a newly deployed AI system that recommends inventory reorder quantities, stating they don't trust its recommendations and continue to use manual methods. According to CPMAI guidance on managing adoption and integration risk, what should the project team have prioritized during the Identify phase to reduce this outcome?

A) Mandating system use through a policy memo without additional preparation
B) Involving end users early in requirements gathering, providing training, and ensuring the system's recommendations include enough transparency for staff to understand and trust the logic
C) Replacing the warehouse staff with employees more comfortable with automation
D) Assuming the technical accuracy of the model would be sufficient to guarantee organic adoption

---

**Q14.** A retail company wants an AI solution that analyzes an individual customer's browsing and purchase history alongside the behavior of similar customers to generate a uniquely tailored recommendation feed for that specific customer, effectively treating each shopper as a segment of one. Which of the Seven Patterns of AI in the CPMAI Methodology BEST matches this business need?

A) Recognition pattern
B) Goal-driven autonomous systems pattern
C) Basic predictive analytics pattern
D) Patterns of patterns (hyperpersonalization) pattern

---

**Q15.** During the feasibility assessment for a predictive maintenance initiative, the CPMAI-certified project lead discovers that the plant's sensors have only logged data for six weeks, use inconsistent timestamp formats, and lost prior history during a system migration eight months ago. Given the CPMAI go/no-go gate discipline, what is the MOST appropriate action?

A) Proceed directly to model development since the sensors are already collecting live data
B) Recommend pausing development, establishing proper data collection and retention practices, and reassessing feasibility once sufficient historical data exists
C) Recommend a no-go decision and permanently terminate the AI initiative
D) Outsource all data collection to a third-party vendor without further internal review

---

**Q16.** An HR department proposes an AI system to automatically screen job applicant resumes and rank candidates for interview. During the risk assessment phase, which risk category should the CPMAI practitioner prioritize as the PRIMARY concern for this specific use case?

A) Ethical and bias risk related to discriminatory outcomes against protected groups
B) Network latency risk during model inference
C) Vendor lock-in risk from cloud provider selection
D) Compute infrastructure scalability risk

---

**Q17.** When drafting the AI project scope statement during the Identify Business Needs and Solutions phase, what is the primary purpose of explicitly listing 'out-of-scope' items?

A) To satisfy legal compliance documentation requirements only
B) To identify which team members will not be assigned to the project
C) To list the vendors that were not selected during procurement
D) To prevent scope creep by clearly setting stakeholder expectations about what the AI solution will NOT address

---

**Q18.** A project sponsor asks for a total cost of ownership (TCO) estimate before approving the AI project's business case. According to CPMAI best practices, which cost category is MOST often underestimated by teams during this exercise?

A) Initial software licensing fees
B) One-time data scientist salaries during the model build phase
C) Ongoing costs for model monitoring, retraining, data labeling, and drift correction after deployment
D) Hardware procurement costs for the initial pilot

---

**Q19.** During the resource identification step of Identify Business Needs and Solutions, a CPMAI practitioner finds that the organization has strong data engineering capabilities but no personnel experienced in model selection, hyperparameter tuning, or model evaluation. What does this finding represent?

A) An infrastructure and compute capacity gap
B) A skills/team resource gap that should be addressed via hiring, training, or contractor engagement before proceeding
C) A data availability gap requiring additional data collection
D) A risk limited only to model interpretability

---

**Q20.** A company is building a predictive maintenance AI model. During the Identify Data Needs phase, the team discovers sensor data covers only 60% of required equipment types, spans 3 years of history, but has 40% missing values in critical readings. Per the CPMAI methodology, what is the BEST next step?

A) Proceed directly to data preparation despite the gaps, since deadlines are tight
B) Issue a data no-go decision and return to business understanding to redefine scope or identify additional data sources
C) Skip data preparation and move directly to model development using the available data
D) Discard the project entirely, since equipment sensor data quality issues can never be resolved

---

**Q21.** An AI team needs authoritative definitions of the 'customer churn' fields stored in the CRM system, along with knowledge of historical schema changes affecting those fields. Which role should the team engage during the Identify Data Needs phase?

A) The data steward/subject matter expert responsible for the CRM system and its data definitions
B) The end-user who will interact with the AI application's UI
C) The executive sponsor funding the project
D) An external compliance auditor

---

**Q22.** An AI team preparing for a computer vision project requires GPU-accelerated compute, versioned datasets, and collaborative notebooks accessible to a distributed team. What should the team coordinate during the Identify Data Needs phase to enable this?

A) An AI development workspace with provisioned GPU compute, versioned storage, and collaboration/version-control tooling
B) A single developer's local laptop with no shared access
C) A shared spreadsheet distributed via email
D) A static, read-only business intelligence dashboard

---

**Q23.** A team plans to enrich its training dataset with a demographic dataset purchased from a third-party vendor. Before ingesting this data, what MUST the team verify first per CPMAI data identification practices?

A) Only the file format and schema compatibility with existing systems
B) The vendor's website design and marketing collateral
C) The total file size of the dataset
D) The licensing terms, usage rights, and applicable privacy/regulatory compliance (e.g., GDPR) for the intended AI use case

---

**Q24.** During data evaluation, the team assesses 'completeness' as a data quality dimension for a required dataset. Which measurement directly indicates completeness issues?

A) The number of columns present in the dataset
B) The average API response latency when querying the data source
C) The number of duplicate records identified during profiling
D) The percentage of missing or null values across fields required for the AI solution

---

**Q25.** When conveying data understanding findings to executive leadership after the data evaluation activities are complete, what approach does the CPMAI methodology recommend?

A) Present raw statistical profiling output and technical charts without business context
B) Translate data quality, gaps, and readiness findings into business-relevant risk and opportunity language leadership can act on
C) Delay any reporting to leadership until after model development is complete
D) Only report data findings if leadership explicitly requests an update

---

**Q26.** A CPMAI project team has assembled a list of business subject matter experts who can explain what the data represents in context, but the team still cannot get authoritative answers about who is allowed to approve external access to the customer master dataset or how field-level lineage should be documented. Which role is missing from the team?

A) A data scientist to build exploratory models
B) A data steward responsible for governance and access policy over the dataset
C) A project sponsor to approve the AI business case
D) A UX designer to validate how the data will be displayed

---

**Q27.** During data source mapping, the team discovers that a third-party vendor feed used for training data is licensed only for internal analytics reporting, not for training commercial AI models that will be resold to customers. What should the team do next in the Identify Data Needs phase?

A) Escalate the licensing conflict and either renegotiate terms or exclude the dataset before further use
B) Proceed with model training since the data is already integrated into the pipeline
C) Anonymize the dataset so licensing restrictions no longer apply
D) Move the licensing review to the operationalization phase after the model is built

---

**Q28.** An AI team is planning its workspace for a computer vision project that will require iterative deep learning model training on large image batches, along with version control for datasets and experiment tracking. Which infrastructure decision best reflects CPMAI guidance for this stage?

A) Use only a shared spreadsheet to track experiment results and skip specialized compute
B) Provision standard CPU-only virtual machines identical to those used for the business intelligence team
C) Provision GPU-enabled compute resources and set up dataset/version control and experiment tracking tooling before development begins
D) Wait until model development begins to determine compute and tooling needs

---

**Q29.** A fraud-detection AI solution requires transaction data that is refreshed hourly from an operational database in order to remain effective. Which activity should the team prioritize when gathering this data during the Identify Data Needs phase?

A) Design and validate an automated, monitored data feed with completeness checks for each refresh cycle
B) Perform a single one-time bulk export sufficient for the entire project lifecycle
C) Manually re-run extraction queries by hand at the start of each project sprint
D) Defer refresh procedure design until after the model reaches production

---

**Q30.** While reviewing data intended for a healthcare AI solution, the team finds patient records that include identifiable information collected without documented consent for AI-driven secondary use. According to CPMAI practices for checking privacy and compliance, what should occur before this data is used?

A) Use the data as-is since it was already legally collected by the healthcare provider for treatment purposes
B) Delay the privacy review until after the model has been trained and evaluated
C) Confirm and document a lawful basis or consent for the AI use case, or apply appropriate de-identification/compliance controls before use
D) Route the compliance question to the marketing team since they manage customer communications

---

**Q31.** After exploratory data analysis, the team finds that the available dataset covers only three of the five customer segments the AI solution is intended to serve, with no near-term way to obtain data for the missing segments. What is the appropriate go/no-go decision under CPMAI guidance?

A) Proceed to full-scale model development and address segment gaps after deployment
B) Ignore the gap since three out of five segments represents majority coverage and is acceptable
C) Document the gap as a scope limitation, and either revise the use case scope, seek alternative data sources, or issue a no-go until the gap is resolved
D) Substitute synthetic data for the missing segments without validating its business relevance

---

**Q32.** A healthcare AI project team has completed data preparation and wants to proceed into model development. Which of the following BEST demonstrates that the data quality go/no-go gate should be passed?

A) The data science team has visually inspected a sample of records and found no obvious anomalies
B) Data has been validated against agreed quality dimensions (completeness, accuracy, consistency) and documented as meeting defined thresholds for the intended use case
C) All available data sources have been collected and merged, regardless of quality issues
D) Every record has been manually labeled with a guarantee of 100% label accuracy

---

**Q33.** A fraud detection model achieves 96% accuracy on training data but only 71% on the holdout test set, with performance dropping further on a separate out-of-time validation set. What should the team recommend at the operationalization go/no-go gate?

A) Go — deploy to production and rely on post-launch monitoring to catch performance drift
B) Go — 96% training accuracy exceeds the defined success criteria, so it should be deployed immediately
C) No-go — the team should request more compute resources to build an even more complex model architecture
D) No-go — the model shows overfitting and poor generalization; it should return to model development for retraining or regularization before proceeding

---

**Q34.** A retailer wants to segment its customer base into distinct groups based on purchasing behavior, with no predefined labels for what the groups should be. Which modeling approach should be selected during technique selection?

A) Supervised classification
B) Unsupervised learning (e.g., clustering)
C) Reinforcement learning
D) Supervised regression

---

**Q35.** During iterative model training, the model manager needs to ensure that hyperparameters, dataset version, and resulting performance metrics can be compared reproducibly across dozens of experiment runs. Which practice BEST supports this need?

A) Standardizing on a single hyperparameter configuration for all future experiments
B) Increasing the number of training epochs for every run to force convergence
C) Implementing an experiment tracking system that logs hyperparameters, data version, and metrics for every run
D) Relying on team members' personal notes and spreadsheets updated at the end of each week

---

**Q36.** In CPMAI model technique selection, choosing a highly complex deep learning model over a simpler decision tree with comparable accuracy for a regulated lending decision use case primarily introduces which trade-off risk?

A) Reduced interpretability/explainability, which may conflict with regulatory and responsible AI requirements
B) Elimination of the need for model QA/QC testing
C) Guaranteed higher accuracy regardless of future data changes
D) Reduced training data requirements compared to the simpler model

---

**Q37.** A model development team applies ad hoc, unversioned manual data cleaning scripts, and different team members run slightly different transformation steps locally. Which risk does this MOST directly introduce?

A) Elimination of the need for the data quality go/no-go gate
B) Guaranteed improvement in model generalization due to varied preprocessing
C) Increased model interpretability because of varied preprocessing approaches
D) Loss of reproducibility, making it difficult to trace which data transformations produced a given model's results

---

**Q38.** An AI project team has completed model training for a customer churn prediction model. The model achieves 94% accuracy on the training set and 93% accuracy on the test set, meeting the documented success criteria. The project manager is preparing for the go/no-go gate decision to move the model into operationalization. Which additional factor MUST be verified before approving this gate, according to CPMAI practice?

A) Whether the model's feature engineering pipeline uses the same programming language as the production environment
B) Whether the data scientists who built the model have completed at least two prior AI projects
C) Whether the model's hyperparameters were tuned using grid search rather than random search
D) Whether the model demonstrates robustness and generalization across varied data conditions beyond the test set, along with deployment readiness

---

**Q39.** An AI model for credit risk scoring has been in production for eight months. The monitoring dashboard shows the model's prediction accuracy has dropped from 92% to 81% over the last six weeks, while the underlying data pipeline shows no errors. What should the operations team do FIRST?

A) Immediately roll back to the previous model version without further investigation
B) Investigate for concept drift or data drift by comparing current input data distributions against the training baseline
C) Shut down the model and revert to fully manual credit decisions until a root cause is found
D) Increase the model's confidence threshold to filter out low-confidence predictions

---

**Q40.** During go-live of a new fraud detection model, the deployment team discovers that the production scoring API is returning malformed responses for 15% of transactions, causing downstream order processing failures. According to CPMAI deployment planning best practices, what should have been prepared in advance to handle this exact situation?

A) A stakeholder communication plan describing project milestones
B) A model card describing the training data lineage
C) A retraining schedule for the next model version
D) A documented rollback and contingency procedure with defined triggers and a tested fallback path

---

**Q41.** Which artifact is MOST appropriate for defining who is responsible for approving model retraining, monitoring drift thresholds, and authorizing version changes once an AI solution moves from the project team to ongoing operations?

A) The initial project charter
B) The data quality assessment report from the data understanding phase
C) The business case ROI calculation
D) A model governance and lifecycle management plan with a RACI matrix for ongoing operational roles

---

**Q42.** A company's operations dashboard for a customer churn prediction model currently shows only infrastructure metrics like CPU utilization and API latency. Business stakeholders complain they cannot tell whether the model is still delivering value. What should be added to close this gap?

A) More detailed server log exports for the data science team
B) A list of all hyperparameters used in the last training run
C) Additional infrastructure metrics such as disk I/O and memory usage
D) Business KPI metrics such as churn reduction rate and retention revenue impact, alongside model performance metrics like precision and recall

---

**Q43.** A team is setting up automated alerting for a demand forecasting model in production. Which configuration best reflects CPMAI guidance for threshold alerting on model performance degradation?

A) Set a statistically meaningful threshold (e.g., mean absolute percentage error exceeding an agreed baseline for a sustained period) and alert stakeholders and the governance owner when it is breached
B) Alert only when the model completely stops returning predictions
C) Alert whenever any single prediction differs from the previous day's prediction by more than 1%
D) Disable alerting and rely solely on quarterly manual model reviews

---

**Q44.** An AI project team has completed deployment and stabilization of a new predictive maintenance solution and is preparing to hand it off to the operations team. Which activity is essential to properly close the loop per CPMAI operationalization guidance?

A) Deliver a final report and lessons learned document, along with knowledge transfer materials and a transition plan defining operational roles and support responsibilities
B) Immediately reassign all project team members to new projects with no further involvement
C) Archive all project documentation and close the project management tool without further communication
D) Schedule a single all-hands meeting to announce the project is complete

---

**Q45.** A retail company's demand forecasting model has been in production for eight months. The operations team's monitoring dashboard shows the model's mean absolute percentage error (MAPE) has gradually increased from 8% at launch to 22% over the past six weeks, while input data distributions show measurable shift in customer purchasing patterns. According to CPMAI production governance practices, which action should the team take FIRST?

A) Trigger the documented drift-response procedure: confirm the degradation against the alerting threshold, notify stakeholders, and initiate root-cause analysis to determine whether retraining is warranted
B) Immediately decommission the model and revert to manual forecasting until a replacement is built
C) Wait until the next scheduled quarterly retraining cycle since MAPE increases are expected over time
D) Adjust the model's output post-hoc with a manual correction factor to mask the increased error until year-end reporting

---

**Q46.** As part of closing out an AI deployment project, the CPMAI-trained project lead is finalizing the transition of a churn-prediction model to the operational support team. Which combination of actions BEST fulfills the 'closing the loop' requirements of the CPMAI methodology?

A) Deliver only the trained model artifact and API documentation, since technical handoff is sufficient for support continuity
B) Keep the original project team informally available for questions instead of formally reassigning ownership, to avoid overhead
C) Produce a final report with lessons learned, complete knowledge-transfer documentation, and formally define operational roles, responsibilities, and escalation paths for ongoing monitoring and retraining before releasing the project team
D) Schedule a retrospective meeting only if a major incident occurs after go-live

---

