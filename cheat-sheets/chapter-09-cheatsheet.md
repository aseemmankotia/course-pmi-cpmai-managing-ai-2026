# Chapter 9 Cheat Sheet: Training Management, Data Prep & the Two Gates

## The Two Go/No-Go Gates

| Gate | Positioned Between | Verifies | Does NOT Verify |
|---|---|---|---|
| Gate 1 — Data Quality | Data Preparation → Data Modeling | Completeness, consistency, accuracy, representativeness, valid labels | Model performance, robustness |
| Gate 2 — Operationalization Readiness | Model Evaluation → Operationalization | Performance vs. threshold, robustness, generalization, documented approval | Raw data cleanliness (already handled at gate 1) |

**Exam rule of thumb:** Gate 1 = data readiness. Gate 2 = model + governance readiness. A model can score high accuracy and STILL fail gate 2 if robustness or sign-off is missing.

## Data Preparation Activities (pre-gate 1)
- Cleaning: handle missing values, remove duplicates, fix inconsistent formats
- Feature engineering: derive new variables, encode categoricals, normalize/scale
- Normalization: rescale numeric ranges so no feature dominates due to scale
- Augmentation: transform existing real data (rotate, crop, add noise) to expand dataset
- Synthetic data: generate wholly new artificial records (simulation, GAN) when real data is scarce

## Augmentation vs. Synthetic Data

| | Data Augmentation | Synthetic Data |
|---|---|---|
| Basis | Modifies real records | Creates new artificial records |
| Use case | Expand variety of existing data | Fill gaps where real data doesn't exist/impractical to collect |
| Risk | May not capture truly novel scenarios | May not fully reflect real-world distribution |

## Cross-Validation Oversight

| Scenario | Correct Strategy | Wrong Choice (Trap) |
|---|---|---|
| i.i.d. tabular/image data | Random k-fold (k=5 or 10 common) | N/A |
| Time-series / sequential data | Forward-chaining / rolling-window split | Random k-fold (causes leakage) |
| Small dataset | Higher k or leave-one-out | Single train/test split (high variance) |

## Experiment Tracking — Minimum Log Fields
1. Code version (commit hash)
2. Data version (dataset snapshot ID)
3. Hyperparameters used
4. Random seed
5. Environment/dependency versions
6. Resulting metrics

**Missing any one field breaks full reproducibility — a heavily tested concept.**

## Compute & Hyperparameter Tuning Oversight
- Set a compute budget ceiling before tuning starts.
- If validation performance plateaus across many trials → apply early stopping, select best-so-far config.
- Expanding search space after a plateau typically wastes compute, not improves results.

## Gate 2 Checklist (all four required)
- [ ] Performance meets defined threshold
- [ ] Robustness confirmed (edge cases, noisy/adversarial input, distribution shift)
- [ ] Generalization confirmed (holdout / production-representative data)
- [ ] Documented stakeholder sign-off recorded

## Common Exam Traps
- Assuming high test accuracy alone clears gate 2 (it doesn't — robustness + sign-off also required).
- Using random k-fold CV on time-series data (causes leakage).
- Confusing model versioning with data versioning (both needed for reproducibility).
- Treating augmentation and synthetic data generation as identical techniques.
