Machine Learning Engineering — Self-Taught Roadmap

A structured, first-principles journey from mathematics to production ML.
Built by someone who believes understanding why matters more than memorizing what.


Who This Is For
This repo documents my complete ML engineering self-study — every concept, project, and mistake along the way. If you're a self-taught learner targeting an ML engineering role and want a roadmap grounded in fundamentals rather than tutorials, follow along.
Background I started with:

Strong linear algebra (Deisenroth Mathematics for Machine Learning — Ch1-2 complete)
Python fundamentals
Hardware/electronics hobby projects (Arduino, GPS, GSM)
Zero formal CS degree

Target: ML Engineering role in 12–15 months at 5+ hours/day

Roadmap Overview
Phase 1 → Data & EDA
Phase 2 → Classical ML
Phase 3 → Model Evaluation & Feature Engineering
Phase 4 → Neural Networks & PyTorch
Phase 5 → Specializations (NLP / CV)
Phase 6 → MLOps & Production

Phase 1 — Python, Data & EDA
Status: 🟡 In Progress
Concepts Covered

Data loading: CSV, Parquet, JSON, SQLite
Schema inspection, dtypes, null handling
Train / validation / test splits (stratified, time-based, group)
Data leakage — sources and detection
Class imbalance: resampling, class weights, stratification
Feature scaling: standardize, min-max, robust
Categorical encoding: one-hot, ordinal, target, hashing
Missing value strategies: drop, impute, indicator
Outlier detection: IQR, z-score, IsolationForest, winsorization

Projects
ProjectDatasetStatusEDA + Outlier TreatmentBig Mart Sales🟡 In ProgressEDA + Null HandlingBMI Dataset🟡 In Progress
Key Learnings

SimpleImputer(strategy='median') is safer than mean when outliers exist
Group-aware imputation (fill by category median) beats global imputation
Pipeline prevents data leakage during cross-validation — mandatory for production
Custom functions handle complex feature creation; Pipeline handles standard preprocessing


Phase 2 — Classical ML
Status: 🔴 Not Started
Concepts to Cover

Linear regression (closed form + gradient descent)
Logistic regression and the sigmoid
k-NN and the curse of dimensionality
Decision trees and entropy / Gini
Random forests and bagging
Gradient boosting (XGBoost, LightGBM, CatBoost)
SVMs and the kernel trick
Naive Bayes
k-means, DBSCAN, hierarchical clustering
PCA, t-SNE, UMAP for dimensionality reduction

Projects
ProjectDatasetStatusTabular Baseline ClassifierKaggle-style tabular🔴 Planned

Phase 3 — Model Evaluation & Feature Engineering
Status: 🔴 Not Started
Concepts to Cover

k-fold and stratified k-fold cross-validation
Classification metrics: accuracy, precision, recall, F1, ROC-AUC, PR-AUC
Regression metrics: MAE, MSE, RMSE, R², MAPE
Confusion matrix reading
Threshold tuning and calibration
Bias / variance tradeoff
Learning curves and validation curves
Numerical transforms: log, Box-Cox, binning
Datetime features (cyclical encoding for hour/month)
Target encoding with leakage protection
Feature selection: mutual info, L1, permutation importance
sklearn.pipeline.Pipeline + ColumnTransformer


Phase 4 — Neural Networks & PyTorch
Status: 🔴 Not Started
Concepts to Cover

Perceptron and MLP from scratch
Forward pass and backpropagation (manual derivation)
Activation functions: ReLU, GELU, SiLU, softmax
Loss functions: MSE, cross-entropy, BCE
Optimizers: SGD, momentum, Adam, AdamW
Overfitting signals and regularization: L2, dropout, early stopping
Weight initialization: Xavier, He
PyTorch: tensors, autograd, nn.Module, Dataset, DataLoader
Training loop anatomy: zero_grad → forward → loss → backward → step
torch.compile for speedups

Projects
ProjectGoalStatusMNIST numpy-only MLPManual backprop, ≥95% accuracy🔴 PlannedMNIST PyTorch CNN≥99% accuracy, reproducible🔴 Planned

Phase 5 — Specializations
Status: 🔴 Not Started
Planned Areas

NLP: tokenization, TF-IDF, embeddings, transformers (conceptual)
CV: CNNs, convolution intuition, transfer learning basics
RL: Q-learning, policy gradient (conceptual)


Note: Going surface-level on advanced architectures (ViT, ResNet variants).
First job target is tabular ML, not research. Will go deeper post-hire.


Phase 6 — MLOps & Production
Status: 🔴 Not Started
Concepts to Cover

Experiment tracking: MLflow, Weights & Biases
Reproducibility: seeding, version pinning, pyproject.toml
Model serving: FastAPI
Basic cloud: BigQuery, AWS S3 basics
Feature stores (conceptual)
Training-serving skew — what it is and how to prevent it
Model monitoring: drift detection, performance degradation


Mathematics Foundation
Completed before starting this roadmap:
TopicResourceStatusLinear Algebra (Ch 1-2)Deisenroth MML✅ CompleteEigenvectors, SVD, PCADeisenroth MML✅ CompleteProbability & StatisticsStatQuest🔴 Reactive (learn when needed)Vector Calculus3Blue1Brown + notes🔴 ReactiveOptimizationGéron Hands-On ML🔴 Reactive

Strategy: Math gaps addressed reactively during practical work, not upfront.
Strong linear algebra is a genuine differentiator — most practitioners skip it.


Resources
ResourceUsed ForDeisenroth Mathematics for Machine LearningLinear algebra foundationGéron Hands-On ML with Sklearn & TensorFlowClassical ML + neural netsfast.aiDeep learning intuitionAndrej Karpathy YouTubeNeural nets from scratchChip Huyen Designing ML SystemsProduction ML thinkingStatQuestStatistics and ML intuitionKaggle datasetsHands-on practice

Repo Structure
machine-learning/
│
├── phase1_eda/
│   ├── bigmart_eda.ipynb
│   └── bmi_eda.ipynb
│
├── phase2_classical_ml/
│   └── (coming soon)
│
├── phase3_evaluation/
│   └── (coming soon)
│
├── phase4_pytorch/
│   └── (coming soon)
│
├── phase5_specializations/
│   └── (coming soon)
│
├── phase6_mlops/
│   └── (coming soon)
│
└── README.md

Progress Tracker
PhaseProgressPhase 1 — EDA🟡 60%Phase 2 — Classical ML🔴 0%Phase 3 — Evaluation🔴 0%Phase 4 — PyTorch🔴 0%Phase 5 — Specializations🔴 0%Phase 6 — MLOps🔴 0%

Done When I Can

 Spot data leakage in someone else's notebook within 5 minutes
 Choose between accuracy, F1, and ROC-AUC for a problem without googling
 Write a PyTorch training loop from scratch without copy-pasting
 Explain bias vs variance using a learning curve I generated
 Reproduce a teammate's experiment from their MLflow run
 Pick the right encoder for a categorical column based on cardinality and target


Updated regularly as phases are completed. Stars and follows welcome — helps me know someone's learning alongside
