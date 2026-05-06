# Machine_Learning_Salary_Prediction

## Project Overview

This repository contains a salary prediction model built using a linear regression approach. The goal of the model is to predict employee salary based on demographic and professional features such as age, gender, education level, job title, and years of experience.

## Dataset

The dataset is stored in `Salary_Data.csv` and includes the following columns:

- `Age`
- `Gender`
- `Education Level`
- `Job Title`
- `Years of Experience`
- `Salary`

### Dataset Notes

- The dataset includes both numeric and categorical features.
- Categorical columns are encoded using `LabelEncoder` before model training.
- Missing numeric values are handled by filling with the column mean.

## Model Training

The notebook `Syntecxhub_Project_Machine_Learning_Salary_Prediction.ipynb` executes the following steps:

1. Import required libraries (`pandas`, `numpy`, `sklearn`).
2. Load the dataset from `Salary_Data.csv`.
3. Fill missing numeric values using mean imputation.
4. Encode categorical features with `LabelEncoder`.
5. Split the data into features (`X`) and target (`y = Salary`).
6. Perform a train-test split with `test_size=0.2` and `random_state=42`.
7. Train a `LinearRegression` model on the training set.
8. Evaluate the model using Root Mean Squared Error (RMSE) and R² score.
9. Compare the full-feature model with a single-feature model using the first feature column.
10. Save the best-performing model to `best_salary_model.pkl`.

## Results

The evaluation results from the current dataset are:

- **Multiple Feature Linear Regression**
  - RMSE: `29883.01`
  - R² Score: `0.6656`

- **Single Feature Linear Regression**
  - RMSE: `35539.35`
  - R² Score: `0.5271`

### Best Model

The multiple feature linear regression model performed better than the single feature model. The selected best model was saved as:

- `best_salary_model.pkl`

## Files in the Project

- `Salary_Data.csv` - Dataset file.
- `Syntecxhub_Project_Machine_Learning_Salary_Prediction.ipynb` - Jupyter notebook with model training and evaluation.
- `best_salary_model.pkl` - Serialized best model artifact.
- `README.md` - Project summary and instructions.

## Usage

To reproduce the training and evaluation:

1. Open `Syntecxhub_Project_Machine_Learning_Salary_Prediction.ipynb`.
2. Execute all cells.
3. The notebook will train the model, evaluate performance, and save the final artifact.

## Notes

- If additional features are added to the dataset, update the feature selection step accordingly.
- For better model performance, consider feature engineering, regularization, and more advanced regression models.
