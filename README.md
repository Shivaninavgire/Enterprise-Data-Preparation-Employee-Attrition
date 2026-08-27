# Enterprise Data Preparation for Employee Attrition

## Project Overview

This project focuses on preparing an HR Employee Attrition dataset for data analysis and future machine learning applications. The main objective is to transform raw employee data into a clean, structured, and machine-learning-ready dataset.

Employee attrition is an important business concern because high employee turnover can increase recruitment costs, reduce productivity, and affect organizational performance. Proper data preparation helps ensure that future analysis and prediction models are based on reliable data.

## Project Objectives

The following tasks were performed:

* Import the HR employee dataset.
* Check and clean missing values.
* Identify and handle duplicate records.
* Detect and treat outliers.
* Remove unnecessary and constant columns.
* Encode categorical variables.
* Scale numerical variables.
* Create derived HR features.
* Build a preprocessing pipeline.
* Export the processed dataset.

## Dataset Information

The original dataset contains:

* 1,470 employee records
* 35 original features
* Numerical and categorical HR variables
* Employee Attrition as the target variable

The dataset includes employee information such as:

* Age
* Department
* Job Role
* Business Travel
* Monthly Income
* Job Satisfaction
* Work-Life Balance
* Total Working Years
* Years at Company
* Overtime
* Marital Status
* Attrition

## Data Preparation Process

### 1. Missing Value Handling

The dataset was checked for missing values.

**Result:** No missing values were found.

### 2. Duplicate Record Handling

The dataset was checked for duplicate employee records.

**Result:** No duplicate records were found.

### 3. Outlier Detection

Outliers were detected using the Interquartile Range (IQR) method. Important numerical HR features were examined using statistical boundaries and boxplots.

Extreme values were treated using capping where appropriate to preserve useful employee records.

### 4. Removal of Unnecessary Columns

Constant-value columns were removed because they do not provide useful information for attrition analysis.

The EmployeeNumber column was also removed because it is an identifier rather than a meaningful analytical feature.

### 5. Categorical Encoding

Categorical variables were transformed into numerical values using encoding techniques.

The preprocessing pipeline uses One-Hot Encoding for categorical features.

### 6. Feature Scaling

Numerical variables were standardized using StandardScaler.

This ensures that variables with larger ranges, such as MonthlyIncome, do not dominate variables with smaller ranges.

### 7. Feature Engineering

The following new features were created:

* IncomePerYearExperience
* PromotionDelayRatio
* CareerStabilityRatio
* ManagerStabilityRatio
* IncomePerJobLevel

These features provide additional insights into employee compensation, career stability, promotion history, and management relationships.

## Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## Project Structure

```text
Enterprise-Data-Preparation-Employee-Attrition/
│
├── Enterprise_Data_Preparation_Employee_Attrition.ipynb
├── HR_Employee_Attrition.csv
├── processed_employee_attrition_dataset.csv
├── Data_Cleaning_Report.md
├── Feature_Engineering_Report.md
├── Pipeline_Documentation.md
└── README.md
```

## Preprocessing Pipeline

The project uses Scikit-learn's Pipeline and ColumnTransformer.

### Numerical Pipeline

* Median imputation
* StandardScaler

### Categorical Pipeline

* Most frequent value imputation
* One-Hot Encoding
* Unknown category handling

The pipeline ensures that the same preprocessing steps can be applied consistently to future employee data.

## Output

The project produces a cleaned and processed employee attrition dataset that is suitable for:

* Exploratory Data Analysis
* HR Analytics
* Employee Retention Analysis
* Machine Learning
* Employee Attrition Prediction

## Conclusion

The HR dataset was successfully prepared through data cleaning, outlier handling, categorical encoding, numerical scaling, feature engineering, and preprocessing pipeline development.

The final dataset is structured and ready for further analysis and machine learning applications.

## Author

**Shivani Navgire**
B.Tech – Artificial Intelligence and Data Science

