## Chapter 9: Training Management, Data Preparation, and the Two Go/No-Go Gates — Practice Questions

**Q1.** A project team has completed missing-value imputation, outlier treatment, feature engineering, and confirmed that the training dataset's distribution matches the target production population. No modeling has occurred yet. According to CPMAI go/no-go gate practice, what should happen next?

A) Withhold gate 1 approval until a baseline model achieves the target accuracy
B) Withhold gate 1 approval until robustness testing against adversarial inputs is complete
C) Skip gate 1 entirely since data preparation activities were already performed
D) Proceed to gate 1 approval and move into the Data Modeling phase

<details>
<summary>Answer</summary>

**Correct: D**

Gate 1 verifies that data is clean, representative, and appropriately engineered BEFORE modeling starts — none of its criteria depend on model performance.

**Why the others are wrong:**
- Model accuracy is a gate 2 (operationalization) criterion, not a gate 1 data-quality criterion.
- Adversarial/robustness testing is a gate 2 activity performed on a trained model, not a data-preparation deliverable.
- Go/no-go gates are mandatory checkpoints in CPMAI iterative methodology and cannot be skipped even if work appears complete.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A model achieves 96% accuracy on the held-out test set. Documentation shows no evaluation against edge cases, noisy inputs, or distribution-shifted data, and no stakeholder sign-off has been recorded. Should this model pass go/no-go gate 2?

A) No, because robustness/generalization evidence and documented approval are both missing
B) Yes, because 96% accuracy exceeds most business thresholds
C) Yes, because test set performance is the only requirement for operationalization
D) No, because the data preparation phase must be redone before any gate 2 review

<details>
<summary>Answer</summary>

**Correct: A**

Gate 2 requires four elements: performance, robustness, generalization, AND documented approval — accuracy alone is insufficient.

**Why the others are wrong:**
- High accuracy alone does not satisfy robustness or governance requirements of gate 2.
- Gate 2 explicitly requires more than a single performance metric — this is a classic exam trap.
- The issue described is a gate 2 deficiency, not a data preparation defect; re-running gate 1 is unnecessary.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A team has very few labeled examples of a rare equipment-failure event needed to train a fault-detection classifier, and collecting more real failure events is impractical within the project timeline. Which approach BEST addresses this at the data preparation stage?

A) Increase the learning rate to help the model learn faster from limited examples
B) Generate synthetic failure examples using techniques such as simulation or generative models
C) Remove the failure class entirely and reframe the problem as unsupervised anomaly detection with no oversight
D) Proceed with training as-is and rely on cross-validation to correct the imbalance

<details>
<summary>Answer</summary>

**Correct: B**

Synthetic data generation (or simulation/GAN-based methods) is the standard way to address severe class scarcity when real-world data collection is impractical.

**Why the others are wrong:**
- Learning rate is a training hyperparameter and does not address a data scarcity problem.
- Reframing without stakeholder/PM oversight abandons the original business requirement instead of solving the data gap.
- Cross-validation evaluates model performance; it does not create additional minority-class data or fix imbalance.

</details>

---

**Q4.** A team is building a demand-forecasting model using three years of monthly sales data. Which cross-validation strategy is MOST appropriate?

A) Time-series (forward-chaining/rolling-window) cross-validation
B) Random 10-fold cross-validation with shuffled data
C) Leave-one-out cross-validation on individual rows
D) A single random 80/20 train/test split with shuffling

<details>
<summary>Answer</summary>

**Correct: A**

Time-series data requires chronological splits so future data never leaks into training; forward-chaining validation preserves this order.

**Why the others are wrong:**
- Random k-fold shuffling allows future observations into the training set, causing data leakage and overly optimistic results.
- Leave-one-out is computationally expensive and still ignores temporal ordering, causing the same leakage problem.
- A shuffled random split has the same leakage issue as random k-fold and is not suitable for temporal data.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** For an AI project to be fully reproducible, which combination of elements must an experiment tracking system capture at minimum?

A) Only the final trained model file and its accuracy score
B) Only the hyperparameters used during the best training run
C) Business requirements document and stakeholder sign-off email
D) Code version, dataset version, hyperparameters, random seed, and environment/dependency versions

<details>
<summary>Answer</summary>

**Correct: D**

Reproducibility requires linking the exact code, data snapshot, configuration (hyperparameters/seed), and runtime environment used to produce a given result.

**Why the others are wrong:**
- The model file and score alone cannot recreate the training process if the code or data changes later.
- Hyperparameters without data and code versioning cannot guarantee the same result is reproducible.
- Governance sign-off is part of gate 2 documentation, not the technical reproducibility record for experiment tracking.

</details>

---

**Q6.** A hyperparameter tuning job has run for several days, consuming a large share of the allocated compute budget, while validation performance has plateaued for the last dozen trials. As the AI project manager overseeing compute utilization, what is the BEST action?

A) Let the job continue indefinitely to guarantee the absolute best possible configuration
B) Apply an early-stopping/budget cutoff and select the best configuration found so far
C) Immediately delete the experiment and restart tuning from scratch with new random hyperparameters
D) Increase the search space to include more hyperparameters to force further improvement

<details>
<summary>Answer</summary>

**Correct: B**

When validation performance plateaus, enforcing a compute budget cutoff and selecting the best result balances resource cost against diminishing returns — a core PM responsibility.

**Why the others are wrong:**
- Continuing indefinitely wastes compute budget for negligible or no performance gain.
- Restarting from scratch discards useful trial history and wastes the compute already invested.
- Expanding the search space when performance has plateaued typically increases cost without improving results.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** What is the key difference between data augmentation and synthetic data generation?

A) Augmentation creates entirely new artificial records; synthetic generation only relabels existing records
B) There is no meaningful difference; the terms are interchangeable in AI project management
C) Augmentation transforms existing real data (e.g., rotation, noise injection); synthetic data generation creates new artificial data points not directly derived from a single real record
D) Augmentation is used only for text data, while synthetic generation is used only for images

<details>
<summary>Answer</summary>

**Correct: C**

Augmentation modifies existing real samples to increase dataset variety, while synthetic data generation (e.g., GANs, simulations) produces novel data representing scenarios that may not exist in the real dataset at all.

**Why the others are wrong:**
- This reverses the actual definitions of the two techniques.
- The terms describe distinct techniques with different use cases and cannot be treated as identical on the exam.
- Both techniques apply across data modalities (text, image, tabular, etc.), not restricted to one type each.

</details>

---

**Q8.** A data scientist reports that retraining the same model on the identical dataset and identical hyperparameters produces noticeably different accuracy results each run. What is the MOST likely root cause?

A) Unseeded randomness or non-deterministic operations (e.g., unset random seed, GPU non-determinism) in the training pipeline
B) The go/no-go gate 1 criteria were not met
C) The model was deployed to production before evaluation was complete
D) The dataset was augmented using synthetic data techniques

<details>
<summary>Answer</summary>

**Correct: A**

Variability in results with identical data and hyperparameters points to unseeded randomness (initialization, shuffling, or GPU nondeterminism) that breaks reproducibility.

**Why the others are wrong:**
- Gate 1 concerns data quality prior to modeling; it does not explain run-to-run training variance.
- Deployment status is unrelated to inconsistent results during training/evaluation.
- Synthetic data augmentation affects dataset composition, not run-to-run variance given otherwise identical inputs and settings.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

