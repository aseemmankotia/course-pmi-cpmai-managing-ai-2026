## Chapter 5: Defining Data Needs and Mapping Data Sources — Practice Questions

**Q1.** An AI project team is combining internal CRM records, external syndicated market data, a cloud data lake, and legacy mainframe extracts to build a customer-churn model. The customer ID field is inconsistent across systems. Which role should the team engage FIRST to resolve the authoritative definition and format of customer ID?

A) Data Scientist
B) Data Steward
C) Executive Sponsor
D) IT Help Desk

<details>
<summary>Answer</summary>

**Correct: B**

The data steward has operational ownership of data definitions, quality rules, and metadata, making them the correct resource to reconcile inconsistent field definitions across systems.

**Why the others are wrong:**
- The data scientist consumes the data for modeling but does not own or authoritatively define shared business entities.
- The executive sponsor provides funding and strategic direction, not operational data definitions.
- IT Help Desk resolves technical access/system issues, not data governance definitions.

</details>

---

**Q2.** The team must predict customer churn within a 30-day decision window. What granularity should the source data be captured at to best support this use case?

A) Aggregate all data to monthly summaries before analysis
B) Use only the most recent snapshot of customer data
C) Capture data at a granularity finer than the decision window, such as daily or transactional level
D) Convert all data to categorical bins regardless of source

<details>
<summary>Answer</summary>

**Correct: C**

Data must be captured at a granularity finer than the prediction window so leading indicators of churn are preserved rather than smoothed out by aggregation.

**Why the others are wrong:**
- Monthly aggregation is coarser than the 30-day window and hides the signals the model needs to detect early churn behavior.
- A single snapshot loses the temporal patterns needed to detect changes leading to churn.
- Arbitrary categorical binning discards the resolution needed for time-sensitive prediction, regardless of source system.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A fraud detection initiative requires near-real-time visibility into transactions as they occur. Which internal data source approach BEST meets this requirement?

A) Nightly batch load from the data warehouse
B) Quarterly export from the legacy archive
C) Change Data Capture (CDC) streaming from operational transactional systems
D) Manual CSV upload from business analysts

<details>
<summary>Answer</summary>

**Correct: C**

CDC captures incremental changes from operational systems as they happen, satisfying the near-real-time requirement for fraud detection.

**Why the others are wrong:**
- A nightly batch load introduces latency that is unacceptable for real-time fraud detection.
- Quarterly legacy exports are far too infrequent for a real-time use case.
- Manual uploads are slow, error-prone, and not scalable for continuous fraud monitoring.

</details>

---

**Q4.** A dataset for a fraud-classification model has very few labeled fraud cases compared to legitimate transactions. Which sampling approach should be used to build the training set?

A) Simple random sampling
B) Systematic sampling
C) Convenience sampling
D) Stratified sampling with oversampling of the minority class

<details>
<summary>Answer</summary>

**Correct: D**

Stratified sampling with oversampling ensures the rare fraud class is adequately represented in training, which is essential for imbalanced classification problems.

**Why the others are wrong:**
- Simple random sampling will likely underrepresent the rare fraud class, harming model performance.
- Systematic sampling selects at fixed intervals and does not correct for class imbalance.
- Convenience sampling introduces bias by relying on easily accessible data rather than a representative distribution.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which statement correctly distinguishes a data owner from a data steward during a data-needs assessment?

A) The data owner performs day-to-day data cleansing while the steward sets enterprise policy
B) The data owner is accountable for authorizing access and business use of the data, while the steward manages day-to-day definitions, quality, and stewardship of that data
C) The data owner and data steward are interchangeable titles for the same governance role
D) The data owner is always an IT role while the steward is always a business role

<details>
<summary>Answer</summary>

**Correct: B**

The owner holds business accountability and authorizes access/use, while the steward handles operational responsibilities like definitions, quality, and metadata management.

**Why the others are wrong:**
- This reverses the roles — cleansing/operational work is the steward's job, not the owner's.
- The two roles serve distinct functions (accountability vs. operational management) and are not interchangeable.
- Neither role is fixed to IT or business by definition; assignment depends on the organization's governance structure.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A legacy mainframe archive contains critical historical claims data in fixed-width EBCDIC format with no metadata catalog available. What should the team do FIRST?

A) Engage a subject matter expert (SME) familiar with the legacy system to document field layouts and definitions before ingestion
B) Ingest the raw EBCDIC file directly into the cloud data lake and let the AI model handle it
C) Discard the legacy data since it predates the current system
D) Ask the governance team to encrypt the file before any further action

<details>
<summary>Answer</summary>

**Correct: A**

Undocumented legacy data must be interpreted correctly before use; an SME can define field layouts and semantics, preventing misinterpretation during ingestion.

**Why the others are wrong:**
- Ingesting raw, undocumented, encoded data without understanding its structure risks corrupting the dataset with misparsed fields.
- Legacy data often holds valuable historical patterns and should not be discarded without evaluation.
- Encryption addresses security, not the immediate need to understand and correctly parse the data's structure.

</details>

---

**Q7.** Which data quality dimension addresses whether a value falls within a defined format, type, or allowable range (e.g., age between 0 and 120)?

A) Completeness
B) Timeliness
C) Validity
D) Uniqueness

<details>
<summary>Answer</summary>

**Correct: C**

Validity refers to data conforming to defined formats, types, or acceptable ranges.

**Why the others are wrong:**
- Completeness measures whether required data values are present, not whether they are within a valid range.
- Timeliness measures whether data is current and available when needed, not its format or range.
- Uniqueness measures whether duplicate records exist, unrelated to range/format constraints.

</details>

---

**Q8.** The team is acquiring third-party demographic data from an external vendor for an AI project. Which requirement should be defined EARLY in the data-needs process, beyond storage format?

A) Storage file format only
B) Compute cost of the AI training pipeline
C) Licensing terms, usage rights, and data refresh/update frequency
D) The specific machine learning algorithm to be used

<details>
<summary>Answer</summary>

**Correct: C**

Third-party data requires clarity on licensing/usage rights and refresh cadence (a temporal requirement) to ensure legal compliance and data currency before it is integrated.

**Why the others are wrong:**
- File format is a technical detail but not the primary early concern with externally licensed data.
- Compute cost relates to the modeling phase, not identifying source data needs.
- Algorithm selection occurs later in the AI lifecycle, not during data-needs identification.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

