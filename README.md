# From-Mess-to-Model-Bank-Churn-Data-Transformation-Insights
# Customer Churn Data Analysis

![Project Cover](cover_image.png)

## 🔍 About this Project
This project demonstrates a complete **data preparation and exploratory data analysis (EDA) workflow** using a fictional bank’s **customer churn dataset**.  
Starting from a raw, unstructured Excel file, the data was **cleaned, merged, and transformed** to prepare it for **predictive modeling** of churn behavior.

---

## 🧰 Tools & Technologies Used
- **Python**: Pandas, NumPy, Seaborn, Matplotlib  
- **Jupyter Notebook**: Interactive development  
- **Excel**: Original data source  

---

## 🎯 Key Objectives & Tasks

### ✅ Data Import & Quality Assurance
- Combined customer and account sheets via **left join** on `CustomerId`
- Removed duplicate rows and irrelevant columns
- Validated structure and completeness

### ✅ Data Cleaning
- Fixed inconsistent data types
- Cleaned currency fields (e.g., stripped `€`, converted to float)
- Handled missing values:
  - **Categorical** → filled with `"MISSING"`
  - **Numeric** (e.g., `-999999`) → replaced with median
- Standardized `Geography` values (e.g., `"FRA"`, `"French"` → `"France"`)

### ✅ Exploratory Data Analysis (EDA)
- **Bar charts**: churn vs. non-churn comparison
- **Categorical breakdown**: churn by Geography, Gender
- **Box plots & histograms**: CreditScore, Age, Balance, EstimatedSalary
- Identified skewed distributions and churn patterns

### ✅ Data Preparation for Modeling
- Dropped non-predictive fields (`CustomerId`, `Surname`)
- One-hot encoded `Geography`, `Gender`
- Engineered new feature:  
  `balance_v_income = Balance / EstimatedSalary`
- Visualized new feature for predictive potential

---

## 📊 Key Insights
- Higher churn rates in specific regions and certain age groups  
- **Balance-to-income ratio** indicated potential churn risk segments  
- Dataset is now **model-ready** for ML algorithms (e.g., logistic regression, decision trees)  

---
```

## 📂 Repository Structure
├── cover_image.png # Project cover photo
├── data/ # Raw and cleaned datasets
├── notebooks/ # Jupyter notebooks for EDA and cleaning
├── scripts/ # Python scripts for automation
├── README.md # Project documentation


```


## 🚀 Next Steps
- Build and evaluate **ML models** for churn prediction  
- Tune hyperparameters for improved performance  
- Deploy a dashboard for **interactive churn insights**

---

## 📜 License
This project is licensed under the **MIT License** – feel free to use and adapt.
