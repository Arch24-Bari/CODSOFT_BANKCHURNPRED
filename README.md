# CODSOFT_BANKCHURNPRED
THIS CONTAINS THE BANK_CHURN MACHINE LEARNING PROJECT
This project aimed to predict customer churn for a bank using various machine learning models.

Data Analysis and Preprocessing:

The dataset was analyzed for missing values and duplicates.
Categorical features ('Geography' and 'Gender') were one-hot encoded.
New features like 'BalanceSalaryRatio' were created to capture potential relationships.
Irrelevant features like 'RowNumber', 'CustomerId', and 'Surname' were dropped.
The target variable 'Exited' showed class imbalance, with a majority of customers not having churned.
Exploratory Data Analysis (EDA):

Univariate analysis revealed that 'Age' and 'Balance' distributions differed between churned and non-churned customers. Older customers and those with higher balances were more likely to churn.
Bivariate analysis indicated that customers with a higher number of products and those who were inactive members were more prone to churn. Having a credit card did not seem to be a strong predictor of churn.
Model Training and Evaluation:

Three classification models: Logistic Regression, Random Forest, and Gradient Boosting were trained and evaluated.
Evaluation metrics included Accuracy, Confusion Matrix, Classification Report (Precision, Recall, F1-score), and ROC AUC.
Gradient Boosting had the highest AUC, suggesting better discrimination, while Random Forest had slightly higher Accuracy, Precision, and F1-score.
Considering the business context of minimizing false negatives (missing potential churners), Random Forest was initially preferred due to a lower number of false negatives.
Feature Importance:

Feature importance analysis from both Random Forest and Gradient Boosting models consistently showed 'Age' as the most important feature in predicting churn, followed by 'NumOfProducts' and 'BalanceSalaryRatio'.
Hyperparameter Tuning:

Randomized Search was performed to tune the hyperparameters of Random Forest and Gradient Boosting models.
The tuned Gradient Boosting model achieved a higher F1-score than the tuned Random Forest model, indicating a better balance between precision and recall after tuning.
Final Conclusion:

Based on the analysis, feature importance, and hyperparameter tuning results, the Gradient Boosting model is the most suitable for predicting customer churn in this dataset. Although Random Forest initially showed a slightly lower number of false negatives, the tuned Gradient Boosting model's improved F1-score and higher AUC suggest it is better at identifying churners while maintaining a reasonable balance with precision.

Further steps could involve exploring other advanced modeling techniques, implementing techniques to handle class imbalance (e.g., SMOTE), and deploying the model for real-time churn prediction.
