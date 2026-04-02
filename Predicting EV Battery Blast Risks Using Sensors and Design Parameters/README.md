# Predicting EV Battery Blast Risks Using Sensors and Design Parameters

This project focuses on developing a predictive model using the XGBoost algorithm to estimate blast risks based on sensors and design parameters. 
The objective is to identify ev batteries that can blast leading to safety hazard.

---

## Project Overview

Battery Blast involve multiple variables such as poor battery design, battery type, overcharging and other factors. Accurate prediction of blast results can reduce blast risks and enhance safety.  
This project applies machine learning techniques to model these relationships and deliver reliable predictions.

---

## Objectives

- Build a supervised learning model using XGBoost  
- Analyze the impact of given features  
- Evaluate model performance  
- Provide insights that support risk mitigation & safety  

---

## Dataset

- **Source:** Provided dataset containing Design and Sensor parameters  
- **Features:** 7 features describing the build qualities and usage description
- **Target Variable:** Battery Health (Good, Moderate, chance_of_blast, Blast)

---

## Methodology

1. **Data Preprocessing**  
   - Handling missing values  
   - Feature scaling and encoding   

2. **Exploratory Data Analysis (EDA)**  
   - Distribution analysis  
   - Correlation assessment  
   - Feature importance exploration  

3. **Model Development**  
   - XGBoost Classifier

4. **Model Evaluation**  
   - Performance metrics (Precision, Recall, Accuracy, and F1‑Score)  
   - Feature importance ranking   

---

## Results

- The XGBoost model demonstrated strong predictive performance (Accuracy: 91%) 
- lead-acid batteries, poor cell design, etc. were identified as major contributors to blast outcomes  
- Insights can support improved planning and risk mitigation  

---

## Technologies Used

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit‑learn  
- XGBoost  

---

## How to Run

1. Install dependencies:  
   ```bash
   pip install xgboost pandas numpy scikit-learn matplotlib seaborn
   ```

2. Open the notebook:  
  `XGBoost_Blast_Prediction.ipynb`

3. Run all cells to reproduce the analysis and model results.

---

## Purpose

This project demonstrates the application of machine learning techniques to real‑world problems, highlighting capabilities in:

- Predictive modeling   
- Model evaluation  
- Data‑driven insights  

---

## Acknowledgements

Thanks to the dataset providers, open‑source libraries, and the data science community for enabling this analysis.
