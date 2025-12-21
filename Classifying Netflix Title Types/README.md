# Netflix Type Classification

This project applies supervised machine learning techniques to classify Netflix titles as either *Movies* or *TV Shows* based on metadata features. The objective is to demonstrate classification model development, and evaluation in a real‑world entertainment dataset.

---

## Project Overview

Netflix hosts a diverse catalog of titles with varying attributes such as release year, duration, genre, and country of origin. By analyzing these features, this project builds a classification model to predict the type of content.  
The analysis highlights how metadata can be leveraged to support content categorization.

---

## Objectives

- Perform exploratory data analysis (EDA) on Netflix metadata    
- Train and evaluate machine learning models  
- Provide insights into feature importance  

---

## Dataset

- **Source:** Netflix titles dataset (publicly available)  
- **Features:** show_id, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description  
- **Target Variable:** type (*Movie* or *TV Show*)

---

## Methodology

1. **Data Preprocessing**  
   - Handling missing values  
   - Encoding categorical variables   

2. **Exploratory Data Analysis (EDA)**  
   - Distribution of movies vs TV shows  
   - Trends of titles released, content added by release year and distribution of ratings 

3. **Model Development**  
   - Random Forest    
   - Cross‑validation  

4. **Model Evaluation**  
   - Accuracy, Precision, Recall, F1‑Score  
   - Confusion matrix analysis  
   - Feature importance ranking  

---

## Results

- The classification model achieved decent but realisitic performance (Accracy: 71%)
- Key features influencing classification included duration, release year, and other factors  
- Insights demonstrate how metadata can effectively distinguish between movies and TV shows  

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
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
2. Open the notebook:  
  `Netflix_Type_Classification.ipynb`

3. Run all cells to reproduce the analysis and model results.

---

## Purpose

This project demonstrates capabilities in:
- Supervised learning and classification  
- Feature engineering and preprocessing  
- Model evaluation and comparison  
- Data‑driven insights for content categorization  

---

## Acknowledgements

Thanks to open‑source datasets, libraries, and the data science community for enabling this analysis.
