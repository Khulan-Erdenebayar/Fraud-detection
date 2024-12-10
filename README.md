# IEEE-CIS Fraud Detection Project

## Project Overview
This project focuses on analyzing and building models for fraud detection using the **IEEE-CIS Fraud Detection Dataset**. The goal is to accurately identify fraudulent transactions while minimizing false positives, leveraging advanced feature engineering and machine learning techniques. The dataset includes over 1 million transactions and provides a combination of transactional, identity, and device-related features, making it ideal for exploring complex relationships and patterns.

## Dataset Description
The IEEE-CIS Fraud Detection dataset contains:
- **Total Transactions:** 590,540 training + 506,691 test
- **Fraud Proportion:** ~3.5% fraud cases in the training set
- **Features:** 434 mixed features, including:
  - Numerical and categorical data
  - Anonymized V-features
  - Temporal data (TransactionDT)
  - Identity and device-related metadata
- **Missing Data:** Approximately 41% missing in the `train_transaction` dataset and ~36% in the `train_identity` dataset.

### Challenges
1. **Class imbalance:** Fraudulent transactions represent a small percentage of total transactions.
2. **High dimensionality:** With 434 features, the dataset requires dimensionality reduction and effective feature selection.
3. **Missing values:** Significant missing data needs careful preprocessing to maintain model performance.

## Objectives
1. Explore and understand the dataset using exploratory data analysis (EDA).
2. Engineer features to uncover hidden patterns and improve model performance.
3. Build and evaluate machine learning models to predict fraudulent transactions.
4. Address challenges such as class imbalance, missing data, and dataset complexity.

## Workflow
1. **Data Preprocessing:**
   - Handle missing values using imputation techniques (e.g., mode-based imputation for categorical features).
   - Scale numerical features (e.g., log transformation for skewed variables).
   - Label unknown categories to maintain interpretability.

2. **Feature Engineering:**
   - Extract temporal features from `TransactionDT` (e.g., hour, day, week).
   - Create interaction features (e.g., combining card and address features).
   - Use dimensionality reduction techniques like PCA for anonymized V-features.

3. **EDA (Exploratory Data Analysis):**
   - Visualize missing data distribution and correlations.
   - Explore numerical and categorical features to detect fraud-related patterns.
   - Compare fraud and non-fraud distributions to identify distinguishing characteristics.

4. **Model Development:**
   - Train and evaluate tree-based models like LightGBM, XGBoost, Random Forest, and CatBoost.
   - Use class imbalance techniques (e.g., SMOTE and class weighting).
   - Optimize hyperparameters for improved performance.

5. **Evaluation Metrics:**
   - AUC (Area Under the Curve)
   - F1-Score (balancing precision and recall)
   - Precision and recall metrics for fraud detection accuracy

## Key Findings
- **Temporal Patterns:** Fraud peaks during specific times, such as late at night when transaction frequency is lower.
- **High-Risk Features:** Certain device types, email domains, and V-features show strong correlations with fraud.
- **Model Performance:** LightGBM achieved the highest AUC of 0.965, while XGBoost balanced precision and recall with an F1-Score of 0.722.

## Tools and Libraries
- Python, Pandas, NumPy, Scikit-learn
- LightGBM, XGBoost, CatBoost
- Matplotlib, Seaborn for visualization

## References
The following resources were instrumental in guiding the analysis and model development:
1. [Automatic EDA Libraries Comparison by andreshg](https://www.kaggle.com/code/andreshg/automatic-eda-libraries-comparisson)
2. [Fraud Detection EDA and Modeling by suoires1](https://www.kaggle.com/code/suoires1/fraud-detection-eda-and-modeling#Explore-Numerical-Features)
3. [EDA and Models by artgor](https://www.kaggle.com/code/artgor/eda-and-models)
4. [Feature Engineering & LightGBM by davidcairuz](https://www.kaggle.com/code/davidcairuz/feature-engineering-lightgbm)

---

This README provides a detailed overview of the project, workflow, findings, and references to help understand and replicate the work.
