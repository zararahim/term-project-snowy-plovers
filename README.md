# term-project-snowy-plovers
term-project-snowy-plovers created by GitHub Classroom

This repository contains our final project for CS133.  
We analyze Snowy Plover data from Point Reyes National Seashore, including observations, predators, nest outcomes, and banding data. Our project includes data exploration, visualizations, an interactive geomap dashboard, and machine learning models.

---

## Repository Structure

### `code/`
Contains all Python notebooks related to:
- data cleaning and preprocessing  
- exploratory data analysis (EDA)  
- machine learning models
See `data/README.md` for details.
Each notebook can be run independently when the required datasets are available.

### `dashboard/`
Contains the **interactive geomap** created with Folium:
- `plover_map.html` — standalone interactive map (open in any browser)  
- `Interactive_Geomap.ipynb` — notebook that generates the map  
- README with environment setup instructions for running the dashboard

### `data/`
Contains the datasets used in the project:
- `merged_OP.csv` — intermediate dataset used for initial EDA  
- `cleaned_plover_dataset.csv` — final dataset used for ML and the interactive map  
See `data/README.md` for details.

### `homework/`
Archived notebooks from earlier assignments.  
These are **not** used in the final pipeline but are included for reference.

---

## How to Run the Project

### 1. Requirements

Before running any notebooks, install Python (3.9–3.11 recommended) and install the required packages:

`bash
pip install pandas numpy matplotlib seaborn scikit-learn folium jupyter `

### You can also use conda 

`conda create -n plover-env python=3.10 -y
conda activate plover-env
pip install pandas numpy seaborn matplotlib scikit-learn folium plotly jupyter`

### 2. Running the Jupyter Notebooks
Step 1 - Launch Jupyter Notebook 
`jupyter notebook
`

Step 2 — Open the notebooks in the /code/ folder:

Initial_Models_And_Data_Preprocessing.ipynb
  - Merges the datasets
  - Cleans missing values
  - Creates engineered features
  - Saves the cleaned dataset as cleaned_plover_dataset.csv

ML_Models.ipynb
- Loads the cleaned dataset
- Performs EDA visualizations
- Trains Logistic Regression, Decision Tree, and Random Forest
- Displays metrics, confusion matrices, ROC curves, and feature importances

Dataset location

Place the following file in the /data/ folder:
`data/cleaned_plover_dataset.csv`


If using Google Colab, update the dataset path inside each notebook.

“For instructions on running the interactive geomap, see /dashboard/README.md.”

