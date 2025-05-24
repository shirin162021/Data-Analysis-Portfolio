# Data-Analysis-Portfolio
# Data Analysis Portfolio

Welcome to my Data Analysis Portfolio! This repository showcases my skills in data analysis, visualization, and machine learning using Python and associated libraries.

## Features
- Data Cleaning and Preprocessing
- Exploratory Data Analysis (EDA)
- Data Visualization
- Machine Learning Models (Regression, Classification, Clustering)

## Datasets
All datasets used are publicly available and included in the `/datasets` folder.

## Tools and Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Scikit-learn

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Data-Analysis-Portfolio.git
   pip install -r requirements.txt

---

#### **2. Dataset (Example: `/datasets/sales_data.csv`)**
Include sample datasets. Here’s a simple dataset example:

| Date       | Product   | Sales | Profit |
|------------|-----------|-------|--------|
| 2023-01-01 | Product A | 200   | 50     |
| 2023-01-02 | Product B | 300   | 80     |

---

#### **3. Python Script (Example: `/scripts/data_cleaning.py`)**
A script for cleaning data.
```python
import pandas as pd

# Load dataset
data = pd.read_csv('./datasets/sales_data.csv')

# Fill missing values
data.fillna(0, inplace=True)

# Convert date column to datetime
data['Date'] = pd.to_datetime(data['Date'])

# Save cleaned data
data.to_csv('./datasets/cleaned_sales_data.csv', index=False)

print("Data cleaning complete. Cleaned data saved.")

# Import libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
data = pd.read_csv('../datasets/cleaned_sales_data.csv')

# Sales distribution
plt.figure(figsize=(10, 6))
sns.histplot(data['Sales'], bins=20, kde=True)
plt.title("Sales Distribution")
plt.xlabel("Sales")
plt.ylabel("Frequency")
plt.show()

# Profit by Product
product_profit = data.groupby('Product')['Profit'].sum().reset_index()
sns.barplot(x='Product', y='Profit', data=product_profit)
plt.title("Profit by Product")
plt.show()


