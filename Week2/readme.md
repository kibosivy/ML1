## Project Overview
This project is part of a Kaggle regression competition.  
The goal is to build a predictive model using machine learning techniques and generate a valid submission file for Kaggle.  

We compare different models (**Linear Regression, Ridge, and Lasso**) and select the best performing one based on validation error.  
The final predictions are submitted in Kaggle’s required format.

---

## Steps Performed
1. **Data Loading**  
   Load training and test datasets provided by Kaggle.

2. **Data Cleaning & Preprocessing**  
   - Handle missing values.  
   - Scale numerical features.  

3. **Model Training & Evaluation**  
   - Compared **Linear Regression**, **Ridge Regression**, and **Lasso Regression**.  
   - Ridge performed best, giving the lowest validation error.  
   - Feature engineering was tested but later dropped as it did not improve results.  

4. **Final Model Selection**  
   - **Ridge Regression** was selected as the final model.  

5. **Prediction on Test Data & Submission File Creation**  
   - The final Ridge model was used to generate predictions on the **test dataset**.  
   - Predictions were saved in `submission.csv`, following the exact format of `sample_submission.csv`.

6. **Scoring on Kaggle**  
   - The submission file was uploaded to Kaggle.  
   - Kaggle evaluated the predictions against the hidden test labels and returned a private/public leaderboard score.
---

