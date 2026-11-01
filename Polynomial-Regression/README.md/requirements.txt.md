# Polynomial Regression | Auto MPG Dataset

## Project Overview

This project implements a Polynomial Regression model using Python and Scikit-learn to explore the relationship between a vehicle's horsepower and its fuel efficiency (MPG).

The main objective is to understand how Polynomial Regression can model nonlinear relationships between variables and compare the model's predictions with actual observations.

## Dataset

The project uses the **Auto MPG Dataset**, which contains information about different vehicles, including:

- `mpg`: Miles per gallon (target variable)
- `cylinders`: Number of engine cylinders
- `displacement`: Engine displacement
- `horsepower`: Engine horsepower
- `weight`: Vehicle weight
- `acceleration`: Vehicle acceleration
- `model year`: Manufacturing year
- `origin`: Vehicle origin
- `car name`: Vehicle name

Although several numerical features are explored during data analysis, `horsepower` is used as the input feature for the Polynomial Regression model, while `mpg` is the target variable.

## Project Workflow

### 1. Data Loading and Exploration
- Imported the dataset using Pandas.
- Inspected the dataset using `head()`, `tail()`, and `describe()`.
- Selected relevant numerical features for analysis.

### 2. Exploratory Data Analysis (EDA)
- Created scatter plots to examine relationships between numerical features and MPG.
- Compared features such as horsepower, weight, cylinders, displacement, acceleration, and model year.
- Visualized the distribution and relationship between horsepower and fuel efficiency.

### 3. Train-Test Split
- Split the dataset into training and testing sets.
- Used approximately 80% of the data for training and 20% for testing.

### 4. Polynomial Feature Transformation
- Used Scikit-learn's `PolynomialFeatures` to transform the original input feature.
- Applied a second-degree polynomial transformation.

The resulting model has the following mathematical form:

\[
MPG = \theta_0 + \theta_1(Horsepower) + \theta_2(Horsepower^2)
\]

### 5. Model Training
- Created a Linear Regression model using Scikit-learn.
- Trained the model using the transformed polynomial features.
- Extracted the learned coefficients and intercept.

### 6. Model Visualization
- Plotted the actual training observations.
- Generated predictions across the horsepower range.
- Visualized the fitted polynomial curve alongside the original data points.

### 7. Model Evaluation
Evaluated the model on the test dataset using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R² Score (Coefficient of Determination)

## Model Results

The following results were obtained in the recorded execution of this notebook:

| Evaluation Metric | Result |
|---|---:|
| Mean Absolute Error (MAE) | 3.79 |
| Mean Squared Error (MSE) | 26.97 |
| R² Score | 0.60 |

These results indicate that the model explains approximately 60% of the variance in the test dataset for this particular train-test split.

The results may vary when the dataset is split differently.

## Technologies and Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Key Learning Objectives

Through this project, I practiced:

- Understanding Polynomial Regression.
- Transforming input features using `PolynomialFeatures`.
- Training regression models with Scikit-learn.
- Understanding model coefficients and intercepts.
- Visualizing nonlinear relationships.
- Evaluating regression models using MAE, MSE, and R².

## Conclusion

This project demonstrates how Polynomial Regression can be used to model nonlinear relationships between vehicle horsepower and fuel efficiency.

It also provides practical experience with the machine learning workflow, from data exploration and feature transformation to model training, visualization, and evaluation.
