# Titanic Survival Prediction using Logistic Regression

## Project Overview

This project is part of my Machine Learning Internship Task 3. The objective is to build a classification model that predicts whether a passenger survived the Titanic disaster based on passenger information.

The project includes data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and performance evaluation using Logistic Regression.

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

**Target Variable:**

- 0 = Did Not Survive
- 1 = Survived

## Project Workflow

### 1. Data Loading

- Loaded the Titanic dataset using Pandas.
- Explored the dataset using:
  - `head()`
  - `info()`
  - `describe()`
  - `shape()`

### 2. Data Cleaning

- Checked for duplicate records.
- Identified missing values.
- Filled missing numerical values using the **median**.
- Filled missing categorical values using the **mode**.

### 3. Exploratory Data Analysis (EDA)

Performed several visualizations to better understand the dataset:

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

Split the dataset into training and testing sets using `train_test_split`.

Trained a **Logistic Regression** model to predict passenger survival.

### 6. Model Evaluation

The model was evaluated using:

- Accuracy Score
- Confusion Matrix


## Results

**Model Used**

- Logistic Regression

**Model Accuracy**
81.01%


### Confusion Matrix
Not Survived → Not Survived | Correct | 90 |
Not Survived → Survived | Incorrect | 15 |
Survived → Not Survived | Incorrect | 19 |
Survived → Survived | Correct | 55 |

The model correctly classified most passengers, achieving an accuracy of approximately **81%**. Most predictions fall on the main diagonal of the confusion matrix, indicating good overall performance.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn


## Project Structure

├── train.csv
├── neurofive-ml-track.ipynb
├── README.md

## Learning Outcomes

Through this project, I learned how to:

- Perform Exploratory Data Analysis (EDA)
- Handle missing values
- Encode categorical features
- Split data into training and testing sets
- Train a Logistic Regression classification model
- Evaluate model performance using Accuracy Score and Confusion Matrix
- Interpret machine learning results


## Author

**Muhammad Maooz**

Machine Learning Intern
