# Breast Cancer Prediction

## Project Overview

This project is focused on building a machine learning model to predict breast cancer based on various diagnostic features. The dataset contains medical information and diagnostic measurements that are used to classify tumors as malignant (`M`) or benign (`B`). The objective is to predict the malignancy of a tumor using a variety of classification algorithms and evaluate their performance.

## Dataset

The dataset used for this project comes from the **Wisconsin Breast Cancer Diagnostic (WBCD)** dataset. It consists of 569 samples, each representing a tumor, with 32 attributes (features) and a target label (Malignant or Benign).

### Data Attributes:

- `id`: An identifier for the sample (not used in model training).
- `diagnosis`: The target variable, which indicates whether the tumor is malignant (`M`) or benign (`B`).
- `feature_1`, `feature_2`, ..., `feature_n`: Various diagnostic features related to the tumor, such as radius, texture, perimeter, area, smoothness, compactness, concavity, symmetry, and fractal dimension of the tumor.

## Project Workflow

The project follows a typical machine learning pipeline:

1. **Data Preprocessing:**
   - Import the dataset and inspect for missing values.
   - Drop unnecessary columns (e.g., `id` and `Unnamed: 32`).
   - Handle missing or null values if present.
   - Encode the categorical target variable `diagnosis` using label encoding, where malignant (`M`) is represented as 1, and benign (`B`) is represented as 0.
   - Standardize the features using `StandardScaler` to improve model performance and convergence.

2. **Feature Selection:**
   - Perform feature selection to identify the most relevant features for prediction. This is done using univariate statistical tests (`f_classif` and `mutual_info_classif`).
   - Select the top features using `SelectPercentile` to improve model accuracy and reduce overfitting.

3. **Model Building and Evaluation:**
   - Train multiple machine learning models, including:
     - Logistic Regression
     - Decision Tree Classifier
     - Random Forest Classifier
   - Evaluate the models using performance metrics such as accuracy, precision, recall, and F1-score. These metrics help determine how well the models are able to distinguish between malignant and benign tumors.

4. **Model Performance Visualization:**
   - Use visualizations to understand feature distributions, model performance, and the importance of different features in predicting the target variable. Matplotlib and Seaborn are used to create informative plots.

## Author
Rohan Dhadwal
