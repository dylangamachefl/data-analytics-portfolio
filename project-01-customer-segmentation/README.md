# Customer Analytics & Retention Strategy: A Data-Driven Approach to Reducing Churn in E-Commerce

## Project Overview

**Challenge:** A UK-based online retailer with over 540,000 transactions aimed to understand customer behavior and decrease customer churn.

**Solution:** An end-to-end analytics pipeline was developed, transforming raw data into an actionable retention strategy with a quantifiable return on investment (ROI).

**Tech Stack:** 
*   Python
*   Pandas
*   Scikit-learn
*   XGBoost
*   K-Means Clustering
*   Seaborn/Matplotlib

**Business Impact:** The project identified an immediate revenue risk of £112,000 and proposed a retention campaign with a projected ROI of 1,117%.

---

## Key Findings & Insights

### Customer Value Concentration

*   **Pareto Principle Validated:** 20% of customers are responsible for 70% of the revenue.
*   **"Loyal Core" Value:** Customers in this segment have an average worth of £14,678.
*   **Segment Value Disparity:** The "Loyal Core" customers are 12.9 times more valuable than those in the "At-Risk" segment, who are worth an average of £1,135.

### Churn Prediction Model

*   **Model Performance:** An XGBoost model was constructed, achieving a 75% AUC score, which indicates a good measure of separability.
*   **Key Predictive Insight:** Purchase frequency was found to be four times more predictive of churn than the customer's monetary value.
*   **Immediate Risk Identification:** The model pinpointed four high-value customers who were at immediate risk of churning, representing £112,000 in revenue.

---

## Business Case

A targeted retention campaign was proposed with the following financial projections:

*   **Cost:** £1,206
*   **Expected Return:** £14,678
*   **Projected ROI:** 1,117%

---

## Technical Approach

1.  **Data Cleaning & Exploration:**
    *   Processed over 397,000 transactions after the removal of outliers.
    *   Identified and isolated 12 "whale" B2B accounts for separate analysis.
    *   Addressed an issue of 25% missing customer IDs.

2.  **Customer Segmentation:**
    *   **RFM Analysis:** A rule-based segmentation was initially performed using Recency, Frequency, and Monetary metrics.
    *   **K-Means Clustering:** A data-driven approach was also used, which revealed naturally occurring customer groupings.
    *   **Final Segments:** The final solution identified two distinct B2C segments: "Loyal Core" and "At-Risk."

3.  **Predictive Modeling:**
    *   **Feature Engineering:** Behavioral metrics such as customer tenure, purchase cadence, and revenue trends were created.
    *   **Model Comparison:** A Logistic Regression model (73.2% AUC) was compared with an XGBoost model (75.1% AUC).
    *   **Feature Importance:** The analysis of feature importance confirmed that frequency was a more significant predictor than recency or monetary value.

---

## Strategic Recommendations

1.  **Focus on High-Value Retention:**
    *   Implement a VIP program for the "Champions" and "Loyal Core" customer segments.
    *   *Rationale:* This group of 20% of customers generates 70% of the revenue, making their retention a top priority.

2.  **Deploy Proactive Retention System:**
    *   Automate the process of churn prediction and intervention.
    *   Integrate the model's output with the marketing platform.
    *   Trigger personalized offers when a customer's churn probability exceeds 50%.
    *   The model's performance should be monitored on a monthly basis.

3.  **Improve Data Collection:**
    *   Mandate customer identification at the point of checkout.
    *   *Rationale:* Currently, there is a loss of visibility on 15% of the revenue.
    *   **Target:** The goal is to reduce anonymous transactions to below 1%.

---

## Project Outcomes

✅ A comprehensive analytics pipeline, from raw data to a strategic business plan.

✅ Actionable segmentation that identifies distinct customer behaviors.

✅ A predictive model capable of identifying at-risk customers before they churn.

✅ A quantified business case with clear projections for return on investment.

✅ An implementation roadmap for deploying these insights into production.

---

## Technical Details

**Dataset:** UCI Online Retail Dataset (December 2010 - December 2011)
*   541,909 transactions
*   4,338 unique customers
*   8 countries

**Notebooks:**
*   Data Exploration & Cleaning
*   Feature Engineering & RFM Segmentation
*   Customer Segmentation with K-Means
*   Churn Prediction Analysis
*   Customer Lifetime Value & Business Case

**Key Libraries:**
*   `pandas`
*   `numpy`
*   `scikit-learn`
*   `xgboost`
*   `seaborn`
*   `matplotlib`