# ECE PA 3: Python Data Analysis with Pandas

**Submitted by:** Joshua Roise B. Paras  
**File:** `PARAS_ECE_PA3.ipynb`

This repository contains a Jupyter Notebook demonstrating fundamental data manipulation techniques using the `pandas` library in Python. The analysis is performed on a dataset of cars (`cars.csv`).

## 🚀 Getting Started

### Prerequisites
- Python 3.x
- Jupyter Notebook or Jupyter Lab
- pandas library

### Installation & Execution
1. Clone this repository to your local machine.
2. Ensure the `cars.csv` dataset is located in the same directory as the notebook.
3. Launch Jupyter Notebook and open `PARAS_ECE_PA3.ipynb`.
4. Run the cells sequentially to see the data manipulation outputs.

## 📊 Tasks and Code Overview

Below are the key operations and the exact code used in the notebook to slice, filter, and subset the dataset:

### Setup
Loading the pandas library and reading the dataset, limiting the scope to the first 32 rows.
```python
import pandas as pd
cars = pd.read_csv("cars.csv")
cars = cars.iloc
cars

A. Positional and Label-Based Slicing
Inspecting the dataset's dimensions and extracting specific rows and columns.

# Print shape and column list
print("Shape:", cars.shape)
print("Columns:", cars.columns.tolist())

# Slice rows 5 to 9 (indices 5 through 9)
cars_6_to_10 = cars
cars_6_to_10

# Display only specific columns for the sliced data
cars_6_to_10[['Model', 'mpg', 'cyl', 'hp', 'gear']]

B. Model Lookup
Filtering the dataframe to isolate individual car models based on a condition.

# Look up Toyota Corolla
toyota = cars[cars['Model'] == "Toyota Corolla"]
toyota

# Look up Pontiac Firebird
pontiac = cars[cars['Model'] == "Pontiac Firebird"]
pontiac

C. Multi-Model Subsetting
Using a list to filter for multiple specific car models simultaneously, and selecting a subset of columns for the output.

target_models = ['Datsun 710', 'Lotus Europa', 'Ferrari Dino']
selected_cars = cars[cars['Model'].isin(target_models)][['Model', 'mpg', 'cyl', 'hp', 'gear']]

display(selected_cars)
print("Shape:", selected_cars.shape)
