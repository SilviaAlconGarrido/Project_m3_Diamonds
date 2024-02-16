![imagen](assets/diamante.jpeg)

# Diamonds price :gem:

The goal of this competition is to predict the price of diamonds based on their characteristics (weight, color, quality of cut, etc.). This is an academic competition created for the students of the Ironhack Data Analytics Bootcamp.

## :footprints: First steps:

Kaggle data provided (diamonds_train.db), I proceed to extract the data with DBeaver. I use SQLite to be able to transform the data and export it to a CSV file

| index_id | price | carat | city | depth | x | y | z | cut |...|
|----------|-------|-------|------|-------|---|---|---|-----|---|
| 5feceb   | 4268  | 1.21  | Dubai| 62.4  | 6 | 6 | 4 | good|...|
| ...      | ...   | ...   | ...  | ...   |...|...|...|...  |...|
     

## :thinking: Project:

In this project I have carried out different types of data cleaning and I have used different regression models.

## :relieved: Data Preprocessing & Model Building: 

- Data Preprocessing:

   - Simplify x, and z in size.
   - Lable encoding the data to get rid of object dtype.
   - Drop columns that I don't need.
   - Correlation matrix.
   - Replace NaN by the mean of each column.
   - Replace the atypical values by the median of each column.

-  Model Building:
   
    - DecisionTree.
    - DecisionTreeRegressor.
    - RandomForestRegressor.
    - LinearRegression.
    - Xgboost.

> [!Best Model] :trophy:

The best model I got with a punctuation of 538 fue Xgboost. the process is explained in the following steps:

- Data Preprocessing:
    - Replace NaN by the mean of each column.
    - Replace the atypical values by the median of each column.
    - Get the list of categorical variables.
    - Make a copy to avoid changing original data.
    - Apply label encoder to each column with categorical data.
    - Correlation matrix.

-  Model Building:
    - Assigning the features as X and target as y.
    - Building pipelines of standard scaler and model for multiple regressors.
    - List of all the pipelines.
    - Dictionary of pipelines and model types for ease of reference.
    - Fit the pipelines.
    - Model prediction on test data.
    - Model Evaluation.


## :robot: Additionally:

- Used libraries:
 
   * Pandas. 
   * Seaborn.
   * Matplotlib.
   * Sklearn.
   * Xgboost.
   * OneHotEncoder.
   * LabelEncoder.
   * StandardScaler.
   * DecisionTreeRegressor.
   * RandomForestRegressor.
   * LinearRegression.
   * XGBRegressor.
   * KNeighborsRegressor.

## 	:see_no_evil: Project structure:

``` bash
Proyect_m3/
├──  assets
│    └── diamante.jpeg
│── data
│   ├── diamonds_test.csv
│   ├── diamonds_train.csv
│   ├── diamonds_train.db.csv
│   ├── sample_submission.csv
│   └── submission
│       ├── submission_DT_RMSE523552.csv
│       ├── submission_LR1_RMSE0.csv
│       ├── submission_NLimRFR_MSR_149815_.csv
│       ├── submission_RFR_MSR_546.csv
│       ├── submission_RFR_MSR_286878.csv
│       ├── submission_XgBoost_MSR_538.csv
│       ├── submission_XgBoost_MSR_543.csv
│       ├── submission_XgBoost_MSR_570.csv
│       └── submission_XgBoost_MSR_ultimo.csv
├── notebooks
│   ├── M_DecisionTree.ipynb
│   ├── Baseline.ipynb
│   ├── Data_Preparation.ipynb
│   ├── Data_visual.ipynb
│   ├── M_DecisionTreeRegressor.ipynb
│   ├── M_RandomForestRegressor.ipynb
│   ├── M_RFR_ultimo.ipynb
│   ├── M_xgboost.ipynb
│   ├── M_xgBoost+OtraLimpieza_best.ipynb
│   └── model_linearRegression.ipynb
├── .gitignore
├── LICENSE
├── main.py
└── README.md
``` 