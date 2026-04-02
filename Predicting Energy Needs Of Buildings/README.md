# Predicting Energy Needs Of Buildings

This project develops regression models to predict two variables heating load and cooling load of buildings based on their dimension & materials. The objective is to apply regression models in real-life dataset.

---

## Project Overview

Energy usage is influenced by multiple factors. This project applies regression techniques to model these relationships and generate actionable insights.

---

## Objectives

- Perform exploratory data analysis (EDA) on energy consumption data  
- Build regression models to predict the target variable  
- Evaluate model performance using statistical metrics  
- Provide actionable insights 

---

## Dataset

- **Source:**  Available in this folder  
- **Features:**  Dimension & Materials of diffrent buildings
- **Target Variable:** Heating load & Cooling load

---

## Methodology

1. **Data Preprocessing**  
   - The dataset was clean from the start hence this step was not required  

2. **Exploratory Data Analysis (EDA)**  
   - Target column distribution 
   - Corelation matrix analysis

3. **Model Development**  
   - Linear Regression
   - Cross‑validation  

4. **Model Evaluation**  
   - Metrics: RMSE, MAE, R²  
   - Residual analysis  
   - Feature importance ranking  

---

## Results

- Regression models achieved strong predictive accuracy, with ensemble methods outperforming baseline linear regression  
- Key drivers of energy consumption included environmental conditions and operational load  
- Insights can support forecasting, cost reduction, and sustainability initiatives  

---

## Technologies Used

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit‑learn  

---

## How to Run

1. Install dependencies:  
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn openpyxl
   ```
2. Open the notebook
   `Energy_Regression.ipynb`

3. Run all cells to reproduce the analysis and model results.

---

## Purpose

This project demonstrates capabilities in:

- Regression modeling  
- Model evaluation 
- Data‑driven insights for energy efficiency 

---

## Acknowledgements

Thanks to the dataset providers, open‑source libraries, and the data science community for enabling this analysis.
