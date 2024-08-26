#User Guide for Paleo Crustal Thickness Prediction and Analysis Scripts

#1. Introduction
This guide covers two primary scripts:

	Paleo Crustal Thickness Prediction: A script for predicting crustal thickness using machine learning.
	
	Spatial and Temporal Evolution Analysis: A script for visualizing the evolution of crustal thickness across time and geography.
#2. Prerequisites
Python 3.7 or higher
Required Libraries:
pandas
numpy
catboost
matplotlib

#3. Installation
Before running the scripts, ensure all required Python packages are installed:
pip install pandas numpy catboost matplotlib

#4. Script 1: Paleo Crustal Thickness Prediction
Step 1: Data Preparation
Load your dataset, ensuring it has the expected structure (features in columns, target as Crustal_Thickness).
The script checks for missing values and notifies you of any issues.
Step 2: Model Training
The script uses CatBoost to train a model on your data.
Ensure that the input data aligns with the specified features.
Step 3: Model Prediction
After training, you can use the model to make predictions on new data.

#5. Script 2: Spatial and Temporal Evolution Analysis
Step 1: Data Visualization
Load your crustal thickness data, which includes coordinates (latitude, longitude) and time (age).
The script creates scatter plots to visualize how crustal thickness varies over time and space.
Step 2: Plot Customization
The script allows for extensive customization of plots, including setting axis limits, labels, and titles.
It also generates color bars to represent median crustal thickness and annotates the plots with the number of samples.
Step 3: Save Figures
Plots are saved as high-resolution PDFs, suitable for publication.

#6. Example Commands

# Example for training the model
from catboost import CatBoostRegressor
model = CatBoostRegressor()
model.fit(x, y)

# Example for creating and saving a plot
import matplotlib.pyplot as plt
plt.scatter(df['Age'], df['Lat'], c=df['Median_Crustal_Thickness'], cmap='viridis')
plt.savefig('crustal_thickness_plot.pdf', format='pdf', dpi=300)

7. Troubleshooting
Ensure datasets are free from NaN values or handle them appropriately.
Verify the data structure matches the expected format in the scripts.
8. Contact Information
For further assistance, please contact [jianping.geo@outlook.com].
