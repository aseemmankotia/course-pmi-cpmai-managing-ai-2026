## Chapter 4: Business Case, ROI/TCO, Architecture, and Resourcing — Practice Questions

**Q1.** A retail company built an AI demand-forecasting model. The business case showed strong ROI based on compute and data labeling costs, but 8 months after launch, finance flags the project as unprofitable. Which cost category was MOST likely omitted from the original TCO calculation?

A) Initial GPU compute costs for model training
B) The cost of the historical sales dataset used for training
C) The salary of the data scientist who built the initial model
D) Ongoing model monitoring, retraining, and drift correction labor

<details>
<summary>Answer</summary>

**Correct: D**

TCO for AI is not a one-time cost — ongoing maintenance, model monitoring, and periodic retraining as data drifts are recurring costs that are the most commonly underestimated in AI business cases, unlike traditional software TCO.

**Why the others are wrong:**
- Training compute is an upfront cost typically already captured in initial TCO estimates.
- Data acquisition cost is also a known upfront line item usually included in initial estimates.
- Initial development labor is typically budgeted as part of the project's build phase.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** Customer service representatives are refusing to use a new AI-powered ticket-routing tool, claiming it will replace their jobs, even though leadership intends it only to reduce manual triage time. Using the ADKAR change management model, which stage is the project team failing to address?

A) Ability — reps lack the technical skill to use the tool
B) Desire — reps lack personal motivation to support the change
C) Awareness — reps don't understand why the change is happening
D) Reinforcement — the change hasn't been sustained long enough

<details>
<summary>Answer</summary>

**Correct: B**

Fear of job loss is a motivational/emotional resistance issue, which maps to the Desire stage of ADKAR — reps understand what's happening but don't want to personally support it.

**Why the others are wrong:**
- There is no indication in the scenario that reps lack technical skill to operate the tool.
- The reps clearly are aware of the tool and its purpose — they are actively refusing to use it, which is a desire/motivation issue, not an awareness gap.
- Reinforcement applies after adoption has begun; this resistance is occurring before adoption, at the motivational stage.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A team drafts a high-level AI solution architecture diagram showing: Data Sources → Data Ingestion → Model Training → Model Serving API → Application. During review, a CPMAI-certified reviewer flags the diagram as incomplete for a production system. What is the MOST critical missing component?

A) A monitoring and feedback loop for model performance and drift
B) A data labeling annotation tool
C) A second redundant training pipeline
D) A data visualization dashboard for executives

<details>
<summary>Answer</summary>

**Correct: A**

A production AI architecture must include a monitoring/feedback loop to detect model drift, capture new labeled data, and trigger retraining — without it, the model degrades silently over time and there is no operationalization closure.

**Why the others are wrong:**
- A labeling tool may be needed upstream during data preparation but is not the critical missing piece for a live production architecture.
- Redundant training pipelines address availability, not the core operational gap being tested here.
- Executive dashboards are a reporting nicety, not a structural requirement of the solution architecture.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** An AI project's success threshold was defined solely as 'model accuracy above 90%.' Six months after deployment, the model hits 93% accuracy, but the business sees no reduction in operational costs. What is the BEST explanation for this outcome?

A) The model needs to be retrained on more recent data
B) 93% accuracy is not statistically significant
C) The KPI was a technical metric, not tied to a measurable business outcome
D) The data science team used the wrong evaluation metric

<details>
<summary>Answer</summary>

**Correct: C**

CPMAI emphasizes that KPIs must link model performance metrics to measurable business outcomes (cost reduction, revenue, cycle time). A purely technical accuracy threshold with no tie to a business KPI can be 'successful' technically while delivering zero business value.

**Why the others are wrong:**
- Retraining addresses model drift, not the disconnect between technical and business metrics described here.
- 93% is a reasonably strong accuracy figure; statistical significance is not the issue in this scenario.
- The scenario doesn't indicate the evaluation metric itself was wrong, only that it wasn't connected to a business result.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** During resourcing planning, a project team has data scientists to build models but no one to build and maintain the pipelines that move data from source systems into the training environment. Which type of resource gap does this represent?

A) A data science skill gap
B) An executive sponsorship gap
C) A data engineering skill gap
D) A change management gap

<details>
<summary>Answer</summary>

**Correct: C**

Building and maintaining ETL/data pipelines is a data engineering function, distinct from data science (modeling). CPMAI explicitly separates these roles when identifying resource/skill gaps.

**Why the others are wrong:**
- Data science skills already exist per the scenario; the gap is specifically in pipeline/infrastructure work.
- Executive sponsorship refers to leadership buy-in and funding, not technical pipeline work.
- Change management concerns user adoption, not the missing technical role described.

</details>

---

**Q6.** A company must decide between purchasing a third-party AI vendor solution versus building a custom model in-house. Which combination of factors should MOST heavily drive the TCO comparison?

A) Only the upfront licensing fee versus the initial development cost
B) Which option has the newest underlying model architecture
C) Compute, labor, data preparation, integration, and ongoing maintenance costs for both options over the same time horizon
D) Which option the executive sponsor personally prefers

<details>
<summary>Answer</summary>

**Correct: C**

A valid TCO comparison requires evaluating all major cost components — compute, labor, data acquisition/prep, integration, and maintenance — across an equivalent time horizon for both build and buy options.

**Why the others are wrong:**
- Comparing only upfront costs ignores recurring costs and understates true TCO, a classic exam trap.
- Model architecture novelty is a technical detail, not a financial TCO driver.
- Personal preference is not a valid business case or TCO input.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** In an AI project business case, which formula correctly represents Return on Investment (ROI)?

A) ROI = Total Cost of Ownership / Project Duration
B) ROI = Model Accuracy × Data Volume
C) ROI = (Net Benefit − Cost) / Cost
D) ROI = Number of Users Adopting the Tool / Total Employees

<details>
<summary>Answer</summary>

**Correct: C**

ROI is standardly calculated as (Net Benefit minus Cost) divided by Cost, expressed as a percentage — this is the formula tested for building the AI business case narrative.

**Why the others are wrong:**
- This describes a cost-per-time-unit metric, not ROI.
- This conflates unrelated technical metrics and is not a financial formula.
- This describes an adoption rate, which is a change management KPI, not ROI.

</details>

---

**Q8.** A project sponsor asks the AI project team to include a labor cost estimate in the TCO for the first year. Which set of roles should be included in that labor estimate for a typical enterprise AI initiative?

A) Only data scientists who build the model
B) Data scientists, data engineers, ML/DevOps engineers, and business analysts supporting change management
C) Only the executive sponsor and project manager
D) Only contractors hired for data labeling

<details>
<summary>Answer</summary>

**Correct: B**

A complete AI labor TCO spans the full cross-functional team: data scientists (modeling), data engineers (pipelines), ML/DevOps engineers (deployment/monitoring), and business analysts supporting adoption and change management.

**Why the others are wrong:**
- Limiting to data scientists ignores pipeline, deployment, and adoption labor, understating TCO.
- Sponsor and PM costs alone omit the technical delivery team entirely.
- Labeling contractors are only one data-acquisition-related labor line item, not the full picture.

</details>

---

