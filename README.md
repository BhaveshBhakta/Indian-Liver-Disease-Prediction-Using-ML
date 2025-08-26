## Indian Liver Disease Prediction

### Project Overview

This project aims to predict the **presence of liver disease** based on various blood test parameters and demographic information. By analyzing features such as age, gender, and the concentrations of various liver enzymes and proteins, the goal is to develop a machine learning model that can accurately classify a patient's liver disease status. This can assist in early diagnosis and management of liver-related illnesses.

-----

### Technical Highlights

  * **Dataset**: The dataset used is 'indian\_liver\_patient.csv', containing patient records.
  * **Size**: 583 entries, 11 columns.
  * **Key Features**:
      * **Demographics**: `Age`, `Gender`.
      * **Lab Results**: `Total_Bilirubin`, `Direct_Bilirubin`, `Alkaline_Phosphotase`, `Alamine_Aminotransferase`, `Aspartate_Aminotransferase`, `Total_Protiens`, `Albumin`, `Albumin_and_Globulin_Ratio`.
  * **Approach**:
      * **Data Cleaning**: The code drops duplicate rows and rows with missing values (`NaN`) in the `Albumin_and_Globulin_Ratio` column.
      * **Exploratory Data Analysis**: Histograms and boxplots were used to visualize the distribution of numerical features, while count plots were created for categorical features.
      * **Label Encoding**: All columns were converted to numerical format using `LabelEncoder`.
      * **Handling Class Imbalance**: The original dataset is imbalanced (416 positive vs 167 negative). `SMOTE` was applied to the training data to balance the classes.
      * **Binary Classification**: The target variable `Dataset` indicates the presence of liver disease (1) or not (0).
      * **Models Used**:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * **71.1%** with AdaBoost Classifier.
      * **68.4%** with XGBoost Classifier.
      * **65.8%** with Logistic Regression, Ridge Classifier, and Bagging Classifier.
      * The accuracies are moderate, suggesting that predicting liver disease from these features is a challenging task, and more data or different features might be needed.

-----

### Purpose and Applications

  * Assist medical professionals in the **early diagnosis and screening of liver disease**.
  * Support public health initiatives by enabling a better understanding of liver disease risk factors.
  * Provide a tool for educational purposes in medical data analysis.
  * Serve as a foundational model for developing more comprehensive liver health prediction systems.

-----

### Installation

Clone the repository and download the dataset.

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn imbalanced-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Performing comprehensive hyperparameter tuning and cross-validation for all models to achieve optimal performance.
  * Exploring more advanced strategies for handling class imbalance.
  * Investigating the impact of different feature selection or transformation techniques on model performance.
  * Adding explainability (e.g., SHAP or LIME) to understand which lab parameters are the most critical for liver disease prediction.
