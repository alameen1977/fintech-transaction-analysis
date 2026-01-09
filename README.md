# Fintech Transaction Analysis

## Overview
This project is all about exploring a real-world retail transactions dataset and building a simple machine learning model to classify high-revenue transactions.  
Along the way, I cleaned the data, explored patterns, created features, and built a model — basically showing how data can tell a story.  
It’s my first full workflow project for a fintech/data internship, and it helped me practice **data cleaning, visualization, and ML modeling** end-to-end.

---

## About the Dataset
I used a retail transaction dataset (`projecttransaction.csv`) that has over 227,000 rows after cleaning.  
The columns include:

- `InvoiceNo` → Transaction ID  
- `StockCode` → Product code  
- `Description` → Product name/description  
- `Quantity` → Number of items  
- `InvoiceDate` → Date and time of transaction  
- `UnitPrice` → Price per item  
- `CustomerID` → Customer identifier (some missing values)  
- `Country` → Country of purchase

---

## Steps I Took

### 1. Data Cleaning
- Converted `InvoiceDate` to datetime for easier analysis  
- Filled missing values in `Description` and `CustomerID`  
- Removed rows with negative `Quantity` or `UnitPrice`  
- Created a new column `Revenue` = `Quantity * UnitPrice`

### 2. Exploratory Data Analysis (EDA)
- Calculated total revenue  
- Found top-selling products  
- Checked revenue per country  
- Explored monthly revenue trends  
- Created bar charts and line charts to visualize patterns

### 3. Machine Learning (Classification)
- Converted the revenue prediction into **High / Low Revenue** classification using the median revenue as a threshold  
- Used `Quantity` and `UnitPrice` as input features  
- Trained a **Logistic Regression** model  
- Evaluated the model using **Accuracy, Precision, Recall, F1-score**  
- Achieved **84% accuracy** with balanced performance across both classes

---

## What I Learned / Key Insights
- The model can classify high vs low revenue transactions reasonably well  
- Monthly and product-level trends show interesting patterns in sales  
- Working on this project helped me understand **data cleaning → EDA → feature engineering → ML workflow** in a practical way  

---

## Tools & Libraries
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn (Logistic Regression, train-test split, evaluation metrics)  
- Jupyter Notebook  

---

## How to Run This Project
1. Clone my repository:  
   ```bash
   git clone https://github.com/alameen1977/fintech-transaction-analysis.git

