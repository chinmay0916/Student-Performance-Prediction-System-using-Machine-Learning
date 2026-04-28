# Student Performance Analysis

## Introduction
This project aims to analyze student performance using a dataset from a Portuguese secondary school. The primary goal is to predict whether a student will pass or fail their final exam (G3) based on various demographic, social, and school-related features. The analysis involves exploratory data analysis (EDA), data preprocessing, training several machine learning models, and evaluating their performance.

## Dataset
The dataset used is the UCI Student Performance Data Set, specifically `student-mat.csv`, focusing on mathematics students. It contains 395 student records with 33 features, including:
- Demographic information (e.g., age, sex, address, family size)
- Social factors (e.g., parental education, job, family relationship, going out, alcohol consumption)
- School-related attributes (e.g., travel time, study time, past failures, school support, extra paid classes, internet access, desire for higher education)
- Academic performance (G1 - first period grade, G2 - second period grade, G3 - final grade).

## Methodology
1.  **Data Loading & Overview**: The dataset was loaded and a summary of numerical features and missing values was generated. The target variable `G3` (final grade) was analyzed.
2.  **Grade Labeling**: Custom grade labels ('A' to 'F') and a binary 'Pass'/'Fail' (G3 >= 10) indicator were created from the `G3` score.
3.  **Exploratory Data Analysis (EDA)**: Various visualizations were generated to understand the distributions of grades, the relationship between different features (study time, failures, gender, absences, internet access, desire for higher education) and the final grade, and feature correlations.
4.  **Data Preprocessing**: Categorical features were encoded using `LabelEncoder`, and numerical features were scaled using `StandardScaler`.
5.  **Feature Selection & Splitting**: A set of 28 features was selected, and the data was split into training (80%) and testing (20%) sets, with stratification based on the 'Pass' target variable.
6.  **Model Training & Evaluation**: The following machine learning models were trained and evaluated:
    - Logistic Regression
    - Decision Tree Classifier
    - Random Forest Classifier
    - Gaussian Naive Bayes
    - Support Vector Machine (SVM)
    Each model's test accuracy and 5-fold cross-validation accuracy were calculated, along with classification reports.
7.  **Results Visualization**: Confusion matrices, accuracy comparison plots, and feature importance (for Random Forest) were generated to visualize model performance.
8.  **Sample Prediction**: The best-performing model was used to predict outcomes for a few sample students.

## Key Findings
-   **Best Model**: The **Random Forest Classifier** achieved the highest test accuracy of **84.81%**.
-   **Pass Rate**: Approximately **46.6%** of students passed the final exam (G3 >= 10).
-   **Important Features**: G1 and G2 (first and second period grades) were identified as the most important features for predicting the final grade outcome, followed by past failures and absences.
-   **Visualizations**: Several plots (`minor1_eda.png`, `minor1_model_results.png`, `minor1_summary.png`) were created to illustrate the findings.
