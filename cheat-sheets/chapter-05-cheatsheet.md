## Chapter 5 Cheat Sheet: Defining Data Needs & Mapping Data Sources

**Exam Domain:** Identify Data Needs — **Weight: 26%**

### Data Requirement Dimensions
| Dimension | What It Defines | Exam Trap |
|---|---|---|
| Type | Structured, semi-structured, unstructured | Confusing 'format' with 'type' |
| Format | CSV, JSON, EBCDIC, Parquet, etc. | Assuming format = quality |
| Volume | Total size / expected growth | Ignoring growth rate in scenario |
| Sampling | Method to select representative subset | Using random sampling on imbalanced data |
| Temporal | Freshness, latency, historical depth | Matching wrong granularity to decision window |
| Granularity | Level of detail (transaction vs. aggregate) | Aggregating too coarsely for the use case |

### Data Quality Dimensions
| Dimension | Definition |
|---|---|
| Completeness | Required values are present |
| Validity | Values conform to defined format/range |
| Timeliness | Data is current when needed |
| Uniqueness | No unwanted duplicate records |
| Consistency | Same value/format across systems |
| Accuracy | Values correctly reflect real-world state |

### Roles & Responsibilities
| Role | Responsibility | Level |
|---|---|---|
| Data Owner | Accountable for business use, authorizes access | Strategic |
| Data Steward | Manages definitions, quality, metadata day-to-day | Operational |
| Data SME | Deep knowledge of specific source/system semantics | Tactical |
| Governance Team | Sets enterprise-wide policy, compliance, retention rules | Policy |

### Data Source Categories
| Category | Examples | Key Consideration |
|---|---|---|
| Internal | Data warehouses, CRM, ERP, operational DBs | Known schema, but siloed ownership |
| External/Third-Party | Syndicated market data, purchased feeds | Licensing, refresh cadence, usage rights |
| Cloud Repositories | Data lakes, SaaS platforms, cloud DBs | Access permissions, egress considerations |
| Legacy Archives | Mainframes, flat files, EBCDIC extracts | Often undocumented — requires SME involvement |

### Granularity vs. Decision Window Rule
Capture data at a granularity **finer** than the prediction/decision window (e.g., daily data for a 30-day churn model). Aggregating to or beyond the window's timescale hides the signals needed for prediction.

### Sampling Rule for Imbalanced Data
Use **stratified sampling with oversampling** of the minority class for rare-event problems (fraud, churn, defects). Simple random sampling is the most common wrong answer in these scenarios.

### Six V's of Big Data
Volume, Velocity, Variety, Veracity, Value, Variability — Veracity = trustworthiness of data, commonly confused with Validity (format/range conformance).

### Quick Decision Checklist
1. What type/format is the data in?
2. What volume and growth rate?
3. What temporal freshness and historical depth are required?
4. What granularity matches the decision window?
5. Who is the SME/Steward/Owner for this source?
6. Are there licensing or governance constraints on access/use?
