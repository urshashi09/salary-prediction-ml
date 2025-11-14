# Salary Prediction Using Linear Regression

This project builds a machine learning system to predict employee salaries based on features such as Age, Gender, Education Level, Job Title, and Years of Experience.
It includes data preprocessing, exploratory data analysis (EDA), model training, model comparison, and an interactive salary prediction script.

## Linear Regression Theory
Linear Regression (LR) is a core statistical method that models the relationship between a continuous output variable (Salary) and one or more input variables as a straight line or hyperplane.

This model aims to find the best fit by minimizing the squared errors between the predicted line and the actual data points.

The mathematical form is:
$y = b_0 + b_1 x + ϵ
## Multiple Linear Regression (MLR) Application
This project uses Multiple Linear Regression (MLR) because the dataset has five predictor variables: Age, Gender, Education Level, Job Title, and Years of Experience.

The MLR equation for this project is: Salary = b0 + b1(Age) + b2(Gender) + b3(Education) + b4(JobTitle) + b(Experience) + ϵ
- The model calculates an optimal coefficient bi for each feature.
- This coefficient quantifies the expected change in Salary for a one-unit change in that specific feature, assuming all other factors remain constant.
- MLR provides an interpretable baseline for understanding how each variable linearly contributes to the predicted salary.

## Project Overview
The goal of this project is to analyze salary-related data and develop predictive models, with a focus on Linear Regression.
Additionally, we compare performance with Decision Tree, Random Forest, and a Voting Regressor.


## Dataset

The dataset Salary Data.csv contains the following columns:

- Age
- Gender
- Education Level
- Job Title
- Years of Experience
- Salary

Basic preprocessing steps:

- Removal of missing values
- Encoding of categorical features (Gender, Education Level, Job Title)

## Exploratory Data Analysis (EDA)

Visualizations are created using Matplotlib and Seaborn, including:

- Age distribution histogram
- Average salary by Education Level
- Average salary by Gender
- Relationship between Experience and Salary

These plots help identify trends, correlations, and the importance of features.

## Models Used

1. Linear Regression
- Simple baseline model
- Measures linear relationships
- Metrics:
  - R² Score
  - Mean Absolute Error (MAE)

2. Decision Tree Regressor

- Non-linear model for comparison
- Useful for comparison

3. Random Forest Regressor

- Ensemble of decision trees
- Typically provides higher accuracy

4. Voting Regressor
- Combines LR, DT, and RF predictions
- Produces an averaged final output



## Model Comparison

Each model was evaluated using R² Score and MAE.
A comparison table and bar graph were created to visualize the performance.

After comparing all models, the Random Forest Regressor achieved the best performance with:
- Highest R² Score 
- Lowest MAE

 Finally, we save the Linear Regression model for future predictions using joblib as

```python
salary_prediction.pkl
```

## Salary Prediction Function

A prediction function accepts user input:
- Age
- Gender
- Education Level
- Job Title
- Years of Experience

After preprocessing the inputs, the function predicts the salary using the saved Linear Regression model.


## Requirements

To run this project,install all dependencies using
```bash
pip install -r requirements.txt
```
## How to Run the Project

1. Clone the repository
2. Install requirements
3. Open the Jupyter Notebook
4. Run all cells to train models, visualize results, and test predictions

## Conclusion

This project successfully analyzes salary factors using Linear Regression.
Among four models, the Random Forest Regressor delivered the most accuracy.
It is efficient, robust, and suitable for real-world salary forecasting.
