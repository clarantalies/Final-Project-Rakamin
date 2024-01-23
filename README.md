# Banking Dataset - Marketing Strategy 

## Overview
This project aims to increase the effectiveness of the bank's term deposit marketing campaigns while reducing the associated costs, leveraging machine learning to improve customer targeting
  
## Table of Contents
1. Business Problem
2. Business Assumption
3. Objective
4. Dataset
5. EDA & Insights
6. Data Preparation
7. Modeling
8. Interpretation
9. Conclusion
10. Recommendation
11. Future Work
12. Team behind this project

## 1. Business Problem
- **Ineffective Campaign**: Only 11% conversion rate in the bank's term deposit marketing campaign.
- **High Marketing Cost**: Need to reduce marketing expenses due to economic strains post-pandemic.

## 2. Business Assumptions
- The dataset from the Portuguese banking institution's direct marketing campaigns holds valuable patterns that can predict customer subscription behavior.
- Implementing a data-driven marketing approach will enable us to target potential subscribers more accurately, reducing marketing costs.
- The insights gained from the data will allow the bank to refine their marketing strategies even in a post-pandemic economic environment.

## 3. Objective
- **Machine Learning Model Development**: Create models to forecast potential term deposit subscriptions.
- **Targeted Marketing Campaigns**: Use model insights to concentrate efforts on high-potential customers, thereby increasing efficiency and reducing costs.
- **Business Decision Refinement**: Extract and apply key features driving subscriptions to enhance future strategies.

## 4. Dataset
The analysis is based on the "Banking Dataset - Marketing Targets" obtained from Kaggle. This dataset encompasses direct marketing campaigns (phone calls) of a Portuguese banking institution, which occurred from May 2008 to November 2010. It contains detailed information on 45,211 marketing contacts with potential clients, structured across 17 input variables and 1 output variable (the target, 'y'), which signifies whether the client subscribed to a term deposit.

## 5. EDA & Insights
- **Job**: Students are 4X more likely to subscribe.
- **Marital**: Singles are 1.477X more likely to subscribe than married individuals.
- **Education**: People with tertiary education are 1.738X more likely to subscribe than those with primary education.
- **Default**: Clients with no default are 1.848X more likely to subscribe.
- **Housing**: Those without a housing loan are 2.167X more likely to subscribe.
- **Loan**: Individuals without a personal loan are 1.893X more likely to subscribe.
- **Contact**: A cellular contact method has 3.661X higher success.
- **POutcome**: A previous outcome of "success" has 7.069X higher chance of subscription.

## 6. Data Preparation
- **Missing Value**: 0 Missing Values.
- **Outliers**: Keep or Drop.
- **Feature Encoding**: Label Encoding and One-Hot Encoding (OHE).
- **Duplicated Data**: 0 Duplicated Data.
- **Feature Transformation**: Convert negative balances to absolute values.
- **Handling Class Imbalance**: Use SMOTE.
- **Feature Extraction**: Convert "Month" to quarters.
- **Feature Selection**: Remove irrelevant features and use RFE for critical feature selection.

## 7. Modeling

### Models Used:
- **Logistic Regression**: Demonstrated the best precision score, indicating high effectiveness in predicting customer subscription likelihood.
- **Random Forest**: Provides robustness to overfitting by using multiple decision trees.
- **XGBoost**: Known for high performance in classification tasks.

### Data Splitting:
- **Training Data (80%)**: Primary data used to train the models.
- **Validation Data**: Subset of training data to fine-tune models and prevent overfitting.
- **Testing Data (20%)**: Used to assess model generalization.

### Precision and Recall:
- Precision decreased slightly after hyperparameter tuning, suggesting the original model may be preferable.
- Precision improved to 0.7012 with a recall of 0.2983 by adjusting the threshold to 0.662721 on the precision-recall curve.

### Costs and Trade-offs:
- Emphasis on precision to reduce marketing costs by avoiding uninterested customers.
- Accepting lower recall based on the assumption that interested customers will reach out independently.


