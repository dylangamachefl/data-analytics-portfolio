# Retail Demand Forecasting & Inventory Optimization

### An End-to-End Data Science Project for Walmart

---

## 🎯 Business Problem

Retailers like Walmart face a critical supply chain challenge: accurately forecasting demand to optimize inventory. Overstocking leads to high holding costs and waste, while understocking results in stockouts and lost sales. This project tackles this problem by developing a system to predict weekly product sales and translate those forecasts into a data-driven inventory policy.

---

## ✨ Key Results & Business Impact

The project successfully delivers a robust forecasting model and a clear framework for inventory optimization, leading to several key outcomes:

*   **High-Performance Forecasting:** Developed a **LightGBM model** that accurately forecasts weekly sales at the store-department level, achieving an **8.19% Weighted Mean Absolute Percentage Error (WMAPE)**. This metric means the total forecast error is only a small fraction of the total sales volume, indicating high business reliability.

*   **Data-Driven Inventory Policy:** The forecasts were used to calculate optimal **Safety Stock** and **Reorder Points** for a 95% service level. This provides a clear, actionable strategy to move away from simple rules-of-thumb and towards an empirically optimized inventory policy.

*   **Core Business Insight:** The analysis proved that the most critical factor for determining inventory levels is **demand volatility**, not just sales volume. This allows for a more intelligent allocation of capital—reducing inventory on predictable items and increasing it on unpredictable ones to minimize overall costs while protecting sales.

![Safety Stock vs Sales Visualization](path/to/your/safety_stock_plot.png)
*This key visualization demonstrates that items with similar sales volumes (x-axis) require vastly different safety stock levels (y-axis) based on their demand volatility (color/size of points).*

---

## 🗺️ The Analytical Journey

The project is presented as a narrative across four Jupyter notebooks, each detailing a critical phase of the data science workflow.

1.  **`01_data_exploration_and_seasonality_analysis.ipynb`**
    *   This notebook lays the foundation by exploring the raw data to uncover core business patterns. Key analyses include identifying strong annual seasonality, quantifying the sales lift from holidays (validated with a t-test), and understanding performance differences across store types.

2.  **`02_external_factors_and_feature_engineering.ipynb`**
    *   Here, the focus shifts to preparing the data for machine learning. This involves analyzing external demand drivers and, most importantly, creating powerful time-series features like **seasonal lags** and **rolling averages** that allow the model to understand historical context.

3.  **`03_demand_forecasting_models_comparison.ipynb`**
    *   This is the core modeling notebook. It compares a naive baseline, a linear model, and a LightGBM model. It justifies the selection of **WMAPE** as the primary business metric and establishes the LightGBM model as the champion based on its superior performance.

4.  **`04_inventory_optimization_analysis.ipynb`**
    *   The final notebook translates the ML forecast into direct business value. It uses the model's predictions and error distribution to simulate an optimal inventory policy, calculating the precise **Safety Stock** and **Reorder Points** needed to meet service level targets.

---

## 💻 Tech Stack

*   **Data Manipulation & Analysis:** Pandas, NumPy
*   **Machine Learning:** Scikit-learn, LightGBM
*   **Data Visualization:** Matplotlib, Seaborn
*   **Statistical Analysis:** SciPy, Statsmodels
*   **Development:** Jupyter Notebook, Git, GitHub

---

## 📈 Methodology Deep Dive

### Evaluation Metric: Why WMAPE?

Standard MAPE is unreliable for retail datasets due to its extreme sensitivity to low-volume items and its instability with zero-sale weeks. We chose **Weighted MAPE (WMAPE)**, calculated as `Sum(Absolute Error) / Sum(Actual Sales)`, as it weights errors by their business impact. This metric directly answers the question: "Of our total sales volume, what percentage was our forecast error?"

### Inventory Optimization Formulas

The core of the business simulation uses two industry-standard formulas:
*   **Safety Stock** = `Z-Score * StdDev_of_Forecast_Error * Sqrt(Lead_Time)`
*   **Reorder Point** = `Forecasted_Demand_During_Lead_Time + Safety_Stock`

This data-driven approach ensures that inventory levels are directly tied to the forecast uncertainty for each specific item.

---

## 🔮 Future Improvements

While this project provides a robust end-to-end solution, future iterations could include:

*   **Walk-Forward Validation:** Implement a more rigorous time-series cross-validation to get a better estimate of the model's out-of-sample performance.
*   **Financial Quantification:** Integrate financial data (unit costs, holding costs) to provide a precise ROI and cost-saving analysis in dollar amounts.
*   **Advanced Distributional Analysis:** Model forecast errors using more appropriate statistical distributions (e.g., Poisson for low-volume items) for even more accurate safety stock calculations.

---

## 👤 Author

*   **Dylan Gamache**
*   **LinkedIn:** [www.linkedin.com/in/datadrivendylan/]
*   **GitHub:** [https://github.com/dylangamachefl]