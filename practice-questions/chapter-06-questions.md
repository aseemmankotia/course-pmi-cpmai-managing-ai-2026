## Chapter 6: AI Workspace, Infrastructure, and Data Gathering — Practice Questions

**Q1.** A healthcare AI project team must provision a development environment to build a diagnostic model using electronic health records (EHR) containing PHI. The team needs data scientists to explore and engineer features quickly. Which approach BEST balances secure development access with team productivity?

A) Grant all data scientists direct production database credentials so they can query live PHI instantly
B) Have the compliance team manually export data via email whenever a data scientist requests it
C) Skip environment provisioning and let each data scientist copy files to personal laptops for offline analysis
D) Provision an isolated sandbox environment with de-identified or masked EHR data, with logging and least-privilege access

<details>
<summary>Answer</summary>

**Correct: D**

A sandbox with masked data and least-privilege, logged access lets teams work efficiently while containing exposure of sensitive PHI — the core goal of secure dev environment provisioning.

**Why the others are wrong:**
- Direct production credentials expose live PHI unnecessarily and violate least-privilege principles.
- Manual ad hoc exports don't scale, create audit gaps, and still move raw PHI insecurely.
- Local laptop copies remove data from controlled infrastructure entirely, a major compliance violation.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** An AI initiative will ingest structured transactional data, unstructured social media text, and image files, all of which must be stored in native format before a schema is applied for downstream model training. Which storage architecture is the BEST fit?

A) Traditional relational data warehouse
B) Flat file server with a manual folder structure
C) In-memory cache only
D) Data lake

<details>
<summary>Answer</summary>

**Correct: D**

A data lake supports schema-on-read and can hold structured, semi-structured, and unstructured data in native format, which is exactly what mixed-type AI training data requires.

**Why the others are wrong:**
- Data warehouses require schema-on-write and are optimized for structured data only.
- A flat file server lacks governance, metadata, and scalability needed for AI pipelines.
- In-memory cache is volatile and meant for temporary speed, not durable storage.

</details>

---

**Q3.** A data engineering team uses Git for code but needs to track changes to large training datasets (multi-GB CSV and image files) alongside model code without bloating the Git repository. Which tool should be configured alongside Git to manage this?

A) SVN (Subversion) as a full replacement for Git
B) DVC (Data Version Control) or Git LFS
C) A shared network drive with manual file naming (v1, v2, v3)
D) Copying the entire dataset directly into the Git repository

<details>
<summary>Answer</summary>

**Correct: B**

DVC or Git LFS are purpose-built to version large binary/data files by storing pointers in Git while keeping actual data outside the repo, solving the bloat problem.

**Why the others are wrong:**
- SVN doesn't solve the large-file problem and abandons the team's existing Git workflow unnecessarily.
- Manual naming on a shared drive provides no real version history or conflict handling.
- Committing large files directly into Git bloats the repo and slows every clone/pull operation.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A fraud detection AI system must score transactions within seconds of occurrence to block fraudulent purchases in real time. Which data refresh/ingestion approach is required?

A) A nightly batch ETL job loading the previous day's transactions
B) A weekly full data warehouse refresh
C) A streaming/real-time ingestion pipeline with continuous data feed
D) A manual quarterly data extraction and refresh

<details>
<summary>Answer</summary>

**Correct: C**

Real-time fraud scoring requires data to arrive continuously with minimal latency, which only a streaming ingestion pipeline provides.

**Why the others are wrong:**
- Nightly batch loads data a day late, missing in-the-moment fraud events.
- Weekly refresh is far too infrequent for a real-time use case.
- Quarterly extraction is orders of magnitude too slow for transaction-level fraud detection.

</details>

---

**Q5.** In the context of gathering data for an AI project, 'completeness validation' primarily refers to which activity?

A) Verifying the data's statistical distribution matches expected business KPIs
B) Ensuring the trained model's accuracy exceeds a target threshold
C) Confirming that all expected records, fields, and value ranges are present without missing data beyond an acceptable threshold
D) Verifying that data is encrypted both at rest and in transit

<details>
<summary>Answer</summary>

**Correct: C**

Completeness validation is a data-gathering quality check confirming that expected records and fields exist and missing data stays within acceptable limits.

**Why the others are wrong:**
- Distribution alignment relates to data validity/representativeness, a different data quality dimension.
- Model accuracy is a modeling/evaluation concern, not a data-gathering completeness check.
- Encryption is a security control, unrelated to whether data is complete.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A team is training a deep convolutional neural network on millions of high-resolution images. Which compute provisioning choice BEST supports this workload?

A) A single CPU-based virtual machine with 4 vCPUs
B) A serverless function with a small fixed memory limit
C) A shared low-power edge device
D) A cluster of GPU-accelerated compute instances

<details>
<summary>Answer</summary>

**Correct: D**

Deep learning on large image datasets relies on massively parallel matrix operations, which GPU clusters are purpose-built to accelerate.

**Why the others are wrong:**
- A 4-vCPU VM lacks the parallel throughput needed for large-scale deep learning training.
- Small serverless functions are memory/time-constrained and unsuited for heavy training jobs.
- Low-power edge devices are meant for inference at the edge, not large-scale model training.

</details>

---

**Q7.** An AI workspace has highly variable, unpredictable compute demand — heavy usage during model training sprints, near-zero usage between sprints. Which compute provisioning strategy minimizes cost while meeting demand?

A) Purchase and maintain a fixed on-premises GPU cluster sized for peak demand
B) Provision elastic, on-demand cloud compute that scales up during training and down afterward
C) Use a single dedicated always-on physical server sized for average demand
D) Avoid provisioning compute and rely solely on data scientists' laptops

<details>
<summary>Answer</summary>

**Correct: B**

Elastic cloud compute scales to match bursty, unpredictable demand, avoiding the cost of idle capacity while still meeting peak training needs.

**Why the others are wrong:**
- A fixed on-prem cluster sized for peak demand sits idle (and wastes capital) between sprints.
- A server sized for average demand will bottleneck during peak training sprints.
- Laptops cannot handle enterprise-scale AI training workloads reliably or securely.

</details>

---

**Q8.** After extracting a dataset from a source production system into the AI workspace, which technique should be used FIRST to validate completeness of the transfer?

A) Train a baseline model and check its accuracy
B) Ask business stakeholders if the data 'looks right'
C) Reconcile record counts and checksums between source and destination
D) Immediately begin feature engineering

<details>
<summary>Answer</summary>

**Correct: C**

Reconciling record counts and checksums directly confirms whether the transfer moved all expected data intact, the definition of a completeness check.

**Why the others are wrong:**
- Model accuracy is measured much later and does not validate whether the extraction itself was complete.
- Subjective stakeholder impressions are not a reliable or repeatable validation technique.
- Feature engineering assumes the data is already validated, skipping a required prerequisite step.

</details>

---

