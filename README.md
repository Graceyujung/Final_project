### 🛍️ Brazilian E-commerce Analysis

## Overview
This project analyzes the **Brazilian E-commerce Public Dataset** from Kaggle to understand delivery performance, customer satisfaction, and factors influencing delivery delays and review scores. The goal is to provide actionable insights to improve logistics, customer experience, and operational efficiency in the retail sector.

## Dataset Description
The dataset contains transactional and delivery data from a large Brazilian e-commerce platform, including:
- Customer information
- Order details and timestamps
- Product and seller data
- Delivery and shipping information
- Customer review scores

Source: [Brazilian E-commerce Public Dataset on Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

## Project Objectives
- Understand how delivery performance affects customer satisfaction (review scores).
- Identify key factors contributing to delivery delays and SLA violations.
- Develop predictive models to estimate customer review scores based on delivery and order features.
- Provide recommendations to optimize delivery logistics and enhance customer loyalty.

## Data Preprocessing
- Dropped rows missing critical order, delivery, or product data.
- Imputed missing product dimension values with median per category.
- Converted delivery timestamp columns to datetime format.
- Created new features such as delivery status, delivery delay, SLA violation, and approval delay.
- Handled missing review scores using mode imputation grouped by SLA violation.

## Exploratory Data Analysis (EDA)
- Analyzed delivery status vs order status.
- Explored relationships between SLA violations and review scores.
- Examined product categories against review scores.
- Assessed delivery delays over time (weekly/monthly).
- Visualized price ranges and their impact on delivery delays and reviews.

## Modeling Approach
- Target variable: **Review Score** (customer satisfaction).
- Models applied: Random Forest, XGBoost, LightGBM.
- Evaluated models using accuracy metrics per class and overall train/test accuracy.
- Feature importance highlighted key predictors like approval delay, delivery delay, freight ratio, and shipping time.

## Key Results

| Class | RF Accuracy | XGB Accuracy | LGBM Accuracy |
|-------|-------------|--------------|---------------|
| 0     | 0.82        | 0.79         | 0.77          |
| 1     | 0.72        | 0.66         | 0.67          |
| 2     | 0.68        | 0.62         | 0.62          |
| 3     | 0.66        | 0.61         | 0.60          |
| 4     | 0.73        | 0.67         | 0.66          |

| Model | Train Accuracy | Test Accuracy |
|-------|----------------|---------------|
| RF    | 0.99           | 0.67          |
| XGB   | 0.86           | 0.62          |
| LGBM  | 0.76           | 0.62          |

## Insights & Recommendations
- Focus on logistics optimization for product categories with high delays or freight inefficiencies.
- Use predicted delivery delay and approval lag to trigger early customer notifications and reroute shipments.
- Investigate sellers with frequent delays or long approval times to improve processes.
- Launch post-delivery loyalty campaigns targeting customers with high review scores.

## Limitations & Future Work
- Review scores may be influenced by factors beyond delivery, like product quality or customer mood.
- Missing delivery timestamps might affect accuracy of delay and SLA violation analyses.
- Dataset covers a limited period, no data on long-term customer behavior or repeat orders.
- Some review score classes have fewer samples, affecting model robustness.
- Future work: Include customer feedback text for sentiment analysis, incorporate external factors like weather, and improve data completeness.

## How to Use
1. Clone the repo.
2. Load the cleaned dataset for analysis or modeling.
3. Use Jupyter notebooks for exploratory data analysis and modeling.
4. Visualize and explore data further in Tableau with the provided exported CSV file.

## Contact
For questions or collaboration, reach out to Grace at dbwjd1742@gmail.com.

You can also view the project presentation here:  
[Project Presentation](https://docs.google.com/presentation/d/1AiF3w4uYLTfUTxCZlkFY5_9vtFqay_6rpb9Phu6zPrk/edit?slide=id.g35ed2064d70_0_1#slide=id.g35ed2064d70_0_1)

