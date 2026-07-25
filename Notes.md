Run 1 — Baseline LR: AUC 0.8522 — simple starting point, good benchmark

Run 2 — Model Selection: Tested 5 models. Gradient Boost won with AUC 0.8906. Interesting — not XGBoost but Gradient Boost that topped this round

Run 3 — Tuned XGBoost ★ BEST: AUC 0.8924, CV AUC 0.8957 — winner overall. Best params: 300 trees, low learning rate (0.05), shallow depth (3) — classic well-regularized XGBoost config

Run 4 — Ensemble: Bagging won at 0.8868 — slightly below the tuned XGBoost, which shows that a well-tuned single model can beat complex ensembles

Run 5 — FE + PCA + SMOTE: AUC 0.8498 — actually dropped slightly. PCA compressed some useful signal, and SMOTE on financial data doesn't always help
