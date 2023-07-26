## Salary Prediction with Machine Learning

This repository contains Python code for predicting salaries based on survey data using machine learning algorithms. The dataset used is "survey_results_public.csv."

### Data Preprocessing
- The dataset is read using `pandas` and relevant columns ("Country," "EdLevel," "YearsCodePro," "Employment," and "ConvertedComp") are extracted.
- The target variable "ConvertedComp" is renamed to "Salary."
- Rows with missing salary values are removed, and the dataset is filtered to include only employed full-time respondents.

### Exploratory Data Analysis (EDA)
- The dataset is analyzed to gain insights into salary distribution across different countries using box plots.
- Outliers are removed to focus on salary ranges between $10,000 and $250,000 for better model performance.

### Feature Engineering
- Experience data is cleaned and converted to numerical format.
- Education level data is cleaned and categorized into four major categories: "Bachelor’s degree," "Master’s degree," "Post grad," and "Less than a Bachelors."
- Categorical features ("Country" and "EdLevel") are encoded using `LabelEncoder`.

### Model Building and Evaluation
- Three regression models are trained and evaluated: Linear Regression, Decision Tree Regressor, and Random Forest Regressor.
- The root mean squared error (RMSE) is used to evaluate the model's performance.

### Hyperparameter Tuning
- Grid search is applied to the Decision Tree Regressor to find the optimal hyperparameter (max_depth) using `GridSearchCV`.
- The best estimator from grid search is used for the final model.

### Predicting New Salary
- The final model is used to predict salaries for a new input (country: "United States," education: "Master’s degree," and experience: 15 years).
- The trained model and label encoders are saved using `pickle`.

Feel free to explore the code and dataset to understand the salary prediction process and how machine learning models can be applied to real-world datasets.
