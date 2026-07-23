# Titanic Survival Prediction using Logistic Regression

## Project Overview

This project is part of my Machine Learning Internship Task 4. The objective is to build a classification model that predicts whether a passenger survived the Titanic disaster based on passenger information.

The project includes data preprocessing, exploratory data analysis (EDA), feature engineering, model training, model evaluation, and hyperparameter tuning using Logistic Regression.

---

## Dataset

The project uses the famous Titanic dataset, which contains passenger information such as:

- Passenger Class (Pclass)
- Sex
- Age
- Number of Siblings/Spouses (SibSp)
- Number of Parents/Children (Parch)
- Fare
- Embarked Port
- Survival Status (Target Variable)

**Target Variable**

- 0 = Did Not Survive
- 1 = Survived

---

## Project Workflow

### 1. Data Loading

- Loaded the Titanic dataset using Pandas
- Explored the dataset using:
  - `head()`
  - `info()`
  - `describe()`
  - `shape()`

### 2. Data Cleaning

- Checked for duplicate records
- Identified missing values
- Filled missing numerical values using the **median**
- Filled missing categorical values using the **mode**

### 3. Exploratory Data Analysis (EDA)

Performed several visualizations:

- Age Distribution Histogram
- Boxplots for detecting outliers
- Survival Count by Gender
- Correlation Heatmap

### 4. Feature Engineering

Removed unnecessary columns:

- PassengerId
- Name
- Ticket
- Cabin

Encoded categorical variables:

- Sex
- Embarked

using **LabelEncoder**.

### 5. Model Building

- Split the dataset into training and testing sets
- Trained a Logistic Regression classifier

### 6. Model Evaluation

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Classification Report

### 7. Hyperparameter Tuning

Used **GridSearchCV** to tune the Logistic Regression model.

The following hyperparameters were optimized:

- C
- Solver
- Class Weight

The best model was selected using **5-fold cross-validation** with **F1-score** as the evaluation metric.

---

# Results

## Original Model

| Metric | Score |
|---------|------:|
| Accuracy | 81.01% |
| Precision | 78.57% |
| Recall | 74.32% |
| F1-Score | 76.39% |

## Tuned Model

| Metric | Score |
|---------|------:|
| Accuracy | 82.12% |
| Precision | 75.00% |
| Recall | 85.14% |
| F1-Score | 79.75% |

### Performance Comparison

The tuned Logistic Regression model achieved higher Accuracy, Recall, and F1-score compared to the original model. Although Precision decreased slightly, the overall improvement in Recall and F1-score indicates better classification performance.

### Why Accuracy Alone is Not Enough

Accuracy measures the overall percentage of correct predictions, but it can be misleading for imbalanced datasets. Precision, Recall, and F1-score provide a more complete evaluation by measuring how well the model identifies each class.

---

## Confusion Matrix

### Original Model

| Actual | Predicted | Count |
|---------|-----------|------:|
| Not Survived | Not Survived | 90 |
| Not Survived | Survived | 15 |
| Survived | Not Survived | 19 |
| Survived | Survived | 55 |

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Project Structure

├── neurofive-ml-track.ipynb
├── README.md


---

## Learning Outcomes

Through this project, I learned how to:

- Perform Exploratory Data Analysis (EDA)
- Handle missing values
- Encode categorical features
- Train a Logistic Regression model
- Evaluate a classification model using Accuracy, Precision, Recall, and F1-score
- Interpret a Confusion Matrix
- Perform Hyperparameter Tuning using GridSearchCV
- Compare the performance of original and tuned models

---

## Author

**Muhammad Maooz**

Machine Learning Intern
