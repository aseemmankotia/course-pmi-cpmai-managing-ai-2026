## Chapter 8: Model Technique Selection and QA/QC — Practice Questions

**Q1.** A company wants to identify fraudulent transactions but has no historical examples labeled as 'fraud' or 'legitimate.' Which learning approach is MOST appropriate?

A) Unsupervised learning using anomaly detection
B) Supervised learning using historical fraud labels
C) Reinforcement learning with a reward signal
D) Semi-supervised learning requiring partial labels

<details>
<summary>Answer</summary>

**Correct: A**

With no labeled data, unsupervised anomaly detection identifies outliers/unusual patterns without needing predefined fraud/non-fraud labels.

**Why the others are wrong:**
- Supervised learning requires labeled outcomes, which do not exist in this scenario.
- Reinforcement learning needs an environment and reward signal for sequential decisions, not suited to static historical transaction data.
- Semi-supervised still requires at least some labeled examples, which are unavailable here.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A regulated healthcare AI project requires the project team to explain every model decision to clinicians and regulators. Which trade-off should be prioritized over raw predictive accuracy?

A) Model complexity
B) Interpretability
C) Training speed
D) Data volume

<details>
<summary>Answer</summary>

**Correct: B**

Regulatory and clinical trust require explainable outputs, so interpretability must be weighted higher than marginal performance gains.

**Why the others are wrong:**
- Complexity typically REDUCES interpretability, so it should not be prioritized here.
- Training speed is an engineering concern, not a compliance/trust concern.
- Data volume does not address the explainability requirement.

</details>

---

**Q3.** A team must train a robotic arm to optimize its pick-and-place sequence through trial and error, receiving feedback only after each attempt. Which learning paradigm is BEST suited?

A) Supervised learning
B) Unsupervised learning
C) Reinforcement learning
D) Deep learning classification

<details>
<summary>Answer</summary>

**Correct: C**

Reinforcement learning is defined by an agent learning optimal sequential actions via trial-and-error and reward/penalty feedback from an environment.

**Why the others are wrong:**
- Supervised learning requires a labeled dataset of 'correct' actions for every scenario, which does not exist here.
- Unsupervised learning discovers patterns/clusters; it does not optimize sequential control actions.
- Deep learning classification is a technique, not a learning paradigm, and does not inherently learn via trial-and-error reward feedback.

</details>

---

**Q4.** A data science team retrains a fraud model weekly with changing hyperparameters. Which configuration management practice is MOST critical for reproducibility and audit?

A) Using the same random seed every time
B) Only saving the final trained model file
C) Documenting hyperparameters in a manually updated shared spreadsheet
D) Version-controlling datasets, code, hyperparameters, and model artifacts together

<details>
<summary>Answer</summary>

**Correct: D**

Full lineage tracking — linking dataset version, code, hyperparameters, and the resulting model artifact — is required to reproduce and audit any given model version.

**Why the others are wrong:**
- A fixed seed alone does not capture data or code version changes.
- Saving only the final model discards the ability to reproduce or audit the training process.
- A manually updated spreadsheet is error-prone and disconnected from the actual pipeline, risking drift between documentation and reality.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A project manager reviews QA/QC results showing a deep neural network trained on 500 employee records achieved 95% training accuracy but only 60% test accuracy. What is the MOST likely issue?

A) Overfitting due to excessive model complexity for the dataset size
B) Underfitting due to insufficient model complexity
C) Data leakage in the test set
D) Incorrect evaluation metric selection

<details>
<summary>Answer</summary>

**Correct: A**

A large gap between high training accuracy and much lower test accuracy on a small dataset with a complex model is the classic signature of overfitting.

**Why the others are wrong:**
- Underfitting produces poor accuracy on BOTH training and test sets, the opposite pattern described.
- Data leakage typically produces artificially HIGH test accuracy, not low, so it does not match this symptom.
- Metric selection issues would not create this specific train/test accuracy gap pattern.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** In the CPMAI methodology, which phase(s) encompass model technique selection and QA/QC testing protocols?

A) Business Understanding and Data Understanding
B) Data Modeling (Model Development) and Model Evaluation
C) Data Preparation only
D) Operationalization and Maintenance

<details>
<summary>Answer</summary>

**Correct: B**

Technique selection occurs during the Data Modeling phase, and QA/QC testing/validation occurs during the Model Evaluation phase.

**Why the others are wrong:**
- Business and Data Understanding phases focus on requirements and data exploration, before modeling begins.
- Data Preparation covers cleaning and transforming data, prior to technique selection.
- Operationalization and Maintenance occur after the model has already been validated and deployed.

</details>

---

**Q7.** A project manager must choose between a linear regression model (R²=0.78) and a gradient-boosted ensemble (R²=0.91) for a sales forecast, and the board requires a clear explanation of which factors drive each prediction. What should the PM recommend?

A) Always select the gradient-boosted ensemble since it has higher performance
B) Select linear regression despite the lower R² because interpretability is a critical business requirement
C) Combine both models into a stacked ensemble to maximize performance
D) Reject both models and mandate the data scientists build only a decision tree

<details>
<summary>Answer</summary>

**Correct: B**

This reflects the complexity/performance/interpretability trade-off — when the business explicitly requires explainability, interpretability should outweigh a modest performance gain.

**Why the others are wrong:**
- Choosing the ensemble purely on performance ignores the explicit board requirement for explainability.
- Stacking increases complexity and further reduces interpretability, working against the stated requirement.
- Mandating a specific algorithm oversteps the PM's governance role and is an arbitrary constraint rather than addressing the trade-off principle.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which peer review practice is recommended by QA/QC best practices before promoting a model from staging to production?

A) A single data scientist self-certifies that the model meets requirements
B) Skip review if training accuracy exceeds 90%
C) An independent reviewer or review board validates performance, bias testing results, and documentation against acceptance criteria
D) Rely solely on automated CI/CD pipeline tests without human review

<details>
<summary>Answer</summary>

**Correct: C**

Independent validation against pre-defined acceptance criteria reduces conflict of interest and ensures performance, bias/fairness, and documentation are properly reviewed before production release.

**Why the others are wrong:**
- Self-certification by the model's own developer lacks independent oversight and is a common exam distractor.
- Training accuracy alone ignores bias, fairness, and robustness testing requirements.
- Automated tests are necessary but not sufficient — human judgment is needed to assess documentation completeness and edge cases.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