## 8. Interpretation

### Conversion Rate Improvement
- **Before Machine Learning (ML)**
The original conversion rate, before applying ML, was calculated as follows:

```
Conversion Rate = (Number of Actual Subscribers / Total Number of Contacts) * 100
Conversion Rate = (5289 / 45211) * 100 = ~12%
```

This resulted in only 12% of the customers contacted actually subscribing to the term deposit.

- **After implementing ML**

```
Conversion Rate = (Number of Actual Subscribers / Number of Predicted Subscribers) * 100
Conversion Rate = (1596 / (884 + 1596)) * 100 = ~64%
```

Based on the model's predictions, about 64% of the customers predicted to subscribe actually did subscribe to the term deposit.

### Cost Reduction

By targeting only those customers identified by the model as likely to subscribe, the company has achieved approximately a 96% reduction in marketing costs, showing a drastic decrease from £3,123,900 to £124,000.

### Profit Comparison
Profits surged by 997% compared to the non-ML approach and by 53% compared to manual filtering, proving that ML can reduce costs without sacrificing revenue potential.

## 9. Conclusion

The strategic implementation of machine learning models has substantially enhanced the bank's marketing efficiency and effectiveness. Among the models utilized, **Logistic Regression** notably stood out, demonstrating **70% precison** dan **30% recall**, which indicates its strong performance in reliably predicting customer subscription behavior for term deposits.

### Key Outcomes:

- **Conversion Rate**: Transitioning from a baseline conversion rate of 12% to an optimized rate of 64% after model deployment showcases a significant uplift in marketing success.

- **Cost Efficiency**: Machine learning has revolutionized cost savings, evidenced by a 96% reduction in marketing expenditures, dropping from £3,123,900 to a mere £124,000.

- **Profit Increase**: The bank's profit metrics reflect a substantial increase, highlighting the efficacy of integrating machine learning into their strategic marketing operations.
  
## 10. Feature Importance-Based Recommendations
### Monthly Campaigns
- **Quarter 3 & 4 (Second Half of the Year)**: Concentrate campaigns during quarters 3 and 4, when customers tend to have surplus funds available for vacations or investments.
  - **Holiday Promotions**: Align holiday promotions with year-end fund disbursements to attract customer interest.
  
- **Quarter 1 & 2 (First Half of the Year)**: 
  - **March**: Implement campaigns in March, which has shown a high conversion rate for term deposit subscriptions.

### Customer Demographics
- **Marital Divorced**: 
  - Divorced customers often have more financial flexibility and can be targeted for long-term investment products.
  
- **Marital Married**:
  - Married couples typically plan their finances for their future together, making term deposits an appealing investment option for them.

### Specific Recommendations
1. **For Divorced Customers**:
   - Offer products like children's education savings or retirement planning, which may align with their needs.
   
2. **For Married Customers**:
   - Tailor holiday promotions specifically for married couples who may want to allocate funds for joint activities.

### Campaign Implementation
- Ensure that each campaign is precisely timed and targeted according to the identified schedule and demographic insights.
- Periodically review the outcomes of campaigns to ensure that these recommendations remain relevant and effective.

## 11.  Future Work:

- Further refinement of the models could be undertaken to improve recall without significantly compromising precision.
- Exploration of additional features that could contribute to the predictive power of the models.
- Expansion of the dataset to include more demographic and transactional features for a more comprehensive analysis.

## 12.  Team behind this project
- Muhammad Iqbal
- A Nahda La Roiba
- Ilham Maulana
- Clara Natalie S
- Eka Apriyani
- R. Rani Indah Salamah
- Sekar Ayu Larasati
- Firstandy Edgar Dhafa
### Source

The dataset is publicly available on Kaggle and can be accessed through the following link:

[Banking Dataset - Marketing Targets | Kaggle](https://www.kaggle.com/datasets/prakharrathi25/banking-dataset-marketing-targets/data)
