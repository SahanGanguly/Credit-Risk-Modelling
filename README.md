Credit risk modeling is the process of using data, statistical techniques, and machine learning to quantify the potential that a borrower (an individual or a company) will fail to meet their debt obligations.
In simple terms, it's about predicting the chance that someone won't pay back a loan.
The German Credit Dataset represents a miniature version of the same problem.
Here’s a snapshot of the key insights and challenges:
Key Findings:
Strong correlation (0.62) found between loan Duration and Credit Amount.
Significant class imbalance in the target variable, with "good" risks vastly outnumbering "bad" risks.
This imbalance led to models with deceptively high accuracy but poor performance in identifying high-risk applicants, the most critical task.
Modeling Approach:
To combat the imbalance, I implemented and compared several techniques:
Baseline Logistic Regression: High accuracy (71%) but a mere 20% F1-score for the 'bad' class.
SMOTE (Synthetic Minority Oversampling): Improved recall for the minority class, ensuring more high-risk cases were identified.
Class Weight Adjustment: Penalized misclassifying the minority class more heavily.
Random Forest Classifier: The most balanced performance, especially when combined with SMOTE.
Best Result:
The Random Forest model with SMOTE achieved the best balance: 75% accuracy with a 55% F1-score for the 'bad' risk class—significantly improving the model's ability to flag potential defaults without sacrificing overall performance.
Possible Extension: 
Other modelling approaches like LightBGM classifier and XGBoost classification can also be used for even higher accuracy and better f1 scores for predicting defaulters
