## Chapter 7: Data Evaluation, Compliance, and the Data Go/No-Go Decision — Practice Questions

**Q1.** A CPMAI project team is evaluating a third-party dataset scraped from public social media profiles to train a sentiment model. The dataset includes usernames and location metadata. What should the team do BEFORE proceeding to the Data Preparation phase?

A) Proceed immediately since the data is publicly available and therefore not subject to privacy restrictions
B) Anonymize the data after model training to reduce risk
C) Conduct a privacy and licensing review to confirm consent, terms-of-service compliance, and applicable regulations such as GDPR/CCPA before using the data
D) Delegate the privacy review to the data science team only, since compliance is not part of Data Understanding

<details>
<summary>Answer</summary>

**Correct: C**

CPMAI requires a documented privacy, licensing, and compliance check as part of the Data Understanding phase and the go/no-go gate — public availability does not exempt data from privacy law or platform terms of service.

**Why the others are wrong:**
- Public availability does not equal legal permission to use for AI training; scraping may violate platform ToS or privacy regulations regardless of visibility
- Anonymizing after training does not remove the risk already incurred during collection and processing, and re-identification risk may persist
- Compliance review is a cross-functional responsibility including legal, business, and data governance stakeholders — not solely the data science team

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** During exploratory data analysis, a team finds that 92% of records in a customer churn dataset are complete, but a histogram reveals that 'account tenure' values cluster unnaturally at exactly 0, 30, 60, and 90 — with almost no values in between. This pattern most directly indicates a problem with which data quality dimension?

A) Completeness
B) Accuracy
C) Timeliness
D) Consistency

<details>
<summary>Answer</summary>

**Correct: B**

Unnatural clustering at round numbers suggests the values were estimated, rounded, or defaulted rather than measured correctly, which is an accuracy problem — the data does not correctly reflect the real-world value.

**Why the others are wrong:**
- Completeness refers to missing values, not the correctness of values that are present
- Timeliness concerns whether data is current/up-to-date, unrelated to value distribution artifacts
- Consistency refers to whether the same data is represented uniformly across sources/records, not whether individual values are correct

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** Which technique would BEST help a CPMAI practitioner detect bias in a training dataset intended to predict loan approvals?

A) Calculating the mean and standard deviation of the loan amount field
B) Comparing the distribution of approval outcomes across demographic subgroups (e.g., by age, gender, ZIP code) to identify disproportionate representation or outcome gaps
C) Checking for duplicate rows in the dataset
D) Verifying that all currency fields use the same decimal format

<details>
<summary>Answer</summary>

**Correct: B**

Bias/gap analysis compares subgroup distributions and outcomes to reveal underrepresentation or disparate impact, which is the core exploratory technique for detecting bias before model training.

**Why the others are wrong:**
- Mean/standard deviation summarizes a single numeric field but does not reveal subgroup disparities
- Duplicate detection is a data quality (uniqueness) check, not a bias detection technique
- Format consistency is a data quality/consistency check unrelated to bias

</details>

---

**Q4.** A team is performing EDA on a new IoT sensor dataset before deciding whether to proceed with model development. Which EDA technique should they use FIRST to understand the overall shape and quality of the data at a glance?

A) Building a full predictive model and evaluating accuracy
B) Deploying the model to a staging environment
C) Generating summary statistics and visualizations (histograms, box plots, missing-value heatmaps) to profile distributions, outliers, and gaps
D) Writing the final business report for leadership

<details>
<summary>Answer</summary>

**Correct: C**

Data profiling via summary statistics and visualizations is the standard first step of EDA, allowing the team to assess distributions, outliers, and missingness before any modeling occurs.

**Why the others are wrong:**
- Building a model requires clean, understood data first — modeling is a later CPMAI phase, not an EDA step
- Deployment happens only after modeling and evaluation are complete, far downstream of EDA
- Reporting to leadership should be informed by EDA findings, not precede them

</details>

