# Crop Yield Prediction Data Analysis Report

## Introduction:

This report presents an analysis of a dataset concerning corn crop yield. The dataset encompasses various attributes related to farmers, farming practices, and environmental factors. The objective is to predict crop yield using machine learning models and evaluate their performance.

### Data Import and Inspection:

- The dataset was imported using pandas' `read_csv()` function.
- It consists of 422 rows and 22 columns.
- Column names were cleaned by removing excess spaces and converting them to lower case.
- Missing values were observed in the 'education' and 'acreage' columns.
- Duplicated rows were checked for, but none were found.

### Data Cleaning:
  
- Missing values in categorical columns were imputed with 'unknown', while those in numeric columns were filled with the mean of the respective column.
- This ensures data completeness and prepares it for further analysis.

### Exploratory Data Analysis (EDA):
  
- The data was explored by examining the value counts of each variable.
- Insights into the distribution of categorical variables and the range of numeric variables were gained.

### Data Preprocessing:
  
- The dataset was split into independent variables (features) and dependent variable (yield).
- Further, the data was split into training and testing sets for model evaluation.
- Features were preprocessed using a pipeline, including scaling numeric columns and encoding categorical columns.

### Model Building and Evaluation:
  
- Machine learning models including RandomForestRegressor, XGBRegressor, LinearRegression, GradientBoostingRegressor, and DecisionTreeRegressor were built.
- Each model was trained on the training data and evaluated on the testing data.
- Evaluation metrics such as R2 score, Mean Absolute Error (MAE), and Mean Absolute Percentage Error (MAPE) were calculated for each model.

## Results:

- RandomForestRegressor and XGBRegressor performed similarly well with R2 scores of 0.86 and MAE around 40.
- LinearRegression performed slightly worse with an R2 score of 0.83 and higher MAE of 43.
- GradientBoostingRegressor and DecisionTreeRegressor exhibited lower R2 scores and higher MAE compared to other models.

## Conclusion:

- RandomForestRegressor and XGBRegressor emerge as suitable models for predicting crop yield based on the provided dataset.
- Further optimization and fine-tuning of these models may lead to improved performance. Additionally, collecting more data or enhancing data quality could potentially enhance model accuracy.
