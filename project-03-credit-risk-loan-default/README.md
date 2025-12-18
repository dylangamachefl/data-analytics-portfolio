# Credit Risk & Loan Default Prediction: An End-to-End Machine Learning Project

## 1. Project Overview

This project demonstrates a complete, end-to-end machine learning workflow for predicting loan default risk. Starting with raw data, the project proceeds through exploratory data analysis (EDA), feature engineering, model development, and culminates in a comprehensive business impact and deployment strategy.

The primary goal is not just to build an accurate model, but to build a *valuable* one: a model that is interpretable, optimized for real-world business costs, and ready for a production environment.

**Core Technologies:** Python, Pandas, Scikit-Learn, XGBoost, SHAP, Matplotlib, Seaborn

---

## 2. Business Problem & Objective

**Problem:** A financial institution faces significant losses from defaulted loans. The traditional manual review process is slow, inconsistent, and struggles to accurately identify high-risk applicants, leading to preventable financial losses.

**Objective:** To develop a machine learning model that can accurately predict the likelihood of a loan applicant defaulting. The model must:
*   **Maximize Recall for "Bad Risk":** The cost of approving a bad loan is ~7x higher than the cost of rejecting a good one. Therefore, the primary goal is to correctly identify as many potential defaulters as possible.
*   **Be Interpretable:** Loan officers must be able to understand *why* the model makes a certain recommendation to build trust and comply with regulations.
*   **Be Optimized for Business Cost:** The final prediction threshold is optimized to minimize financial losses, balancing the costs of missed defaults against lost business opportunities.

---

## 3. 🚀 Key Findings & Business Impact

This model provides a robust framework for reducing financial risk and improving operational efficiency. The final Random Forest model, with an optimized decision threshold, is projected to deliver significant value.

*   💰 **Estimated Annual Savings:** **$2.1M+**
*   📉 **Reduction in Loan Defaults:** **80%** (by catching 4 out of 5 defaulters)
*   📈 **First-Year ROI:** **2823%**
*   ⏱️ **Payback Period:** **Less than 2 weeks** (0.4 months)

| Metric | Dummy Baseline | Final Model (Random Forest) |
| :--- | :---: | :---: |
| **Recall (Bad Risk)** | 0% | **80.0%** |
| **Precision (Bad Risk)** | 0% | **46.6%** |
| **ROC-AUC** | 50% | **78.0%** |

---

## 4. Key Visualizations

#### Financial Impact Summary
A comprehensive view of the model's value, from cost breakdown to ROI over time.
 
<img width="1590" height="1190" alt="image" src="https://github.com/user-attachments/assets/e7ea7435-0c60-4bc4-b711-85aac440c667" />


#### Executive Dashboard Interface (Mockup)
An example of how the model's output, including SHAP-based explanations, can be translated into an actionable tool for end-users.
 
<img width="1789" height="985" alt="image" src="https://github.com/user-attachments/assets/7734bac3-59b5-427e-88b3-11bda89df0dd" />


---

## 5. Technical Walkthrough

The project is structured across four notebooks, each covering a distinct phase of the ML lifecycle:

1.  **`01_eda_credit_risk.ipynb`:** Initial exploratory data analysis to understand feature distributions, correlations, and initial relationships with the target variable ('Risk').
2.  **`02_etl_feature_engineering.ipynb`:** Data cleaning (handling missing values as an informative category), feature engineering (creating `monthly_payment`, `age_group`, etc.), and data scaling to prepare the dataset for modeling.
3.  **`03_model_development.ipynb`:** Training and evaluating multiple models (Logistic Regression, Random Forest, XGBoost). The Random Forest model was selected for its superior performance on recall and ROC-AUC. SHAP was used for model interpretability.
4.  **`04_business_impact_deployment.ipynb`:** Translating the final model's performance into a business case. This includes ROI calculation, sensitivity analysis, a fairness assessment, and a detailed plan for production deployment and monitoring.

---

## 6. Project Structure

```
├── notebooks/
│   ├── 01_eda_credit_risk.ipynb
│   ├── 02_etl_feature_engineering.ipynb
│   ├── 03_model_development.ipynb
│   └── 04_business_impact_deployment.ipynb
├── data/
│   ├── german_credit_data.csv        # Raw dataset
│   └── processed/                      # Cleaned data from Notebook 02
├── outputs/
│   ├── models/                         # Saved model (.pkl) and metadata
│   └── dashboard_data/                 # CSV files to power the Tableau dashboard
├── requirements.txt                    # Project dependencies
└── README.md                           # This file
```

---

## 7. How to Run This Project

### Prerequisites
*   Python 3.8+
*   `pip` for package management

### Installation
1.  Clone this repository to your local machine:
    ```bash
    git clone https://github.com/your_username/credit-risk-project.git
    cd credit-risk-project
    ```
2.  Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```

### Execution
The notebooks are designed to be run in sequential order. Running them out of order will result in errors, as they depend on the output artifacts from the previous notebook.

1.  **Run `01_eda_credit_risk.ipynb`**
2.  **Run `02_etl_feature_engineering.ipynb`**
3.  **Run `03_model_development.ipynb`**
4.  **Run `04_business_impact_deployment.ipynb`**

After running all notebooks, the `/outputs` directory will be fully populated with all analysis results, saved models, and dashboard data.
