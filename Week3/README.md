# Credit Risk Classification

This project focuses on building and evaluating classification models to assess customer credit risk.  
The workflow includes exploring linear separability, testing for multicollinearity, comparing models, and ranking customers based on predicted credit scores.

## Objectives

- Explore the linear separability of the two classes and document intuition about the best model type.
- Document the effect of multicollinearity on model performance.
- Train and compare multiple classification models, with a focus on **Support Vector Classifier (SVC)**.
- Tune models for improved performance (optional).
- Generate credit scores from probability outputs (optional).
- Rank customers into risk categories based on score thresholds.

## Dataset

The dataset contains customer loan and repayment information, with features such as:
- Customer repayment behavior
- Loan amount, EMI, tenure
- Number of secured/unsecured loans
- Past due counts (30, 60, 90 days)
- Customer age, interest rates, and more

The target variable is **`default`** (binary classification).

## Steps Covered

1. **Linear Separability**
   - Visualized class separation using scatter plots and PCA projections.
   - Found overlap between classes, suggesting a non-linear model would perform better.

2. **Multicollinearity Check**
   - Used Variance Inflation Factor (VIF) to check correlations.
   - Identified high collinearity among EMI, Loan Amount, and Tenure.
   - Documented potential effect on model interpretability.

3. **Model Training**
   - Tested Logistic Regression, Decision Trees, Random Forest, and **SVC**.
   - **SVC with RBF kernel** gave the best overall results, handling non-linear boundaries effectively.

4. **Model Tuning**
   - Tuned SVC hyperparameters (`C`, `gamma`, `class_weight`) using RandomizedSearchCV.
   - Found improvement in F1 score compared to default parameters.

5. **Credit Scoring**
   - Converted SVC probability outputs into credit scores.
   - Customers ranked using the following methodology:
     - **0 – 200**: Bad Customer  
     - **201 – 350**: 2nd Worst  
     - **351 – 500**: Not So Bad  
     - **501 – 700**: Ideal Guys  
     - **700+**: Eligible for Big Loans  

## Results

- Logistic Regression struggled due to class overlap and multicollinearity.
- **SVC with RBF kernel outperformed other models**, providing the most reliable classification.
- Ranking methodology successfully mapped probability scores to customer categories.


