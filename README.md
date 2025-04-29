# Bengaluru Property Price Prediction

This project is a **classic machine learning regression problem** that aims to predict residential property prices in Bengaluru, India, based on features such as square footage, number of bedrooms and bathrooms, and location. The goal is to build a model that can generalize well to unseen data and provide accurate price estimates for users, investors, or real estate platforms.

---

## 1. Problem Statement

In a growing city like Bengaluru, real estate prices vary drastically based on the location, amenities, and property size. The objective of this project is to:

- Understand the factors affecting housing prices.
- Clean and preprocess raw housing data.
- Train a regression model to predict prices.
- Save the model and feature mappings for later use in a deployed application.

---

## 2. Dataset

- **File**: `bengaluru_house_prices.csv`
- **Source**: Kaggle / open-source dataset
- **Features include**:
  - `location`: Area or neighborhood of the property
  - `total_sqft`: Total area of the property (some values were irregular strings)
  - `bath`: Number of bathrooms
  - `bhk`: Number of bedrooms
  - `price`: Price in lakhs (target variable)

---

## 3. Data Cleaning and Feature Engineering

Several preprocessing steps were performed to make the dataset usable:

- Converted `total_sqft` to numeric by handling ranges and invalid entries.
- Removed outliers based on unreasonable price-per-sqft thresholds.
- Normalized features by removing rare locations with few data points.
- Applied one-hot encoding to the `location` column (resulting in ~243 binary columns).
- Final features used for modeling:
  - `total_sqft`
  - `bath`
  - `bhk`
  - One-hot encoded location columns

---

## 4. Model Building

- **Model Used**: Linear Regression from scikit-learn.
- The dataset was split into training and test sets.
- Performance was evaluated using R² score and residual plots.
- The final model showed good generalization on validation data.

---

## 5. Saving the Model and Metadata

To make the model reusable in a web or API deployment, two files were generated:

### `bhp_model.pickle`
- This is a **serialized version of the trained model** using Python’s `pickle` module.
- It allows you to **load the model instantly** without retraining it.
- Usage:
  ```python
  import pickle
  with open('bhp_model.pickle', 'rb') as f:
      model = pickle.load(f)

# Credits

- This project is done by **Kumar Manik**.
