# Surprise Housing - Advanced Regression Assignment
> Advanced regression analysis using Lasso and Ridge regularization techniques to predict house prices for a US-based housing company.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)

## General Information

### Background
This project focuses on advanced linear regression techniques using regularization to solve a real-world business problem in the housing market.

### Business Problem
The primary business objective is to:
1. Predict the actual price of houses accurately using historical data
2. Identify key variables that drive housing prices in the Australian market
3. Help management:
    > Buy houses below intrinsic value
    > Focus on features that yield maximum return on investment
    > Understand pricing dynamics in a new market
    > The model will support data-driven investment decisions and strategic planning.

### Dataset
The analysis uses the **train.csv** dataset containing housing data with:
- **1459 observations** (after data cleaning)
- **258 features** (after encoding categorical variables)
- **Target variable**: Log-transformed SalePrice [LogSalePrice] for better model performance
- **Mixed data types**: Numerical and categorical features

### Methodology
The project is divided into two main parts:
1. **Exploratory Data Analysis (EDA)**
   - Data exploration and visualization
   - Missing value analysis and treatment
   - Feature engineering and derived attributes
2. **Model Building**
   - Ridge Regression
   - Lasso Regression
   - Hyperparameter tuning using GridSearchCV
   - Model comparison and evaluation

## Conclusions

### Key Findings from Model Performance:

1. **Optimal Regularization Parameters:**
   - **Ridge optimal alpha: 10.0** 
   - **Lasso optimal alpha: 0.001**


2. **Model Performance Comparison:**
    - **Ridge Regression:**
    For Ridge regression, the most important features are OverallQual, GrLivArea, TotRmsAbvGrd, OverallCond, 1stFlrSF, FullBath, 2ndFlrSF, GarageCars, and Neighborhood_Crawfor, showing that quality, size, and layout drive house prices.
        Alpha selected: 10.0
        Ridge Train R²: 0.9127731647815557
        Ridge Test R²: 0.8744827545479026
        Ridge RMSE: 0.13744649630277958
        Features Selected = 258(all features retained)
    
   - **Lasso Regression:** 
   For Lasso regression, the key predictors are GrLivArea, OverallQual, PoolQC_Gd, OverallCond, GarageCars, TotRmsAbvGrd, BsmtFullBath, and neighborhood-related variables, indicating that Lasso focuses on fewer but stronger predictors while eliminating less important ones.
        Alpha selected: 0.001
        Lasso Train R2: 0.9088427486286539
        Lasso Test R2: 0.8736070972240357
        Lasso RMSE: 0.13792510323469795
        Features Selected = 87
   - **Comparison**     
   Although Ridge and Lasso deliver almost identical prediction performance, the difference in accuracy between them is minimal and not practically significant. Lasso is selected because it automatically removes less important features, reducing the model from 258 to 87 variables. This makes the model simpler, more interpretable, and more useful for identifying key drivers of house prices for business decisions.

3. **Impact of Doubling Alpha Values:**
   - **Trade-off:** Simpler models with slightly reduced predictive power, a drop in R2 score

## Technologies Used

**Programming Language & Core Libraries:**
- **Python** - Primary programming language
- **NumPy** version: 2.3.2 - Numerical computing
- **Pandas** version: 2.3.1 - Data manipulation and analysis
- **SciPy** version: 1.16.1 - Scientific computing

**Machine Learning & Statistics:**
- **Scikit-learn** version: 1.7.2 - Machine learning algorithms
  - Lasso and Ridge regression models
  - GridSearchCV for hyperparameter tuning
  - StandardScaler and MinMaxScaler for feature scaling
  - Cross-validation and model evaluation metrics

**Data Visualization:**
- **Matplotlib** version: 3.10.5 - Basic plotting and visualization
- **Seaborn** version: 0.13.2 - Statistical data visualization

**Development Environment:**
- **Jupyter Notebook** - Interactive development and analysis

## Acknowledgements
- This project was completed as part of the Advanced Regression coursework using the provided housing dataset. I thank the IIITB faculty for their guidance on regularization concepts and the scikit-learn documentation for helpful machine learning references.

## Contact
Created by [@simran_jv](https://github.com/simranjv) simran.chhabra@sap.com

---