---

**Q5.** A CPMAI project's Data Understanding phase reveals that the only available dataset for a proposed fraud-detection AI project is 3 years old, has significant demographic gaps, and includes personally identifiable information without documented consent. What is the correct go/no-go decision?

A) Go — proceed to Data Preparation since fraud data is inherently valuable regardless of age or consent
B) Go — proceed but skip the modeling evaluation phase to save time
C) No-Go — cancel the entire AI initiative permanently
D) No-Go — halt or redefine the project scope until data quality, currency, bias, and compliance issues are resolved or an alternative data source is identified

<details>
<summary>Answer</summary>

**Correct: D**

The go/no-go gate exists precisely to stop projects when data quality (timeliness, gaps) and compliance (undocumented consent) issues would create unacceptable risk; the correct action is to pause and remediate or find alternate sources, not proceed or fully cancel.

**Why the others are wrong:**
- Proceeding ignores multiple identified red flags that the go/no-go gate is designed to catch
- Skipping evaluation does not address the root data problems and increases downstream risk
- Permanent cancellation is an overreaction; the framework calls for redefining scope or sourcing better data, not ending the initiative outright

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** Which pair of data quality dimensions is correctly matched to its definition?

A) Completeness = data is free of duplicate records; Consistency = data has no missing values
B) Timeliness = data is formatted uniformly across systems; Accuracy = data has no missing fields
C) Accuracy = data correctly reflects the real-world value it represents; Timeliness = data is current and available when needed
D) Consistency = data is up to date; Completeness = data matches source-of-truth values

<details>
<summary>Answer</summary>

**Correct: C**

Accuracy measures correctness against real-world truth, and timeliness measures currency/availability at the point of need — these are the standard CPMAI definitions.

**Why the others are wrong:**
- Completeness relates to missing values, not duplicates; consistency relates to uniform representation, not missingness
- Timeliness is about currency, not formatting; accuracy is about correctness, not missing fields
- Consistency is about uniform representation across sources, not recency; completeness is about missing data, not matching source-of-truth (that's accuracy)

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A data science team needs to present EDA findings to non-technical executives to support a go/no-go decision. Which approach BEST aligns with CPMAI guidance for conveying data understanding to leadership?

A) Translate findings into business-relevant impacts (e.g., 'missing data in 40% of customer records limits accurate churn prediction for one-third of our customer base') and tie them to project risk and cost
B) Present the full statistical output including p-values, correlation matrices, and raw code so leadership sees all technical detail
C) Avoid discussing data quality issues to prevent delaying project approval
D) Ask leadership to review the raw dataset directly so they can form their own technical conclusions

<details>
<summary>Answer</summary>

**Correct: A**

CPMAI emphasizes translating technical data findings into business language that ties directly to risk, cost, and decision-making relevance for non-technical stakeholders.

**Why the others are wrong:**
- Raw statistical detail overwhelms non-technical audiences and obscures the business implications needed for a decision
- Withholding known data issues undermines informed go/no-go decision-making and violates transparency principles
- Executives generally lack the technical background to interpret raw datasets; this abdicates the analyst's translation responsibility

</details>

---

**Q8.** A retail company wants to use two years of sales transaction data to train a demand-forecasting model. During EDA, the team discovers that store location codes were renamed six months ago, causing the same physical store to appear as two different entities in the dataset. This is an example of a problem with which data quality dimension?

A) Timeliness
B) Consistency
C) Accuracy
D) Completeness

<details>
<summary>Answer</summary>

**Correct: B**

The same real-world entity being represented differently across records (old vs. new store codes) is a classic consistency problem, since the data lacks uniform representation over time.

**Why the others are wrong:**
- Timeliness concerns whether data is current, not whether representations are uniform
- Accuracy concerns whether individual values are correct, but here each code was correct at the time it was recorded — the issue is representation mismatch
- Completeness concerns missing values, not conflicting representations of the same entity

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

