# HR Attrition Analysis

## Project Overview

This project focuses on understanding employee attrition at IBM through statistical analysis and machine learning models. By leveraging various statistical tests and machine learning algorithms, we aim to identify the key drivers behind employee attrition and develop predictive models to help HR teams proactively manage employee retention.

## Key Features
- **Data Preprocessing**: Dropped irrelevant columns, handled missing values, and performed feature engineering to prepare the data for analysis.
- **Statistical Analysis**: Used chi-squared and Wilcoxon rank sum tests along with effect size measures to identify important features influencing attrition.
- **Exploratory Data Analysis (EDA)**: Visualized relationships between attrition and variables like Business Travel, Job Role, Marital Status, and OverTime using barplots and treemaps.
- **Feature Selection**: Conducted feature selection using step-wise addition and bootstrapping to identify the most relevant predictors of attrition.
- **Machine Learning Models**: Trained and evaluated multiple machine learning models, including Generalized Linear Model (GLM), K-Nearest Neighbors (KNN), and XGBoost, using downsampling and SMOTE to address class imbalance.
- **Model Evaluation**: Evaluated model performance using metrics like accuracy, specificity, and sensitivity, with a focus on predicting the likelihood of employee attrition.

## Repository Structure

```plaintext
|
|-- denis_stashkevich_hr_attrition.Rmd   # R markdown file for detailed analysis.
|-- denis_stashkevich_hr_attrition.pdf   # PDF report summarizing analysis and findings.
|-- WA_Fn-UseC_-HR-Employee-Attrition.csv # Dataset used for the project.
|-- best_knn_downsampled.rds             # Saved KNN model using downsampling.
|-- best_xgb_downsampled.rds             # Saved XGBoost model using downsampling.
|-- best_xgb_smote.rds                   # Saved XGBoost model using SMOTE.
|-- glm_specs.rds                        # GLM model specifications.
|-- knn_specs.rds                        # KNN model specifications.
|-- xgb_specs.rds                        # XGBoost model specifications.
|-- vector_of_formulas.rds               # Bootstrapped formulas for feature selection.
Dependencies
To run this project, you will need the following dependencies:

R
tidyverse
data.table
rcompanion
effsize
roperators
future.apply
dqrng
tidymodels
themis
caret
treemapify
gridExtra
FactoMineR
Data Preparation
The dataset consists of employee records, including various personal, professional, and performance attributes. The key steps taken include:

Loading the dataset from WA_Fn-UseC_-HR-Employee-Attrition.csv.
Dropping irrelevant columns (e.g., Over18, EmployeeNumber).
Handling missing values and encoding categorical variables.
Identifying significant features through statistical testing.
Statistical Analysis
Feature Selection
Categorical Data: Chi-squared tests and Cohen's W were used to measure the association between categorical variables and attrition.
Numerical Data: Wilcoxon rank sum tests and Vargha and Delaney’s A were applied to compare groups.
Correction for Type I Error: False Discovery Rate (FDR) was used to adjust p-values.
Exploratory Analysis
Visualized attrition relationships with various features, such as:
Business Travel: Increased frequency of travel was associated with higher attrition.
Job Role: Sales Representatives showed the highest attrition rate.
OverTime: Employees working overtime were more likely to leave.
Machine Learning Models
GLM (Logistic Regression): Used for its interpretability and to establish relationships between features and attrition.
K-Nearest Neighbors (KNN): Applied to classify employees into high and low-risk attrition categories.
XGBoost: A powerful classifier used for enhanced prediction and understanding feature importance.
Class Balancing
Used downsampling and SMOTE to deal with class imbalance in attrition data.
Evaluation Metrics
Accuracy: The percentage of correct predictions.
Specificity: The model's ability to correctly identify non-attrition cases.
Sensitivity: The model's ability to correctly identify attrition cases.
Results
Key Drivers of Attrition: Features such as OverTime, Job Role, Marital Status, Environment Satisfaction, and Business Travel were significant predictors.
Model Performance: KNN and XGBoost showed similar performance, with downsampling being more effective than SMOTE for class balancing.
Future Improvements
Feature Expansion: Include external data such as sentiment analysis or additional personal factors.
Dimensionality Reduction: Further explore PCA for reducing data dimensions and improving model efficiency.
Deployment: Deploy the model for real-time employee attrition prediction.
How to Use
Clone the Repository:
sh
Копировать код
git clone <repository-url>
Install Dependencies: Install required R packages mentioned in the Dependencies section.
Run Analysis: Execute the R markdown file (denis_stashkevich_hr_attrition.Rmd) to replicate the analysis.
Model Training: Pre-trained models are saved in .rds files, and model evaluation results are documented in the report.
References
Tidymodels Documentation: https://www.tidymodels.org/
XGBoost Documentation: https://xgboost.readthedocs.io/
