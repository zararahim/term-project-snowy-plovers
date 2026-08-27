# Interactive Geomap Dashboard – README

This folder contains the interactive geomap component of our project. The map was created using Folium and visualizes Snowy Plover activity and nesting metrics across Point Reyes.

## Files

- plover_map.html  
  HTML map that can be opened directly in any web browser.  
  Does not require Python or the dataset to view.

- Interactive_Geomap.ipynb  
  Jupyter Notebook used to generate the geomap. Requires the cleaned dataset ( in the data folder of our project).

## Dataset Requirement (for running the notebook)

To run the notebook and regenerate the map, download the following csv: 

data/cleaned_plover_dataset.csv

The notebook expects a path such as (add to Google Drive):

"/content/drive/MyDrive/Snowy Plover Datasets/cleaned_plover_dataset.csv"


Update the path inside the notebook if your dataset is stored elsewhere.

## Rebuilding the Map Using the Notebook (Optional)

You can regenerate or modify the geomap by running the Jupyter notebook included in this folder.

### Option 1: Google Colab (recommended)

1. Upload `Interactive_Geomap.ipynb` to Google Colab.
2. Upload `data/cleaned_plover_dataset.csv` to the Colab environment.
3. Update the file path in the notebook if necessary, for example:

   ```python
   df = pd.read_csv("cleaned_plover_dataset.csv")
   
4. Run all cells in order.
5. Save the map as an HTML file:
   plover_map.save("plover_map.html")

### Option 2: Local Jupyter Notebook

1. Step 1 – Install dependencies

   pip install folium pandas numpy jupyter

2. Step 2 – Launch Jupyter
   jupyter notebook

3. Step 3 – Run the notebook

   Open Interactive_Geomap.ipynb.

    Place cleaned_plover_dataset.csv in the same folder as the notebook (or update the path inside the notebook).

    Run all cells to generate the map.

    A new plover_map.html file will be created in the current directory.


## Running the Notebook

1. Activate your environment  
2. Launch Jupyter Notebook:
   jupyter notebook
3. Open Interactive_Geomap.ipynb  
4. Confirm the dataset path  
5. Run all cells to rebuild the map  
6. The map is saved using:
   plover_map.save("plover_map.html")

## What the Map Shows

- Each bubble represents a beach or survey location  
- Bubble size reflects a plover activity index (total plovers, nest density, and nest success)  
- Clicking a bubble displays detailed metrics  
- The map supports panning, zooming, and interactive inspection of locations
