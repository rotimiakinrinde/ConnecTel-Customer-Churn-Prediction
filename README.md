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
3. **Metric Trade-offs**: Balancing recall (catch churners) vs. precision (minimize costs).  
   - **Solution**: Prioritized recall after validating business costs.
  
### **False Negatives vs. True Positives**  
ConnectTel should prioritize **reducing false negatives** (missed churners) because:  
1. **Cost of Churn**:  
   - **Lost Revenue**: High-value customers contribute significantly to recurring revenue.  
   - **Acquisition Cost**: Replacing a customer costs 5x more than retention.  
2. **Strategic Impact**:  
   - A 10% reduction in churn could save ~$2M annually (estimated from industry benchmarks).  
3. **Reputation**:  
   - Loyal customers drive referrals; losing them damages brand equity.
  
### Conclusion

This machine learning solution equips ConnectTel with a data-driven approach to customer retention. By implementing targeted intervention strategies based on churn predictions, ConnectTel can reduce customer attrition, enhance customer satisfaction, and maintain a strong competitive edge in the telecommunications industry. Continuous monitoring and model retraining will be essential to adapting to evolving customer behaviors.
