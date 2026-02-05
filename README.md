# Link Prediction on Social Networks (Positive & Negative Links)

This repository contains experiments for **link prediction** on social networks with **positive (+)** and **negative (−)** edges (signed networks).  
The core workflow is implemented in the Jupyter notebook: **`Link_Prediction.ipynb`**.

## 🎯 Goal
Given a social graph snapshot, predict:
- **Positive links** (e.g., friendship/trust)
- **Negative links** (e.g., distrust/opposition)

This is useful for recommendations, moderation, social analysis, and modeling signed interactions.

## 📁 Repository Structure
- `Link_Prediction.ipynb` — main notebook (feature extraction, training, evaluation)
- `Datasets/` — datasets used in the experiments (raw or preprocessed)

## 🧠 Methods (High-level)
The notebook follows a typical pipeline:

1. **Data loading & preprocessing**
   - Load signed edges (+/−)
   - Train/test split (and optionally negative sampling, depending on dataset format)

2. **Feature extraction (graph-based)**
   - Common Neighbors (CN)
   - Preferential Attachment (PA)
   - Normalized variants and combined metrics (custom heuristics)
   - (Optional) additional features: Adamic–Adar, Jaccard, Katz, etc.

3. **Model training (classical ML)**
   - Logistic Regression
   - Random Forest
   - XGBoost
   - (Optional) other baselines

4. **Evaluation**
   - Accuracy / Precision / Recall / F1
   - ROC-AUC (binary or multiclass depending on formulation)
   - Confusion matrix
   - (Optional) separate evaluation for + and − classes