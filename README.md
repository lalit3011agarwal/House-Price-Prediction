# House Price Prediction Project

## Dataset Exploration
- The project focuses on predicting housing prices using the provided dataset.
- The dataset includes various features related to housing, such as location, number of rooms, population, and income levels.
- The target variable is the `median_house_value`, making this a supervised learning problem and specifically a regression problem.

## Preprocessing
Below are the preprocessing steps performed on the data:
- **Missing Values:** Dropped tuples containing missing values in the `total_bedrooms` column.
- **Feature Engineering:** 
  - Created a new feature `location_new` by combining `longitude` and `latitude`.
  - Dropped columns that are negatively correlated with the target variable, such as `total_rooms`, `total_bedrooms`, `population`, and `households`.
  - Removed the categorical column `ocean_proximity` and applied One-Hot Encoding to its subfeatures (`<1H Ocean`, `Inland`, etc.).
- **Log Transformation:** Applied logarithmic transformation to right-skewed columns (`total_rooms`, `total_bedrooms`, `population`, `households`, `median_income`).
- **Feature Scaling:** Standardized or normalized numerical features to ensure consistent input to the model.

## Model Selection
- The recommended machine learning models for predicting housing prices include:
  - **Linear Regression**
  - **Decision Tree Regression**
  - **Random Forest Regression**
  - Additionally, models like **XGBoost** can be considered.

## Model Architecture and Training
- **Feature/Column Selection:** Ensured only relevant columns are fed to the model by dropping unwanted columns.
- **Hyperparameters:** Tuned hyperparameters such as `n_estimators` and `max_depth` for the Random Forest model to improve performance.
- **Cost Function:** Mean Squared Error (MSE) was suggested for evaluating model performance, although it wasn't explicitly used in the current implementation.

## Model Evaluation
- The model's performance is evaluated using cross-validation to ensure it generalizes well to unseen data, thus avoiding overfitting.
- Cross-validation helps in accurately assessing the model's performance on new data.

## Limitations
- Potential risks of underfitting or overfitting need to be monitored.
- The current implementation does not see any significant risks of under/overfitting, but future occurrences can be managed by cross-validation and regularization techniques.

