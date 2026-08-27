# Code Folder – README

This folder contains all Python notebooks used for data preparation, merging datasets, exploratory analysis, and the full machine learning pipeline for our Snowy Plover project.

---

### **1. `ML_Dataset_Preprocessing.ipynb`**
- Merges all raw datasets from the Data.gov Snowy Plover Monitoring collection  
- Handles missing values, inconsistent text fields, and duplicate entries  
- Generates engineered features (`Month`, `DayOfYear`, `Total_SNPL`, etc.)  
- Outputs the final cleaned dataset: **`cleaned_plover_dataset.csv`**

---

### **2. `Initial_Models_And_Data_Preprocessing.ipynb`**
- Performs initial exploratory data analysis (EDA)  
- Creates static visualizations for predator activity, plover counts, and beach trends  
- Examines feature distributions and relationships  
- Prepares the selected features used later in the ML pipeline  

---

### **3. `ML_Models_Snowy_Plovers.ipynb`**
- Implements the entire supervised ML pipeline  
- Includes:
  - Train/test split with stratification  
  - ColumnTransformer with numeric + categorical preprocessing  
  - Logistic Regression, Decision Tree, and Random Forest models  
  - Hyperparameter tuning with **5-fold cross-validation**  
  - Full evaluation metrics: accuracy, precision, recall, F1-score, ROC-AUC  
  - Confusion matrices and ROC curves  
- Selects **Random Forest** as the final model and evaluates it on the held-out test set  

---

The notebooks require the following Python packages:
pandas

numpy

matplotlib

seaborn

scikit-learn

## ▶ How to Run the Notebooks

1. Open and execute the notebooks **in this order**:
   1. `Data_Merging_and_Cleaning.ipynb`
   2. `Initial_Models_And_Data_Preprocessing.ipynb`
   3. `ML_Models_Snowy_Plovers.ipynb`

2. Ensure `cleaned_plover_dataset.csv` is generated before running the ML notebook.

3. Use **Runtime → Restart & Run All** to ensure a clean, reproducible run.

---


