# ConnecTel-Customer-Churn-Prediction

### Project Overview

ConnectTel, a leading telecommunications company, is experiencing challenges in retaining customers due to ineffective customer retention strategies. To address this issue, we developed a machine learning-based customer churn prediction system. By leveraging advanced analytics on customer data, this system enables ConnectTel to identify customers at risk of leaving and implement targeted retention strategies.

**Purpose**:  
ConnectTel Telecom seeks to reduce customer churn by developing a machine learning model to predict at-risk customers. The goal is to enable targeted retention strategies, improve customer loyalty, and maintain a competitive edge in the telecommunications industry.

## Methodology
### 1. **Data Preparation**
   - **Dataset**: 7,043 customers, 21 features (e.g., `tenure`, `MonthlyCharges`, `Contract`, `InternetService`).
   - **Cleaning**:  
     - Handled missing values in `TotalCharges` (imputed median for 11 records).  
     - Encoded categorical variables (`PaymentMethod`, `Contract`).  
     - Dropped non-predictive columns (`customerID`).  

### 2. **Exploratory Data Analysis (EDA)**
   - **Key Insights**:  
     - **26.5% churn rate**, with higher attrition among:  
       - Month-to-month contracts (55% of churners).  
       - Fiber optic internet users (41% churn rate).  
     - **Tenure**: Churners averaged 18 months vs. non-churners’ 38 months.  
     - **Monthly Charges**: Churners paid 21% more on average.  

### 3. **Feature Engineering**
   - Created `TenureGroup` (binned 0-12mo, 13-24mo, etc.).  
   - Scaled numeric features (`tenure`, `MonthlyCharges`) for model stability.  



## Key Challenges
1. **Class Imbalance**: Churners represented only 26.5% of data.  
   - **Solution**: SMOTE oversampling and class-weighted models.  
2. **Sparse Categorical Features**: High dimensionality from one-hot encoding.  
   - **Solution**: Aggregated low-frequency categories and feature selection.  

  
### **False Negatives vs. True Positives**  
ConnectTel should prioritize **reducing false negatives** (missed churners) because:  
1. **Cost of Churn**:  
   - **Lost Revenue**: High-value customers contribute significantly to recurring revenue.  
   - **Acquisition Cost**: Replacing a customer may cost 5x more than retention.  
2. **Strategic Impact**:  
   - A 10% reduction in churn could save the company resources.  
3. **Reputation**:  
   - Loyal customers drive referrals; losing them damages brand equity.

### Recommendation

-   **Targeted Retention Campaigns:**
Focus on high-risk customer segments identified by the model — particularly those on monthly contracts with high charges and low tenure.

-   **Incentivize Long-Term Contracts:**
Offer discounts or perks for customers to move from month-to-month to annual contracts.

-   **Monitor Key Predictors:**
Keep a close watch on churn-influencing features like customer service calls, internet service issues, and tenure to catch early warning signs.
 
### Conclusion

This machine learning solution equips ConnectTel with a data-driven approach to customer retention. By implementing targeted intervention strategies based on churn predictions, ConnectTel can reduce customer attrition, enhance customer satisfaction, and maintain a strong competitive edge in the telecommunications industry. Continuous monitoring and model retraining will be essential to adapting to evolving customer behaviors.
