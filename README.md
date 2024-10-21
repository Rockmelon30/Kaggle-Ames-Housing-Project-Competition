# Predicting AMES Housing Prices 

# Problem Statement

Given a set of data on Ames housing features and sale prices, build a model to predict the sale price of future houses.

# Questions

1. How accurately can we predict the prices of homes?
2. Which housing qualities impact the price of homes the most?

# Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**ID**|*index*|All|The ID associated with a listed property.|
|**saleprice**|*int*|All|The property's sale price in dollars.|
|**gr_liv_area**|*int*|All|Above grade (ground) living area square feet.|
|**garage_area**|*float*|All|TSize of garage in square feet.|
|**garage_cars**|*float*|All|Size of garage in car capacity.| 
|**total_bsmt_sf**|*float*|All|The average life expectancy of the associated country.|
|**1st_flr_sf**|*int*|All|First Floor square feet.|
|**year_remod/add**|*int*|All|Remodel date (same as construction date if no remodeling or additions).|
|**garage_yr_blt**|*float*|All|Year garage was built.|
|**land_slope**|*object*|All|Slope of property.|
|**neighborhood**|*object*|All|Physical locations within Ames city limits.|
|**roof_matl**|*object*|All|Roof material.|
|**exter_qual**|*object*|All|Exterior material quality.|
|**bsmtfin_type_2**|*object*|All|Quality of second finished area (if present).|
|**lot_area**|*int*|All|Lot size in square feet.|
|**house_style**|*object*|All|Style of dwelling.|
|**overall_qual**|*int*|All|Overall material and finish quality.|
|**year_built**|*int*|All|Original construction date.|
|**central_air**|*object*|All|Central air conditioning.|
|**full_bath**|*int*|All|Full bathrooms above grade.|
|**half_bath**|*int*|All|Half baths above grade.|
|**bedroom_abvgr**|*int*|All|Number of bedrooms above basement level.|
|**kitchen_qual**|*object*|All|Kitchen quality.|
|**yr_sold**|*int*|All|Year Sold.|


## Data Used
1. train.csv
2. test.csv
3. sample_sub_reg.csv
4. train_cols_cleaned_01.csv
5. train_cols_cleaned_02.csv
6. test_cols_cleaned_01.csv
7. test_cols_cleaned_02.csv
8. Prediction_01.csv
9. Prediction_02.csv
10. Prediction_03.csv

Links to outside resources used:
1. Kaggle Competition [Link](https://www.kaggle.com/competitions/dsb-521-ames-housing-challenge)
2. ANOVA Tests [Link](https://www.scribbr.com/statistics/one-way-anova/)


---

## Requirements
- Python, Jupyter
- Pandas, Numpy, Matplotlib, Seaborn
- Scikit Learn libraries:
   - Ridge, RidgeCV, Lasso, LassoCV
   - StandardScaler, Train Test Split, Metrics, LinearRegression
   - Statsmodels PairwiseTukey

---
## Executive Summary
 This project aims to develop a predictive model for estimating home prices using advanced data science and machine learning techniques. By leveraging historical real estate data and property characteristics, the model will provide as accurate and reliable home price predictions as possible. This initiative is designed to assist real estate professionals, investors, and potential homebuyers in making informed decisions, thus enhancing market efficiency and transparency.
 
#### Purpose
- Kaggle Competition


#### Methods
  - Selected the 10 features I thought would be the best predictors and built a basic model and made first predictions using them
  - Separated my datasets into categorical and numeric datasets
  - Explored raw data for correlation between numeric variables
  - Used ANOVA tests and created a function using them to explore statistical relevance of categorical variables
  - Selected the best results from both of the previous steps
  - Explored the data sets for missing values and dropped them
  - Explored data for outliers in data and corrected them
  - Ensured my feautres contained matching value types between train and test sets
  - Created dummies of my categorical features
  - Joined my numeric and categorical features into one dataset
  - Ran a train test split on the combined data
  - Instantiated my linear regression model, fit the data and scored my model
  - Made 2nd set of predictions
  - Used standard scaling and ridge regression on data to see if it would improve the score
  - Created visualizations of actual vs predicted sale prices of my train sets with my different datasets
  

#### Findings
  - I was able to build successively more accurate models, with the final one being able to explain roughly 84% of the variability in sale prices based on my chosen predictor variables.
  - Using Ridge and Lasso regularization didn't meaningfully improve my models in this situation
  - Removing features with multicollinearity didn't seem to meaningfully improve my model's performance either
  - Using more variables yieled better results

#### Next steps
  -   If I were to continue working on improving my model, I might try adding in the next 5 most highly correlated numeric variables
  -   I would also try using GridSearch
