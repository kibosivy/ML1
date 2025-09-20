# Credit Card Fraud Detection

## Project Overview
This project focuses on building and evaluating machine learning models to detect fraudulent credit card transactions. Fraud detection is a highly imbalanced classification problem where fraudulent cases are rare compared to non-fraudulent transactions. The goal is to maximize the ability to detect fraud (recall) while minimizing false alarms (precision).

## Dataset
- Source: Credit Card Transactions dataset    
- Target: Class (`0 = Non-Fraud`, `1 = Fraud`)  
- Challenge: Highly imbalanced dataset with fraud cases being less than 1% of the data.  

## Methodology
1. Exploratory Data Analysis (EDA)  
   - Checked class distribution, feature relationships, and separability of classes.  

2. Preprocessing  
   - Train-test split (80/20).  
   - Handled class imbalance using upsampling of minority class (Fraud).  
   - Scaled features using StandardScaler.  

3. Modeling  
   - Tried multiple models: Logistic Regression, KNN, SVM, Random Forest.  
   - Evaluated models using cross-validation.  
   - Chose Random Forest with `criterion='entropy'` as the best-performing model.  

4. Evaluation Metrics  
   - Accuracy  
   - Precision  
   - Recall  
   - F1 Score  
   - ROC-AUC  

   **Cross-validation and Test Results (Random Forest):**  
      Cross-validated F1 : 0.9998749835076719
      Accuracy : 0.9995241955380115
      Precision (Fraud) : 0.9565
      Recall (Fraud) : 0.7333
      F1 Score (Fraud) : 0.8302
      ROC-AUC : 0.9310
      
   - False Positives: 2 (Non-Fraud flagged as Fraud)  
   - False Negatives: 23 (Fraud missed as Non-Fraud)  

5. Error Analysis  
- Most errors came from false negatives, i.e., fraud transactions classified as normal.  
- Improving recall is crucial for real-world applications.  

6. Learning & Validation Curves  
- Plotted learning and validation curves to check model generalization.  
- Model shows high training performance but recall on fraud remains a challenge.  

## Key Findings
- Random Forest achieved the best overall results.  
- Excellent precision ensures very few false alarms.  
- Recall for fraud cases (~73%) needs improvement, as some frauds are still being missed.  
