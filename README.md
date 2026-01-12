# 🧹 Data Cleaning Using Python Pandas (Real-World Zomato Dataset)

## 📌 Project Overview

Data cleaning is one of the most critical steps in any data pipeline. Real-world datasets are often messy, incomplete, and inconsistent, which directly impacts the quality of downstream analytics and machine learning models.

This project demonstrates a **step-by-step data cleaning workflow using Python and Pandas** on a real-world dataset sourced from Kaggle. The focus is on identifying data quality issues and applying practical cleaning techniques to transform raw data into a structured, analysis-ready format.

The project follows a hands-on approach inspired by a detailed Pandas data cleaning tutorial and reflects industry-relevant practices used in data engineering and analytics workflows.

---

## 🎯 Objectives

- Understand the structure and quality of a real-world dataset  
- Identify missing, inconsistent, and duplicate data  
- Apply Pandas-based cleaning and transformation techniques  
- Prepare a clean dataset suitable for accurate analysis and reporting  

---

## 🛠️ Tech Stack

- **Language:** Python  
- **Libraries:**  
  - Pandas   
- **Environment:** Jupyter Notebook  
- **Dataset Source:** Kaggle  

---

## 📂 Dataset Information

- **Source:** Kaggle  
- **Type:** CSV dataset  
- **Nature:** Real-world, semi-structured data  
- **Common Data Issues Found:**
  - Missing values  
  - Incorrect data types  
  - Duplicate records  
  - Inconsistent text formats  

The dataset was loaded into a Pandas DataFrame and analyzed to understand its schema, data types, and overall quality before applying any transformations.

---

## 🔍 Data Exploration (Data Card)

Initial data exploration was performed to understand the dataset structure and identify potential issues.

Key steps included:
- Viewing sample records using `head()` and `tail()`
- Inspecting schema and null counts using `info()`
- Generating statistical summaries with `describe()`
- Verifying column data types using `dtypes`

This step helped in deciding the appropriate cleaning strategies for each column.

---

## 🧼 Data Cleaning Workflow

### 1️⃣ Handling Missing Values

- Identified missing values using:
  ```python
  df.isnull().sum()
  ```
Applied appropriate strategies based on column context:

- Dropping rows or columns with excessive null values  
- Filling missing values using **mean**, **median**, or **mode**  
- Using constant or placeholder values where applicable  

---

### 2️⃣ Data Type Corrections

- Converted incorrect data types to their appropriate formats  
- Parsed date columns into `datetime` format  
- Ensured numerical columns were stored as numeric types for accurate calculations  

**Example:**
```python
df['column_name'] = df['column_name'].astype(int)
```
---

### 3️⃣ Duplicate Record Handling

- Identified duplicate rows using:
```python
df.duplicated().sum()
```
- Removed duplicate entries to maintain data integrity:
```python
df.drop_duplicates(inplace=True)
```
---

### 4️⃣ Column Renaming and Standardization

- Renamed columns for clarity and consistency  
- Applied standard naming conventions (lowercase, underscores)  
- Improved readability and usability for downstream processes  

---

### 5️⃣ Text Data Cleaning

- Trimmed unnecessary whitespaces  
- Standardized inconsistent text values  
- Applied string transformations using Pandas string methods  

---

### 6️⃣ Data Optimization

- Removed unnecessary columns  
- Reduced memory usage where possible  
- Prepared the dataset for efficient analysis and visualization

---

## 📊 Outcome

- Raw dataset transformed into a clean, structured format  
- Improved data consistency and reliability  
- Dataset ready for analysis, visualization, or machine learning use cases  

---

## 📚 Key Learnings

- Importance of data profiling before cleaning  
- Practical handling of missing and inconsistent data  
- Efficient use of Pandas for real-world data preparation  
- How clean data directly improves analysis accuracy  

