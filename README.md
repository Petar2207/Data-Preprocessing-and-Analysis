# Titanic Dataset Preprocessing and Analysis

This repository contains the steps and code to preprocess and analyze the Titanic dataset. The main objective is to clean and prepare the data for further analysis or machine learning applications. It includes data cleaning, handling missing values, feature engineering, normalization, and visualizing insights from the data.

## Steps in the Notebook

1. **Data Loading**:
   - Loaded the Titanic dataset from a CSV file for analysis.
   - `pandas` library is used to read the dataset.

2. **Initial Data Inspection**:
   - Used `df.info()` to get a brief overview of the dataset structure.
   - Checked for missing values with `df.isnull().sum()` to identify which columns have missing data.

3. **Missing Data Handling**:
   - The 'Cabin' column had missing values, and the missing values were filled with the string 'Cabin' using `fillna()`.
   - The 'Age' column missing values were replaced with the average value using `replace()`.
   - The 'Embarked' column missing values were filled with 'Unknown'.

4. **Binning the Age Feature**:
   - The 'Age' feature was divided into 5 groups (Child, Teen, YoungAdult, Adult, Senior) based on the age ranges using `pd.cut()`.
   - This helps to analyze survival rates across different age groups.

5. **Normalization**:
   - The 'Age' and 'Fare' features were normalized by dividing by their maximum values to scale them between 0 and 1.

6. **Encoding Categorical Data**:
   - Used `pd.get_dummies()` to create binary columns for the 'Sex' feature (female and male).
   - Dropped the original 'Sex' column after encoding.

7. **Data Visualization**:
   - Created a histogram and KDE plot to show the distribution of the binned 'Age' data.
   - Visualized survival rate by gender and age group using bar charts.


## Installation

To run the notebook on your local machine, you'll need to install the required libraries. You can install them using the following commands:

```bash
pip install pandas
pip install numpy
pip install matplotlib
pip install seaborn

