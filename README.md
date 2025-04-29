# Property Price Prediction in Bengaluru

This project predicts property prices in various localities of Bengaluru, India, using machine learning. The model takes into account features such as square footage, number of bathrooms, number of bedrooms (BHK), and location to estimate the price of residential properties.

# Project Objectives

- Clean and preprocess the housing dataset.
- Engineer relevant features (e.g., converting textual square foot entries).
- Build a regression model to predict property prices.
- Serve predictions using a serialized model and location metadata.

# Dataset

- Source: [bengaluru_house_prices.csv]
- Size: ~1300+ records after cleaning
- Features used:
  - `total_sqft`
  - `bath`
  - `bhk`
  - `location` (one-hot encoded)

# Model Details

- **Model Used**: Linear Regression
- **Preprocessing**:
  - Cleaned inconsistent values in `total_sqft`
  - Removed outliers based on price per square foot
  - One-hot encoded locations (e.g., 'BTM Layout', 'Whitefield', etc.)
- **Target Variable**: Price (in lakhs)

# Credits

- This project is done by **Kumar Manik**.
