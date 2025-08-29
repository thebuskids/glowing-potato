# Predicting Customer Churn

## What is customer churn?
Customer churn is when customers stop doing business with a company. If a customer stopped using a service, they churned.

## Churn in the telco industry
Churn in the telco industry can occur due to factors such a pricing (monthly / annual fees), service quality, customer support, other competitive offerings, etc.

## Importance of churn as a KPI
- **Customer Retention Insight**: Churn directly reflects how well a company retains its customers. High churn signals dissatisfaction, poor service, or strong competition.
- **Revenue Impact**: Losing customers means losing recurring revenue, and even a small increase in churn can lead to significant financial losses over time.
- **Cost Efficiency**: Acquiring new customers is usually more expensive than retaining existing ones. Monitoring churn helps prioritize retention strategies that are more cost-effective compared to strategies to bring in new customers.
- **Service & Product Feedback**: Churn trends can reveal which products, services, or customer segments are underperforming, guiding improvements and innovation.

## Why predict churn
Churn prediction is important for telco companies because retaining existing customers tend to be more cost-effective than acquiring new ones. By leveraging data science techniques, companies can identify at-risk customers and implement targeted retention strategies to reduce churn and improve long-term profitability.

## Dataset
Information about the dataset:
- **Source**: https://www.kaggle.com/datasets/blastchar/telco-customer-churn
- **Structure**: 7,043 customers with 21 features (20 features + 1 ID column)

## Project Objective
In this project, we will explore the data and try to answer the following questions:
- What is the % of churn in our fictional telco company?
- Are there specific demographics that tend to have higher/lower churn?
- Are there specific locations that tend to have higher/lower churn?
- Are there specific services that tend to have higher/lower churn?

## Structure of the Project
- Data Exploration & Preprocessing
- Data Modelling & Evaluation
  - Logistic Regression
  - Random Forest Classifier
  - XG Boost
  - Stacking Classifier combining all 3 base models

## Findings
<table>
    <tr>
        <th>Model</th>
        <th>Accuracy</th>
        <th>ROC AUC Score</th>
        <th>F1-Score</th>
        <th>Precision</th>
        <th>Recall</th>
    </tr>
    <tr>
        <td>Logistic Regression</td>
        <td>0.726</td>
        <td>0.835</td>
        <td>0.606</td>
        <td>0.490</td>
        <td>0.794</td>
    </tr>
    <tr>
        <td>Random Forest Classifier</td>
        <td>0.781</td>
        <td>0.814</td>
        <td>0.535</td>
        <td>0.615</td>
        <td>0.473</td>
    </tr>
    <tr>
        <td>XG Boost</td>
        <td>0.743</td>
        <td>0.810</td>
        <td>0.583</td>
        <td>0.513</td>
        <td>0.674</td>
    </tr>
    <tr>
        <td>Stacking Classifier</td>
        <td>0.796</td>
        <td>0.836</td>
        <td>0.603</td>
        <td>0.625</td>
        <td>0.583</td>
    </tr>
</table>

## Future Enhancements
Dig into the false negatives and false positives which could potentially help form more targeted retention strategies e.g.
- Are there certain customer segments that tend to be more misclassified?
- Do high-paying customers tend to be wrongly flagged?

Other classification models e.g. decision trees, ensemble methods, etc.