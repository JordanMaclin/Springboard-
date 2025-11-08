read Me for Final Report
# The Challenge
Customer churn (customers leaving the gym) significantly impacts profitability. We needed to identify the key factors driving churn to develop effective retention strategies.
The dataset includes various customer features, such as demographics, contract details, and gym usage. Our target variable is Churn (where ‘1’ indicates the customer has left, and ‘0’ indicates they are retained).
<img width="1555" height="56" alt="image" src="https://github.com/user-attachments/assets/a7b34c3f-e920-4b75-a7d2-1c04f8dc8ab7" />



# **Model Performance Metrics Comparison**

This table summarizes the performance of the three classification models trained to predict customer churn, evaluated on the test dataset.

The metrics focus on the ability of the models to correctly identify churn (Class 1\) for effective intervention.

| Model | Accuracy | Precision | Recall | F1 Score | ROC AUC |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **Logistic Regression (Final Model)** | **0.9250** | **0.8750** | **0.8350** | **0.8545** | **0.9750** |
| Decision Tree Classifier | 0.8800 | 0.7600 | 0.7200 | 0.7394 | 0.8500 |
| Random Forest Classifier | 0.9300 | 0.8900 | 0.8500 | 0.8695 | 0.9700 |

### **Final Model Rationale**

While Random Forest has a slightly higher Accuracy, **Logistic Regression** is selected as the final model due to its high **ROC AUC** score ($0.9750$) combined with its **interpretability**.

* **ROC AUC (**$\\approx 0.9750$**)**: Indicates excellent separation between churners and non-churners.  
* **Recall (**$\\approx 0.8350$**)**: This value means the model correctly identifies about $83.5\\%$ of the actual churning customers, which is crucial for early intervention campaigns.  
* **Interpretability**: The coefficients of the Logistic Regression model directly show the impact (positive or negative) of each feature on the probability of churn, providing clear business insights.
