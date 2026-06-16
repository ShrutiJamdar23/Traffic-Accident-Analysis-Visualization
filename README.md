# Traffic Accident Severity Prediction using Decision Tree Classifier

## Project Overview

This project implements a Decision Tree Classification model to predict the severity of traffic accidents based on environmental and road-related factors. The model analyzes accident conditions such as time of occurrence, weather conditions, and road conditions to classify accident severity levels.

The project demonstrates the complete machine learning workflow, including data preprocessing, model training, evaluation, feature importance analysis, and decision tree visualization.

---

## Objective

The main objective of this project is to predict accident severity using historical traffic accident data and identify the factors that contribute most to accident outcomes.

---

## Dataset Information

The dataset contains traffic accident records with the following features:

| Feature        | Description                               |
| -------------- | ----------------------------------------- |
| Time           | Time of accident occurrence               |
| Weather        | Weather condition during the accident     |
| Road_Condition | Condition of the road surface             |
| Severity       | Accident severity level (Target Variable) |

### Dataset Statistics

* Total Records: 50
* Total Features: 3
* Target Variable: Severity
* Classification Type: Multi-Class Classification

---

## Technologies Used

* Python
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

---

## Project Workflow

### 1. Data Loading

* Loaded the traffic accident dataset using Pandas.
* Examined dataset dimensions and sample records.

### 2. Data Preprocessing

Since all input features are categorical:

* Missing values handled using the most frequent value strategy.
* Categorical features converted into numerical format using One-Hot Encoding.
* Built preprocessing pipelines using Scikit-learn.

### 3. Train-Test Split

The dataset was divided into:

* Training Set: 70%
* Testing Set: 30%

Stratified sampling was used to preserve the class distribution of accident severity levels.

### 4. Model Training

A Decision Tree Classifier was trained with:

* Maximum Tree Depth: 4
* Random State: 42

The preprocessing pipeline and classifier were combined into a single machine learning pipeline.

### 5. Model Evaluation

The trained model was evaluated using:

* Accuracy Score
* Confusion Matrix
* Precision
* Recall
* F1-Score
* Classification Report

---

## Results

### Model Accuracy

Accuracy: **40%**

### Confusion Matrix

| Actual / Predicted | Severity 1 | Severity 2 | Severity 3 |
| ------------------ | ---------- | ---------- | ---------- |
| Severity 1         | 3          | 1          | 1          |
| Severity 2         | 1          | 0          | 3          |
| Severity 3         | 3          | 0          | 3          |

### Classification Report

| Severity Level | Precision | Recall | F1-Score |
| -------------- | --------- | ------ | -------- |
| 1              | 0.43      | 0.60   | 0.50     |
| 2              | 0.00      | 0.00   | 0.00     |
| 3              | 0.43      | 0.50   | 0.46     |

### Overall Performance

* Accuracy: 40%
* Macro Average F1-Score: 0.32
* Weighted Average F1-Score: 0.35

---

## Feature Importance Analysis

The project calculates feature importance scores from the trained Decision Tree model.

Feature importance visualization helps identify which accident factors have the greatest impact on severity prediction.

Possible influential factors include:

* Weather Conditions
* Road Conditions
* Time of Accident

---

## Visualizations

### Feature Importance Plot

A bar chart displaying the importance of encoded features generated after One-Hot Encoding.

### Decision Tree Visualization

A graphical representation of the trained Decision Tree showing:

* Decision rules
* Splitting criteria
* Severity classifications
* Prediction paths

This visualization improves model interpretability and helps understand how predictions are made.

---

## Observations

* The dataset is relatively small with only 50 records.
* The model achieved moderate performance due to limited training data.
* Severity Level 2 was difficult for the model to classify correctly.
* Increasing dataset size would likely improve model accuracy and generalization.

---

## Conclusion

This project demonstrates how Decision Tree Classification can be applied to predict traffic accident severity using categorical environmental factors. While the current model achieved an accuracy of 40%, it provides valuable insights into accident patterns and highlights the importance of data quantity and quality in machine learning applications.

The project serves as a practical example of classification, preprocessing pipelines, feature engineering, and model visualization using Scikit-learn.

---

## Future Improvements

* Collect a larger traffic accident dataset.
* Include additional features such as:

  * Vehicle Speed
  * Driver Age
  * Traffic Density
  * Lighting Conditions
  * Location Information
* Perform hyperparameter tuning using GridSearchCV.
* Compare Decision Tree performance with:

  * Random Forest
  * XGBoost
  * Gradient Boosting
  * Logistic Regression
* Apply Cross-Validation for more reliable evaluation.
* Deploy the model using Flask or Streamlit for real-time predictions.
