# Chapter 8 Cheat Sheet: Model Technique Selection & QA/QC
**Exam Domain:** Manage AI Model Development and Evaluation (16%) | **CPMAI Mapping:** Phase 4 (Data Modeling) + Phase 5 (Model Evaluation)

## Learning Paradigm Selection
| Paradigm | Data Needed | Best For | Key Trigger Words |
|---|---|---|---|
| Supervised | Labeled input/output pairs | Classification, regression, prediction from history | "historical labeled outcomes" |
| Unsupervised | No labels | Clustering, anomaly detection, dimensionality reduction | "no labels", "discover hidden structure" |
| Reinforcement | No labels, reward signal | Sequential decisions, control, optimization | "agent", "reward", "trial-and-error" |

## Complexity / Performance / Interpretability Trade-off
| Model Type | Complexity | Interpretability | Typical Performance |
|---|---|---|---|
| Linear/Logistic Regression | Low | High | Moderate |
| Decision Tree | Low-Med | High | Moderate |
| Random Forest / Gradient Boosting | Med-High | Low-Med | High |
| Deep Neural Network | High | Low | High (data-dependent) |
**Rule:** Regulated/high-stakes decisions (healthcare, finance, HR, legal) → prioritize interpretability even at some performance cost. The PM's job is to align technique choice with the BUSINESS requirement, not just the highest accuracy metric.

## PM Role in Technique Selection
- PM does NOT choose the algorithm.
- PM ensures the data science team's choice aligns with business constraints: explainability, latency, cost, regulatory risk.
- PM documents the RATIONALE for technique selection as part of governance.

## QA/QC Testing Protocol (Standard Sequence)
1. Split data: train / validation / test (common: 70/30, 80/20, or k-fold CV with k=5 or k=10)
2. Train model
3. Evaluate: accuracy, precision, recall, F1, AUC (choose metric matching business goal, e.g., recall for fraud/disease detection)
4. Bias/fairness testing across demographic or business subgroups
5. Robustness/adversarial/stress testing
6. Independent peer review vs. documented acceptance criteria

## Overfitting vs Underfitting (Exam Trap)
| Symptom | Diagnosis | Fix |
|---|---|---|
| High train acc, low test acc | Overfitting | Regularize, simplify model, add data, cross-validate |
| Low train acc, low test acc | Underfitting | Increase complexity, add features |

## Configuration Management Checklist
- Dataset version
- Code/algorithm version
- Hyperparameters + random seed
- Environment/dependency versions
- Resulting model artifact (in a model registry)
**Purpose:** reproducibility + auditability. "Just save the final model file" = insufficient (exam distractor).

## Peer Review Before Production
- Reviewer must be INDEPENDENT of the model's developer.
- Validate: performance metrics, bias/fairness results, documentation vs. acceptance criteria.
- Self-certification by the developer = common wrong answer.

## Exam Gotchas
1. "Detect anomalies with no labels" → students wrongly pick supervised or RL; correct = unsupervised.
2. High train/low test accuracy → students wrongly pick data leakage; correct (usually) = overfitting.
3. Explainability requirement stated → students wrongly pick highest-accuracy model; correct = interpretable model.
