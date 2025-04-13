# Predicting Insurance Charges

This project builds and evaluates a linear regression model to predict medical insurance charges based on demographic and lifestyle factors such as age, BMI, smoking status, and more.

## Data

Available in ```insurance.csv```

| Column    | Data Type | Description                                                      |
|-----------|-----------|------------------------------------------------------------------|
| `age`       | int       | Age of the primary beneficiary.                                  |
| `sex`       | object    | Gender of the insurance contractor (male or female).             |
| `bmi`       | float     | Body mass index, a key indicator of body fat based on height and weight. |
| `children`  | int       | Number of dependents covered by the insurance plan.              |
| `smoker`    | object    | Indicates whether the beneficiary smokes (yes or no).            |
| `region`    | object    | The beneficiary's residential area in the US, divided into four regions. |
| `charges`   | float     | Individual medical costs billed by health insurance.             |

## Data Cleaning

The cleaning process includes:

- Standardizing inconsistent sex labels (e.g., "M", "man" → "male")

- Removing dollar symbols from charges

- Dropping rows with invalid or missing data

- Fixing negative values in children

- Converting all region values to lowercase

## Model Training
A Linear Regression model is trained using the following steps:

- One-hot encoding for categorical variables: sex, smoker, region

- Standardization of numerical features: age, bmi, children

- Model evaluation using 5-fold cross-validation

-- Metrics: Mean Squared Error (MSE) and R² Score

## Predictions
After training, the model makes predictions on the validation dataset. Any prediction below $1000 is capped at $1000 as a minimum.

## Setup
To run the project on your local machine, follow these steps:

### Prerequisites:
Ensure you have the following installed:
- Python 3.x
- pip (Python package installer)

### Installation:
1. Clone the repository:
   ```
   git clone https://github.com/rd9437/predicting_insurance_consumption.git
   cd predicting_insurance_consumption 
   ```
