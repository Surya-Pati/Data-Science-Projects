# Market Basket Analysis of a Grocery Store

This project applies association rule mining techniques to analyze grocery transaction data and uncover frequently purchased item combinations. The objective is to generate actionable insights for product placement, promotions, and inventory optimization.

---

## Project Overview

Market basket analysis is a common technique in retail analytics used to identify relationships between items purchased together. By applying Apriori algorithm, this project highlights patterns in consumer behavior and provides recommendations to improve sales strategies.

---

## Objectives

- Perform exploratory data analysis (EDA) on grocery transaction data  
- Apply association rule mining algorithms (Apriori)  
- Identify frequent itemsets and generate association rules  
- Provide insights for promotions, product bundling, and store layout optimization  

---

## Dataset

- **Source:** Grocery transaction dataset (publicly available or provided)  
- **Features:** Customer IDs, item names, purchase date  
- **Target:** Identification of frequent itemsets and association rules

---

## Methodology

1. **Data Preprocessing**  
   - Transaction formatting  
   - Encoding items for analysis  

2. **Exploratory Data Analysis (EDA)**  
   - Item frequency distribution  
   - Visualization of top purchased items  

3. **Association Rule Mining**  
   - Apriori algorithm for frequent itemsets    
   - Rule generation with support, confidence, and lift metrics  

4. **Insights**  
   - Identification of item associations
   - Recommendations for promotions and product placement  

---

## Results

- Frequent itemsets were successfully identified using Apriori
- Association rules revealed weak relationships between the items
- The customers here are focused on single item in this grocery store 
- Insights can be applied to optimize store layout, marketing campaigns, and inventory management  

---

## Technologies Used

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- mlxtend (for Apriori, TransactionalEncoder)  

---

## How to Run

1. Install dependencies:  
   ```bash
   pip install pandas numpy matplotlib seaborn mlxtend
   ```
2. Open the notebook:  
  `Grocery_Dataset_Market_Basket_Analysis.ipynb`

3. Run all cells to reproduce the analysis and results.

---

## Purpose

This project demonstrates capabilities in:

- Association rule mining and market basket analysis  
- Exploratory data analysis
- Data preprocessing & visualization 
- Data‑driven insights for retail optimization  

---

## Acknowledgements

Thanks to the dataset providers, open‑source libraries, and the data science community for enabling this analysis.
