# User Guide for Accessing and Inputting Data for Paleo Crustal Thickness Prediction
# Geochemical data modelling towards predicting crustal thickness

Accessing Training Files and Inputting Your Data
This guide provides instructions on where to find the necessary training files for the paleo crustal thickness prediction script and how to input your own data for analysis.

Training Files
The training files required for the paleo crustal thickness prediction script are provided within the project repository. These files contain preprocessed geological data that has been curated and formatted to train the machine learning models effectively.

#Location of Training Files:

The training files can be found in the data/Models for machine learning data training/ directory within the project repository.

The main training dataset is named Model 1.csv and includes various geological parameters necessary for the model training process. 

#Inputting Your Own Data
To utilize the script for calculating paleo crustal thickness with your own data, follow these steps:

Format Your Data: Ensure your data is formatted similarly to the provided training files. The dataset should include columns for each geological parameter used in the prediction model. Detailed instruction can be in the script.

Data Input Directory: Place your data file in the data/input/ directory within the project repository. Ensure your data file is in CSV format and named appropriately, such as Model 1.csv. Ages and age errors of each sample can be added when you have received your output file.

Script Configuration: Modify the script configuration to point to your input data file. Locate the section of the script where the data file path is specified and update it to reflect the location of your input file. 

For any further assistance or queries regarding data input or script usage, please refer to the detailed documentation within the script or contact the script's author.

