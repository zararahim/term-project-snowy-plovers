# Datasets 
This folder contains the datasets used throughout the project.

### merged_OP.csv  
The intermediate merged dataset created during initial data exploration.  
It includes observational data joined with predator data and was used to produce early visualizations and exploratory analysis.

### cleaned_plover_dataset.csv  
The fully cleaned and standardized dataset used for all machine learning models and for generating the interactive geomap.  
This dataset contains corrected column formats, cleaned missing values, unified location names, and engineered features such as Total_SNPL, Month, DayOfYear, NestSuccess, and others.

Both files are included so the notebooks in the repository can be run without needing to recreate the preprocessing pipeline.
