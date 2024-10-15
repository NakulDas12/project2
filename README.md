# Data Wrangling Project

## Overview

This project involves combining and analyzing two datasets using Python and popular libraries like `pandas`, `numpy`, `matplotlib`, and `seaborn`. The datasets are cleaned, merged, and analyzed to extract useful insights, handle missing values, and remove outliers.

## Project Files

- `data_processing.py`: The main Python script containing the code to load, clean, merge, and analyze the datasets.
- `dataset_1.xlsx` and `dataset_2.xlsx`: The raw input datasets used in the analysis.
- `processed_combined_data.xlsx`: The final processed dataset output from the script.

## Workflow

1. **Data Loading**:
   - Two Excel files (`dataset_1.xlsx` and `dataset_2.xlsx`) are loaded using `pandas.read_excel()`.

2. **Handling Missing Values**:
   - Missing values in the `atemp` column of `dataset_2` are filled with the mean of the column.

3. **Data Merging**:
   - The datasets are merged on the `instant` column using `pandas.merge()`.

4. **Data Cleaning**:
   - Unnecessary columns like `Unnamed: 0` are dropped.
   - Datetime conversion for the `dteday` column to extract `year`, `month`, and `day`.

5. **Exploratory Data Analysis**:
   - The unique values of categorical columns such as `season`, `holiday`, and `weathersit` are displayed.
   - Data types are checked before and after conversion.
   - The correlation matrix is computed to observe relationships between the numerical variables.

6. **Handling Outliers**:
   - Outliers are detected using the IQR (Interquartile Range) method.

7. **Output**:
   - The cleaned and processed dataset is exported to an Excel file `processed_combined_data.xlsx`.

## Code Highlights

- **Libraries Used**:
  - `pandas` for data manipulation and analysis.
  - `numpy` for numerical operations.
  - `matplotlib` and `seaborn` for visualizations.
  
- **Handling Missing Values**:
   ```python
   dataset_2['atemp'] = dataset_2['atemp'].fillna(dataset_2['atemp'].mean())

