# Task 1: Data Cleaning and Preprocessing using Python

## Project Overview

This project focuses on performing data cleaning and preprocessing on the **Mall Customer Segmentation Dataset** obtained from Kaggle. The objective is to prepare the raw dataset for further analysis by checking data quality, handling inconsistencies, and validating the dataset structure.

Data preprocessing is an essential step in the data science workflow because the quality of analysis depends on the quality of the data being used.

---

## Dataset Information

**Dataset Name:** Mall Customer Segmentation Dataset

**Source:** Kaggle

**File Used:** `Mall_Customers.csv`

### Dataset Features

| Column Name            | Description                                        |
| ---------------------- | -------------------------------------------------- |
| CustomerID             | Unique customer identifier                         |
| Gender                 | Customer gender                                    |
| Age                    | Customer age                                       |
| Annual Income (k$)     | Annual income in thousands of dollars              |
| Spending Score (1-100) | Score assigned based on customer spending behavior |

---

## Objectives

The main objectives of this project were:

* Load and inspect the dataset.
* Identify missing values.
* Check and remove duplicate records.
* Standardize column names.
* Verify data types.
* Validate categorical values.
* Export a cleaned dataset for future analysis.

---

## Technologies Used

* Python 3.x
* Pandas
* NumPy
* Jupyter Notebook / VS Code

---

## Data Cleaning Process

### 1. Import Required Libraries

The Pandas and NumPy libraries were imported to perform data manipulation and preprocessing tasks.

### 2. Load Dataset

The dataset was loaded into a Pandas DataFrame using:

```python
df = pd.read_csv("Mall_Customers.csv")
```

### 3. Initial Data Inspection

The dataset structure was examined using:

```python
df.head()
df.info()
df.shape
```

This helped understand the number of rows, columns, and data types.

### 4. Missing Value Analysis

Missing values were checked using:

```python
df.isnull().sum()
```

Result:

* No missing values were found in any column.

### 5. Duplicate Record Detection

Duplicate rows were checked using:

```python
df.duplicated().sum()
```

Result:

* No duplicate records were detected.

### 6. Column Name Standardization

Column names were reviewed and standardized to improve readability and consistency.

Example:

```text
CustomerID → customer_id
Annual Income (k$) → annual_income
Spending Score (1-100) → spending_score
```

### 7. Data Type Validation

Data types were verified using:

```python
df.dtypes
```

Result:

* Integer columns were stored correctly as numeric values.
* Gender was stored as a categorical/text column.

### 8. Categorical Value Verification

Unique values in the Gender column were examined:

```python
df["Gender"].unique()
```

Result:

```text
['Male', 'Female']
```

No inconsistencies were found.

### 9. Export Cleaned Dataset

The cleaned dataset was exported using:

```python
df.to_csv("cleaned_mall_customers.csv", index=False)
```

---

## Results

The dataset was successfully cleaned and validated.

### Key Findings

* No missing values were present.
* No duplicate records were found.
* Column names were standardized.
* Data types were verified.
* Categorical values were consistent.
* Dataset was ready for analysis and machine learning tasks.

---

## Output Files

```text
Mall_Customers.csv
cleaned_mall_customers.csv
```

---

## Project Structure

```text
Task1-Data-Cleaning/
│
├── Mall_Customers.csv
├── cleaned_mall_customers.csv
├── task1.ipynb
├── task1.py
└── README.md
```

---

## Conclusion

This project successfully demonstrated the complete data cleaning and preprocessing workflow using Python and Pandas. The dataset was inspected, validated, and prepared for further analysis. Proper preprocessing ensures reliable results in future data analysis, visualization, and machine learning tasks.
