# Titanic Survival Prediction

This project aims to build a machine learning model to predict whether a passenger survived the Titanic shipwreck based on various features such as age, sex, fare, and passenger class.

---

## Project Overview

The Titanic dataset contains information about passengers onboard the Titanic, including their demographics and ticket details. The goal is to use this data to predict survival (binary classification problem).

This project involves the full machine learning pipeline: data cleaning, preprocessing, feature engineering, handling imbalanced classes, model building, and evaluation.

---

## Dataset Description

Key columns used:

- **Pclass:** Passenger ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
- **Sex:** Gender of the passenger
- **Age:** Age of passenger in years
- **Fare:** Ticket fare price
- **Embarked:** Port where the passenger boarded (C = Cherbourg, Q = Queenstown, S = Southampton)
- **Survived:** Target variable (0 = Did not survive, 1 = Survived)

---

## Step-by-Step Explanation

### 1. Data Loading and Initial Inspection
- Loaded the dataset using Pandas.
- Checked for missing values and overall data structure.

### 2. Data Cleaning
- Dropped irrelevant columns like `PassengerId`, `Name`, `Ticket`, and `Cabin` that do not contribute to survival prediction.
- Imputed missing values in `Age` with the median, and in `Embarked` with the mode (most frequent value).

### 3. Encoding Categorical Variables
- Converted categorical features `Sex` and `Embarked` into numerical format using Label Encoding to make them suitable for ML algorithms.

### 4. Feature Scaling
- Standardized `Age` and `Fare` features to have zero mean and unit variance. This improves model convergence and performance.

### 5. Handling Imbalanced Classes
- The dataset is imbalanced with fewer survivors.
- Applied **SMOTE (Synthetic Minority Oversampling Technique)** to create synthetic samples for the minority class, balancing the dataset for better model training.

### 6. Splitting the Data
- Split the dataset into training (80%) and testing (20%) sets to evaluate the model on unseen data.

### 7. Model Selection and Training
- Used **Random Forest Classifier**, a powerful ensemble model known for handling complex datasets and reducing overfitting.
- Set `class_weight='balanced'` to give equal importance to both survival classes.

### 8. Model Evaluation
- Predicted survival on the test set.
- Evaluated the model using:
  - **Accuracy:** Overall correctness of predictions.
  - **Precision:** How many predicted survivors were actually survivors.
  - **Recall:** How many actual survivors were correctly predicted.
- Presented results with a confusion matrix and classification report.

### 9. Feature Importance (Optional)
- Visualized feature importance to understand which factors influenced survival predictions the most (e.g., `Sex`, `Fare`, `Age`).

---

## Results

| Metric    | Score  |
|-----------|--------|
| Accuracy  | ~82%   |
| Precision | ~81%   |
| Recall    | ~77%   |

The model achieves solid predictive performance, balancing between identifying survivors correctly and minimizing false positives.

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/titanic-survival-prediction.git

---

## Contact & Contributions

I welcome feedback and collaboration.  
Feel free to connect:

- GitHub: [https://github.com/omkar1872](https://github.com/omkar1872)  
- LinkedIn: [https://linkedin.com/in/omkar1872](https://www.linkedin.com/in/omkar1872/)  
- Email: chomkar1872@gmail.com


---
