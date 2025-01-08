
# E-commerce Customer Analysis and Prediction

This project demonstrates the application of machine learning models to predict customer behavior in an e-commerce platform. The dataset consists of customer information, including demographics, session data, and purchase history. The goal of this analysis is to predict customer purchase behavior based on several features.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Model Building](#model-building)
4. [Performance Evaluation](#performance-evaluation)
5. [Requirements](#requirements)
6. [Usage](#usage)

## Project Overview

This project uses various machine learning models to predict whether a customer will make a purchase based on their profile and interaction with the e-commerce platform. It applies models such as Linear Regression, Support Vector Machines (Linear and RBF), and Random Forest Regressor.

## Dataset

The dataset used in this project is provided in the `customer_data.xlsx` file. The dataset contains the following columns:

- **age**: Age of the customer
- **gender**: Gender of the customer
- **annual_income**: Customer's annual income
- **last_visited_days_ago**: Number of days since the customer last visited the site
- **session_duration**: Duration of the session in minutes
- **pages_visited**: Number of pages visited by the customer during their session
- **device**: The type of device used (mobile, desktop, tablet)
- **purchase**: Target variable indicating whether the customer made a purchase (1 for purchase, 0 for no purchase)

## Model Building

The notebook demonstrates the following steps for building and evaluating machine learning models:

### 1. Data Preprocessing:
- Cleaning and handling missing values.
- Encoding categorical variables using one-hot encoding (`pd.get_dummies`).
- Splitting the data into training and test sets.
- Scaling the features using `StandardScaler` to standardize the input features.

### 2. Model Training:
- **Linear Regression**: A baseline regression model to predict the target variable (purchase).
- **Support Vector Machines (SVM)**:
  - Linear kernel: Using `LinearSVR`.
  - Radial Basis Function (RBF) kernel: Using `SVR`.
- **Random Forest Regressor**: An ensemble method to predict the target.

### 3. Performance Evaluation:
- Each model is evaluated using the following metrics:
  - **Mean Squared Error (MSE)**
  - **Root Mean Squared Error (RMSE)**
  - **Mean Absolute Error (MAE)**
  - **R-squared Score (R²)**

### 4. Model Persistence:
- The trained models and scaler are saved as `.pkl` files using `pickle`.
- The processed training data (`X_train` and `y_train`) is saved as CSV files.

## Performance Evaluation

Each model is evaluated based on the aforementioned metrics, and comparisons are made to determine which model best predicts customer purchase behavior.

## Requirements

To run this project, you need the following Python libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `pickle`

These libraries are typically available in Google Colab by default.

## Usage

1. Open the [Google Colab notebook](https://colab.research.google.com/drive/1JdUIFe_ogvF6bCMGPXsvgAACL1S87r9l#scrollTo=sI2iZRx5wDfl).
2. Upload the `customer_data.xlsx` file to the Colab environment.
3. Run each cell step-by-step to perform data preprocessing, train models, and evaluate them.
4. Save the trained models and scaler for later use.
5. The processed data and models can be used for further analysis or predictions.

## How to Contribute

If you would like to contribute to this project, feel free to fork the repository, make your changes, and submit a pull request. Any suggestions or improvements are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
