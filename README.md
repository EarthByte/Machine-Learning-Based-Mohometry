# Paleo Crustal Thickness Estimation and Evolution Visualization

The paleo-crustal thickness estimation and validation workflows from Zhou, J., Farahbakhsh, E., Williams, S., Li, X., Liu, Y., Li, S., & Müller, R. D. (2025). Machine learning and big data mining reveal Earth's deep time crustal thickness and tectonic evolution: A new chemical mohometry approach. Journal of Geophysical Research: Solid Earth, 130, e2024JB030404. https://doi.org/10.1029/2024JB030404.

This repository contains two Jupyter notebooks designed to work with Paleo crustal thickness data. One script focuses on machine learning-based predictions of crustal thickness, and the other focuses on visualizing its spatial and temporal evolution.

## Table of Contents
<ul>
<li>Requirements
<li>Installation
<li>Usage
<ul>
<li>Paleo_Crustal_Thickness-prediction.ipynb</li>
<li>Spatial_Temporal evolution of the Paleo Crustal Thickness.ipynb</li>
</ul>
</li>
<li>Data Requirements</li>
<li>Output Files</li>
<li>Troubleshooting</li>
<li>License</li>
</ul>

## Requirements
To successfully run these notebooks, you need to have Python 3.7 or above installed on your system.

Required Python Packages
<ul>
<li>Python 3.7+
<li>Jupyter Notebook (for running the notebooks interactively)
</li> 
</ul>
Required Python libraries:
<ul>
<li>pandas
<li>numpy
<li>matplotlib
<li>catboost (for Paleo_Crustal_Thickness-prediction.ipynb)
<li>scikit-learn (for additional model evaluation if needed)
  </li>
</ul>

### To install these dependencies, you can create a virtual environment and install the required packages using the following commands:

#### Create a virtual environment (optional but recommended)
<ul>
  <li>python -m venv crustal_env
source crustal_env/bin/activate  # On Windows, use crustal_env\Scripts\activate</li>
</ul>

#### Install required packages
<ul>
 <li>pip install pandas numpy matplotlib catboost scikit-learn jupyter</li>
</ul>

#### If you don't have Jupyter installed globally, you can install it within the environment and launch it with:

<ul>
  <li>pip install jupyter</li>
  <li>jupyter notebook</li>
</ul>

### Additional Data Requirements
<ul>
  <li>The notebooks require datasets in CSV format. Ensure that your data includes the relevant columns, such as geochemical elements and crustal thickness measurements.</li>
</ul>

## Repository Contents
<ol>
<li>Paleo_Crustal_Thickness-prediction.ipynb: </li>
<p>This notebook builds a machine learning model (CatBoost) to predict Paleo crustal thickness using geochemical element data.</p>
<li>Spatial_Temporal evolution of the Paleo Crustal Thickness.ipynb:</li> 
<p>This notebook visualizes the spatial and temporal correlation between geologic age, crustal thickness, latitude, and longitude using scatter plots.</p>
</ol>

## Instructions
### 1. Paleo_Crustal_Thickness-prediction.ipynb
This notebook is designed to predict Paleo crustal thickness from geochemical measurements using a machine learning approach. Follow the steps below to run the notebook successfully:

#### Prepare the Dataset: 
<p>Ensure you have a CSV file with whole-rock geochemical data for paleo-crustal thickness estimation. The dataset should include various major and trace elements (such as SiO₂, TiO₂, Al₂O₃, etc.) with proper order (see Model 1 dataset) as input features and a column labeled Crustal_Thickness for the target variable. If you have only limited geochemical elements, ensuring at least Sr/Y, (La/Yb)n, Rb/Sr, Lu/Hf, Nd/Y, Th/Yb, Ba/V, A/CaO, Cr/Sc, Cr/V, MgO, CaO, K2O, P2O5, Al2O3, MnO, Ho, Lu, Sr, Y, Rb, Ba, Nb, Pb, Sc, V, Ni, A, Nb/Yb, Zr/Y, La/Sm, Dy/Yb, and Sm/Yb are prepared for the LASSO-CV-based estimation model.</p>

#### Edit File Path: 
<p>In the notebook, update the dataFile path to point to your dataset. Example: dataFile = '/path/to/your/dataset.csv'</p>
  
#### Run the Notebook: The notebook will:
<ul>
  <li>Load the dataset and check for missing values (NaN).</li>
  <li>Extract features (geochemical elements) and the target (crustal thickness).</li>
  <li>Train a CatBoost model to predict crustal thickness based on the geochemical inputs.</li>
</ul>

#### Optional: 
You can modify the machine learning workflow, such as performing hyperparameter tuning or cross-validation to optimize the model further.

#### Results: 
Once the model is trained, it can be used to predict crustal thickness for new or unseen geochemical data. You can save the trained model and use it in future predictions.

### 2. Spatial_Temporal evolution of the Paleo Crustal Thickness.ipynb
<p>This notebook focuses on visualizing the spatial and temporal evolution of the paleo-crustal thickness. It generates scatter plots showing the relationship between geographic coordinates (latitude and longitude), geologic age, and median crustal thickness.</p>

Steps to Use:
#### Prepare the Dataset: 
<p>Ensure that your dataset includes columns for Age, Longitude, Latitude, and Median_Crustal_Thickness.</p>

##### Example CSV Columns:

Predicted_Crustal_Thickness, Age, Age error, Lat, Lon

#### Edit File Path: 
Update the file path in the notebook to point to your dataset. dataFile = '/path/to/your/dataset.csv'

#### Run the Notebook: 
The notebook will:
<ul>
  
</ul>
<li>Plot scatter plots that show the correlation between age, geographic coordinates (latitude/longitude), and crustal thickness.</li>
<li>Customize the appearance of the plots with color bars and sample annotations.</li>
</ul>

#### Customize Plots: 
You can adjust the axes limits, color schemes, and minor tick locators depending on your preferences.
#### Save the Output: 
The script saves the resulting plots as a PDF. Make sure to specify your desired file path in the code where the PDF will be saved.

### Usage Notes
#### Running the Notebooks
To run the notebooks:
<ol>
<li>Clone this repository or download the notebooks.</li>
<li>Navigate to the directory where the notebooks are stored.</li>
<li>Launch Jupyter Notebook: </li>
<li>Open either the Paleo_Crustal_Thickness-prediction.ipynb or Spatial_Temporal evolution of the Paleo Crustal Thickness.ipynb notebook and run the cells in order.</li>
</ol>

### Output Files
<ol>
<li>Paleo_Crustal_Thickness-prediction.ipynb: The output is a machine learning model trained to predict crustal thickness based on geochemical data. You can use this model to make predictions on new data.</li>
<li>Spatial_Temporal evolution of the Paleo Crustal Thickness.ipynb: The output is a PDF file containing the scatter plots visualizing the spatial-temporal correlation of crustal thickness.</li>
</ol>

### File Paths
Ensure that you update the file paths for your datasets and output files as needed in each notebook. 

## Troubleshooting
<ul>
<li>Ensure that your data is correctly formatted and that there are no missing values in critical columns.</li>
<li>Check that the Python environment has the correct versions of the required libraries installed.</li>
<li>If you encounter memory issues while processing large datasets, consider running the notebooks on a machine with more RAM or splitting the dataset into smaller chunks.</li>
</ul>
