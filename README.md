# Loan Default Risk with Business Cost Optimization

## Objective
Predict the likelihood of a customer defaulting on a loan and optimize the decision threshold based on business cost-benefit analysis. This helps financial institutions minimize financial loss and make better loan approval decisions.

---

## Dataset
- **Dataset:** Home Credit Default Risk (Kaggle)
- **Target Variable:** `TARGET` (0 = No Default, 1 = Default)
- **Features:** Customer demographic, financial, and credit history attributes
- **Size:** ~300,000 rows, 180+ features (sampled for memory efficiency)

---

## Approach
1. **Data Cleaning**
   - Dropped columns with >50% missing values
   - Filled numeric columns with median and categorical columns with mode
2. **Encoding**
   - Applied One-Hot Encoding for categorical variables
3. **Train-Test Split**
   - 80% train / 20% test
4. **Model Training**
   - Logistic Regression (max_iter=1000)
5. **Prediction**
   - Predicted probabilities for test set
6. **Cost Optimization**
   - Defined cost for false positives (FP = 1) and false negatives (FN = 5)
   - Swept thresholds from 0.1 to 0.85
   - Selected threshold minimizing total cost
7. **Evaluation**
   - Classification report (precision, recall, F1-score)
8. **Feature Importance**
   - Identified top features influencing default prediction

---

## Results
- Optimal threshold: `0.20` (minimizes business cost)
- Model performance (at optimal threshold):
  - Accuracy: 91%
  - F1-score: 96%
  - Recall: 98%
- Key features influencing default:
  - `AMT_CREDIT`, `DAYS_BIRTH`, `EXT_SOURCE_3`, etc.

---

## Insights
- Adjusting the classification threshold based on business cost reduces total financial loss
- High-risk customers can be identified early, improving loan approval decisions
- Certain features strongly influence default risk (credit amount, age, external scoring)

---

## Repository Structure
