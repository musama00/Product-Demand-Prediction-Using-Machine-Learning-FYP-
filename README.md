# Product-Demand-Prediction-Using-Machine-Learning-FYP-

#  Walmart Sales Forecasting Project


This guide provides the necessary steps to set up and run the Walmart Sales Forecasting Project. Follow the instructions below to ensure a smooth setup process.

## About this Project

## Overview
This project evaluates the performance of various machine learning and time series models for forecasting weekly sales at Walmart stores. The analysis focuses on understanding how different algorithms capture sales patterns and which factors most significantly impact retail performance.

## Dataset

*Description:*
The dataset contains weekly sales data from 45 Walmart stores with the following key features:

- *Store*: Unique store identifier (1–45)  
- *Date*: Week start date (2010-02-05 to 2012-10-26)  
- *Weekly_Sales*: Sales amount
- *IsHoliday*: Binary flag for holiday weeks  
- *Temperature*: Average regional temperature  
- *Fuel_Price*: Regional fuel cost  
- *CPI*: Consumer Price Index  
- *Unemployment*: Regional unemployment rate  
- *Type*: Store category (A, B, C)  
- *Size*: Store size in square feet  

*Dataset Characteristics:*
- 421,570 entries covering nearly 3 years of data  
- Significant variability in weekly sales  
- Holiday weeks are rare events  

## Models Evaluated

### Machine Learning Models

| Model                          | RMSE      | R²     |
|-------------------------------|-----------|--------|
| Random Forest Regressor       | 3345.78   | 0.986  |
| XGBoost Regressor             | 2491.11   | 0.9923 |
| AdaBoost Regressor            | 12139.43  | 0.8176 |
| Gradient Boosting Regressor   | 2804.41   | 0.9903 |
| Support Vector Regression     | 18704.60  | 0.567  |
| Neural Network (MLP)          | 1326.88   | 0.9978 |

### Time Series Models
| Model         | RMSE    | R²     |
|---------------|---------|--------|
| SARIMAX       | 310.33  | 0.360  |
| ARIMA         | 184.40  | 0.774  |
| Holt-Winters  | 226.73  | 0.658  |
| Prophet       | 714.54  | -0.362 |

## Key Findings

### Best Performing Models

- *Best Regression Model*: Neural Network (MLP) with RMSE of 1326.88 and R² of 0.9978  
- *Best Time Series Model*: ARIMA with RMSE of 184.40 and R² of 0.774  

### Performance Insights

- Ensemble methods (XGBoost, Random Forest) showed strong performance  
- Neural networks excelled at capturing complex patterns  
- Traditional time series models generally underperformed compared to machine learning approaches  
- Economic indicators (CPI, unemployment) and holidays significantly impact sales  

## Prerequisites

- Python installed on your system
- virtualenv installed
- VS Code Installed

## Installation Steps

### Step 1: clone the repository and Install virtualenv
To clone repository use the give command:

# Repo Link here
https://github.com/musama00/Product-Demand-Prediction-Using-Machine-Learning-FYP-

To create a virtual environment for the project, you need to install virtualenv:

pip install virtualenv

### Step 2: Create a Virtual Environment

Create a virtual environment for your project.


python -m venv venv

### Step 3: Activate the Virtual Environment
Activate the virtual environment to isolate your project dependencies from your global Python environment.

Windows:

venv\Scripts\activate

Linux:
source venv/bin/activate

### Step 4: Install Required Libraries

With the virtual environment activated, install all necessary libraries specified in the requirements.txt file:

pip install -r requirements.txt



### Step 5: Run the Project

- It's recommended to use VS Code to run the project.

    To open VS Code in the current folder, open the Command Prompt or Terminal in the project directory and type: code .

- Install Jupyter Extension in VS Code (if not already installed):

    If you're using VS Code and haven’t installed the Jupyter extension, search for Jupyter in the Extensions view and install it.

- Open the Complete_models_all.ipynb or Complete_models_subset.ipynb file in VS Code.


- Select the Virtual Environment Kernel:

    In Notebook file i.e. Complete_models_all.ipynb or Complete_models_subset.ipynb, their will be an option Select Kernal on right side. 
    Choose the interpreter associated with your virtual environment i.e. venv.

- Run the Notebooks:


    Execute each cell sequentially to run the project.

    Complete_models_all.ipynb contains all the models applied in the code with original dataset i.e. used for training, validation and testing purpose.

    Complete_models_subset.ipynb does have original code but with a subset dataset as per requirements.
