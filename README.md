# Retail Customer Analytics — Machine Learning Project (36106 AT3)

This project builds three machine-learning solutions for a global retailer:  
**classification**, **regression**, and **clustering**.  
It demonstrates a full end-to-end ML workflow including EDA, feature engineering, modeling, evaluation, and business impact analysis.

The work shows how data science can support real business decisions such as customer targeting, sales forecasting, and segmentation strategy.

---

## Key Highlights

- **Full ML pipeline**: EDA → Preparation → Baseline → Final Model → Evaluation  
- **Three complementary models** solving three different business questions  
- **Well-structured notebooks and reproducible data workflow**  
- **Model choice and metric selection clearly explained**  
- **Strong focus on communication, interpretability, and business value**  
- **Designed for real stakeholders: Marketing, Finance, Operations**

---

## Project Overview

The retailer provided multi-year sales, customer, product, and returns data (2020–2022).  
We address three core questions:

1. **Who is likely to buy next?** → *Classification*  
2. **How much revenue will an order generate?** → *Regression*  
3. **How are customers grouped?** → *Clustering*  

Each task was completed independently by one team member, following the same analysis framework for consistency.

---

## Why Each Student Selected Their Model

### **1. Student A(Me) — Classification (Purchase Prediction)**  
**Why this task?**  
- The business wants to predict repurchase behaviour.  
- Target is binary → classification is the natural choice.  
- Helps marketing reduce campaign cost and increase ROI.

**Why these metrics?**  
- **ROC-AUC**: Evaluates ranking quality on imbalanced data.  
- **PR-AUC**: Focuses on precision + recall; meaningful when few customers repurchase.  
- **Lift/Gain**: Shows real business improvement over random targeting.

---

### **2. Student B — Regression (Revenue Forecasting)**  
**Why this task?**  
- Finance and operations need accurate **per-order revenue** predictions.  
- Target is continuous → regression is appropriate.  
- Predictions can be aggregated for monthly or territory forecasting.

**Why these metrics?**  
- **MAE**: Clear business meaning — “average prediction error per order.”  
- **RMSE**: Penalizes large mistakes; important for high-value items.  
- **R²**: Measures how well the model explains revenue variation.

---

### **3. Student D — Clustering (Customer Segmentation)**  
**Why this task?**  
- Retailers need to understand customer segments for targeting and retention.  
- No label exists → unsupervised learning is required.  
- Clustering reveals differences in value, behavior, and demographics.

**Why these metrics?**  
- **Silhouette Score**: Measures how well customers fit within clusters.  
- **Calinski-Harabasz Index**: Higher = better defined clusters.  
- **Davies-Bouldin Index**: Lower = more separation between groups.

These metrics support selecting a segmentation that is both technically strong and easy for business teams to use.

---

## Repository Structure

```text
project/
│
├── data/                     # All raw and processed datasets
│
├── notebooks/
│   ├── classification/       # Student A notebooks
│   ├── regression/           # Student B notebooks
│   └── clustering/           # Student D notebooks
│
└── reports/                  # Final project reports (DOCX)
```
---  

## Data Description

The dataset includes:

- Sales (2020–2022)

- Customers with demographics

- Product catalog + categories + subcategories

- Returns

- Territories (region, market)

- Training / validation / test splits

- Saved model + prediction outputs (for classification)

The data supports all modeling tasks and ensures reproducibility.

---

## Model Summaries
### 1. Classification — Customer Purchase Prediction

Predicts purchase within next 3 months.

Final model: **Calibrated Random Forest**

Metrics:

- ROC-AUC: 0.815

- PR-AUC: 0.484

Business impact: Higher accuracy for targeted campaigns.

### 2. Regression — Revenue Prediction

Predicts revenue per order line.

Models tested: Ridge Regression, Random Forest Regression.

Metrics: MAE, RMSE, R²

Business impact: More reliable forecasting for budgeting and stock planning.

### 3. Clustering — Customer Segmentation

Final model: **K-Means (6 clusters)**

Findings:

- Two clusters (~34.7% of customers) are high-value groups.

Business impact: Enables differentiated marketing strategies.

---

## How to Run

Python 3.9+ recommended.

Put datasets under: 36106/assignment/AT3/data/

Open and run notebooks in this order for each part (A -> B -> D) :

- EDA

- Preparation

- Baseline

- Experiment 1–4

Run all cells top → bottom.

See the project_report.docx for final numbers, figures, and decisions.

---

## Skills Demonstrated

Data cleaning & integration

Exploratory Data Analysis (EDA)

Feature engineering

Model building & tuning

Ensemble methods (Random Forest)

Regularized regression

Clustering algorithms

Model evaluation & selection

Business interpretation of ML results

Communicating insights for real stakeholders

## Summary

This project brings together three machine-learning methods to create a practical, multi-angle view of retail customers.
It shows strong technical skills, solid understanding of ML modeling, and the ability to connect data science with measurable business value.

The structure, reproducibility, and clarity make this suitable for production-style development and for showcasing to employers.
