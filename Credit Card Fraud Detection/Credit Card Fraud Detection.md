# 🏦 Credit Card Fraud Detection (Kaggle)

## Project objective
Build an end-to-end fraud detection pipeline on the Kaggle **Credit Card Fraud Detection** dataset to identify rare fraudulent transactions while balancing business trade-offs between missed fraud and false alerts.

## Dataset
- Source: Kaggle — Credit Card Fraud Detection (European card transactions)
- Characteristics:
  - Highly imbalanced target (`Class`)
  - PCA-transformed features (`V1` to `V28`), plus `Time` and `Amount`

## Business questions
1. How accurately can we identify fraudulent transactions in an extreme class-imbalance setting?
2. What decision threshold maximises business value (fraud prevented vs. review cost)?
3. Which features most influence fraud risk predictions?

## Planned workflow
1. **Data quality checks**
   - Validate missing values, duplicates, and class proportions
2. **Exploratory analysis**
   - Fraud rate by time and amount bands
   - Distribution shift between fraud/non-fraud transactions
3. **Preprocessing**
   - Train/validation/test split with stratification
   - Scaling and optional resampling baselines
4. **Modeling**
   - Baseline: Logistic Regression
   - Tree model: XGBoost/Gradient Boosting
   - Anomaly benchmark: Isolation Forest
5. **Evaluation**
   - PR-AUC, Recall@Precision, F1, confusion matrix
   - Threshold tuning using cost-based scenarios
6. **Interpretability**
   - SHAP global feature importance
   - Local explanations for high-risk transactions
7. **Recommendations**
   - Suggested operating threshold and alert triage strategy

## Portfolio deliverables
- Technical notebook with full EDA, modeling, and explainability
- Business summary report with actionable recommendations

## Tools
- Python, Pandas, NumPy
- Scikit-learn, XGBoost
- Matplotlib, Seaborn
- SHAP

## Success criteria
- Strong precision-recall performance on minority class
- Interpretable risk drivers for analyst review
- Clear business-aligned threshold recommendation
