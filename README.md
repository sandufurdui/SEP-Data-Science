# Project Documentation

## Overview

This project involves pre-processing and combining agricultural datasets related to temperature, pesticides, rainfall, and crop yield for further usage. The process is split into two main Jupyter notebooks: `pre_process_csv.ipynb` and `main.ipynb`. The former handles data cleaning and initial processing, while the latter focuses on merging and organizing the datasets.

<!-- 
to change the continent grouping by climate zones


 -->

### Folder Structure

- `original_data/`: Contains the original CSV files for temperature (`temp.csv`), pesticides (`pesticides.csv`), rainfall (`rainfall.csv`), and yield (`yield.csv`).
- `processed_data/`: Stores the processed CSV files after cleaning and filtering.

### Instructions

1. **Temperature Data Pre-processing**
   - File: `pre_process_csv.ipynb`
   - Function: Cleans and filters temperature data.
   - Input: `original_data/temp.csv`
   - Output: `processed_data/processed_temp.csv`

2. **Pesticides Data Pre-processing**
   - File: `pre_process_csv.ipynb`
   - Function: Cleans and filters pesticides data.
   - Input: `original_data/pesticides.csv`
   - Output: `processed_data/processed_pesticides.csv`

3. **Rainfall Data Pre-processing**
   - File: `pre_process_csv.ipynb`
   - Function: Cleans and filters rainfall data.
   - Input: `original_data/rainfall.csv`
   - Output: `processed_data/processed_rainfall.csv`

4. **Yield Data Pre-processing**
   - File: `pre_process_csv.ipynb`
   - Function: Cleans and filters crop yield data.
   - Input: `original_data/yield.csv`
   - Output: `processed_data/processed_yield.csv`

5. **Complete Yield Ranges**
   - File: `pre_process_csv.ipynb`
   - Function: Deletes incomplete yield ranges where records do not cover the years 1992-2013.
   - Input: `processed_data/processed_yield.csv`
   - Output: Updated `processed_data/processed_yield.csv`

6. **Combine and Map Data**
   - File: `main.ipynb`
   - Function: Merges yield data with continent data, pesticides data, rainfall data, and temperature data successively.
   - Outputs: `yield_continent.csv`, `yield_continent_pesticides.csv`, `yield_continent_pesticides_rainfall.csv`, `combined_raw_data.csv`

7. **Data Cleaning and Filtering**
   - File: `main.ipynb`
   - Functions: Removes unnecessary columns, deletes rows with missing values, and counts the number of records per continent.
   - Output: Updated `combined_raw_data.csv`

8. **Fill Missing Rainfall Values**
   - File: `main.ipynb`
   - Function: Fills single missing values for average rainfall by interpolating neighboring values.
   - Input/Output: Updated `combined_raw_data.csv`

9. **Final Column Operations**
   - File: `main.ipynb`
   - Functions: Renames, reorders, and deletes columns for the final dataset.
   - Output: Final dataset saved in `processed_data/combined_raw_data.csv`
