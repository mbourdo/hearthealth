# Heart Health – Women’s Heart Disease Risk Analysis

## Project Objectives
This project aims to:
- Analyze heart disease data with a **focus on female patients**.
- Identify the most important clinical and exercise-related predictors of heart disease.
- Build and evaluate machine learning models to predict heart disease risk in women.
- Highlight the importance of **sex-specific analysis** in cardiovascular research.

---

## Data Used
- **Source:** Cleveland Heart Disease dataset (public, UCI Machine Learning Repository / Kaggle).
- **Format:** CSV file with demographic, clinical, and ECG-related features.
- **Filtering:** Only female patients (`sex = 0`) were included in this analysis.

---

## Tools & Libraries
- **Data Handling:** Python, Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Model Storage:** Joblib
- **Environment:** Jupyter Notebook

---

## Methodology
1. **Data Loading & Cleaning**  
   - Removed missing value placeholders.
   - Filtered dataset to include only women.
   
2. **Exploratory Data Analysis (EDA)**  
   - Examined distributions of key variables (age, cholesterol, blood pressure, heart rate, ECG indicators).
   - Calculated correlations with heart disease presence.

3. **Model Building**  
   - Trained **Logistic Regression** and **Random Forest** classifiers.
   - Used class weighting to address imbalance.
   - Evaluated using ROC AUC, precision, recall, and F1-score.

4. **Feature Importance Analysis**  
   - Identified top predictors from the Random Forest model.

---

## Results
- **Prevalence:** ~72% of women in the dataset have heart disease.
- **Top Predictors:**  
  - Chest pain type (cp)  
  - ST depression (oldpeak)  
  - Exercise-induced angina (exang)  
  - Slope of ST segment (slope)  
  - Age  
- **Model Performance:**  
  - Logistic Regression: ROC AUC ≈ 0.98  
  - Random Forest: ROC AUC = 1.00 (possible overfitting due to small dataset size)

---

## Key Takeaways
- Exercise-related ECG features are highly predictive for women in this dataset, even more than cholesterol or blood pressure.
- Results reinforce the need for **sex-specific diagnostic models** in cardiology.
- Future work should validate these findings on larger, more balanced datasets.

---

## How to Run

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/hearthealth.git
cd hearthealth
```



### 2. Create a virtual environment (recommended)
```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows 
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Add the dataset
- Place the CSV file (e.g., heart.csv) in the data/ folder.
- Ensure the file has the correct column format from the Cleveland Heart Disease dataset.

### 5. Run the analysis
- Open Jupyter Notebook
```bash
jupyter notebook
```
- Navigate to notebooks/heartanalysis.ipynb and run all cells.

