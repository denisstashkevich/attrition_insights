# HR Attrition Analysis

<h2 align="center" style="color:blue">Project Description</h2>

This project focuses on understanding employee attrition at IBM through statistical analysis and machine learning models. By leveraging various statistical tests and machine learning algorithms, we aim to identify the key drivers behind employee attrition and develop predictive models to help HR teams proactively manage employee retention.

<h2 align="center" style="color:blue">Project Structure</h2>

1. **Data Loading**
2. **Exploratory Data Analysis and Cleaning**
    - Handling Missing Values
    - Removing Duplicates
    - Cleaning Numerical and Categorical Features
    - Outlier Analysis
3. **Feature Engineering**
    - Creating New Features
    - Encoding Categorical Variables
    - Feature Selection and Multicollinearity Check
4. **Model Building**
    - Generalized Linear Model (GLM)
    - K-Nearest Neighbors (KNN)
    - XGBoost Regression
5. **Model Evaluation and Results Analysis**
    - Model Performance Metrics
    - Residual Analysis
    - Identifying Extreme Errors

<h2 align="center" style="color:blue">Technologies and Libraries</h2>

- R
- tidyverse
- data.table
- rcompanion
- effsize
- roperators
- future.apply
- dqrng
- tidymodels
- themis
- caret
- treemapify
- gridExtra
- FactoMineR

<h2 align="center" style="color:blue">Installation</h2>

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/yourusername/HR-Attrition-Analysis.git
    cd HR-Attrition-Analysis
    ```

2. **Install Dependencies:**

    Install the required R packages listed in the Dependencies section. You can install them using the following R script:

    ```r
    install.packages(c(
      "tidyverse",
      "data.table",
      "rcompanion",
      "effsize",
      "roperators",
      "future.apply",
      "dqrng",
      "tidymodels",
      "themis",
      "caret",
      "treemapify",
      "gridExtra",
      "FactoMineR"
    ))
    ```

    Alternatively, you can install them individually:

    ```r
    install.packages("tidyverse")
    install.packages("data.table")
    install.packages("rcompanion")
    install.packages("effsize")
    install.packages("roperators")
    install.packages("future.apply")
    install.packages("dqrng")
    install.packages("tidymodels")
    install.packages("themis")
    install.packages("caret")
    install.packages("treemapify")
    install.packages("gridExtra")
    install.packages("FactoMineR")
    ```

<h2 align="center" style="color:blue">Usage</h2>

1. **Data Preparation:**

    Ensure that the `WA_Fn-UseC_-HR-Employee-Attrition.csv` file is located in the root directory of the project.

2. **Run Analysis:**

    Execute the R Markdown file to replicate the analysis. Open RStudio and run the following command or use the RStudio interface to knit the document.

    ```bash
    Rscript -e "rmarkdown::render('denis_stashkevich_hr_attrition.Rmd')"
    ```

3. **Model Training:**

    - Pre-trained models are saved in `.rds` files.
    - Model evaluation results are documented in the PDF report (`denis_stashkevich_hr_attrition.pdf`).

<h2 align="center" style="color:blue">Data Description</h2>

- **age**: Age of the employee.
- **income_lakhs**: Annual income in lakhs.
- **number_of_dependants**: Number of dependents.
- **gender**: Gender.
- **region**: Region of residence.
- **marital_status**: Marital status.
- **bmi_category**: Body Mass Index category.
- **smoking_status**: Smoking status.
- **employment_status**: Employment status.
- **income_level**: Income level.
- **medical_history**: Medical history.
- **insurance_plan**: Insurance plan.
- **annual_premium_amount**: Annual premium amount (target variable).

<h2 align="center" style="color:blue">Methodology</h2>

1. **Data Loading and Preprocessing:**
    - Import libraries.
    - Load data from `WA_Fn-UseC_-HR-Employee-Attrition.csv`.
    - Clean column names (convert to lowercase and replace spaces with underscores).

2. **Exploratory Data Analysis (EDA):**
    - Analyze missing values and duplicates.
    - Statistical description of data.
    - Handle anomalies and outliers in `age` and `income_lakhs` features.
    - Visualize distributions and relationships between features.

3. **Feature Engineering:**
    - Create `total_risk_score` based on medical history.
    - Normalize the risk score.
    - Encode categorical variables using one-hot encoding.
    - Feature selection and removal of multicollinear features with high VIF.

4. **Model Building and Evaluation:**
    - Split data into training and testing sets.
    - Train Generalized Linear Model (GLM), K-Nearest Neighbors (KNN), and XGBoost models.
    - Evaluate models using Accuracy, Specificity, and Sensitivity metrics.
    - Hyperparameter tuning for XGBoost using RandomizedSearchCV.
    - Analyze feature importance and residuals.

<h2 align="center" style="color:blue">Results</h2>

- **Generalized Linear Model (GLM):**
    - Model coefficients visualized to understand the impact of each feature.
    - Performance metrics: Accuracy, Specificity, Sensitivity.

- **K-Nearest Neighbors (KNN):**
    - Improved performance metrics compared to GLM.
    - Effective in classifying high and low-risk attrition categories.

- **XGBoost Regression:**
    - Best performance metrics after hyperparameter tuning.
    - Feature importance displayed for model interpretation.
    - Residual analysis identified 30% extreme errors associated with specific employee segments.

<h2 align="center" style="color:blue">Conclusion</h2>

The project demonstrates a complete data analysis and modeling pipeline for predicting employee attrition. Key factors influencing attrition were identified, and model errors were analyzed, suggesting potential improvements such as building separate models for specific employee segments.


<h2 align="center" style="color:blue">References</h2>

- [Tidymodels Documentation](https://www.tidymodels.org/)
- [XGBoost Documentation](https://xgboost.readthedocs.io/)
- [Caret Package Documentation](https://topepo.github.io/caret/)
- [SMOTE Technique](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html)

