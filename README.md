🛒 E-Commerce Sales Analysis

A Python-based E-Commerce Sales Analysis project focused onunderstanding sales and profit performance using the SampleSuperstore dataset. The project uses Pandas for data preparationand analysis and Plotly for interactive visualizations.

📌 Project Overview

The goal of this project is to analyze e-commerce sales data andidentify patterns across:

Monthly sales

Product categories

Product sub-categories

Monthly profit

Profit by category

Customer segments

Sales-to-profit performance

The analysis is designed as a practical Data Analytics / Data Scienceproject using real-world-style retail transaction data.

🎯 Project Objectives

Calculate monthly sales and identify the highest- and lowest-salesmonths.

Analyze sales by product category and identify the highest- andlowest-sales categories.

Analyze sales at the sub-category level.

Calculate monthly profit and identify the highest-profit month.

Analyze profit by category and sub-category.

Analyze sales and profit by customer segment.

Analyze the sales-to-profit ratio.

📊 Dataset

The project uses the Sample - Superstore dataset.

Rows: 9,994

Columns: 21

Dataset type: Retail / E-Commerce transactions

Geography: United States

Main Columns

Column            Description

Order ID        Unique order identifierOrder Date      Date when the order was placedShip Date       Date when the order was shippedShip Mode       Shipping methodCustomer ID     Unique customer identifierCustomer Name   Customer nameSegment         Customer segmentCountry         CountryCity            Customer cityState           Customer stateRegion          Sales regionCategory        Product categorySub-Category    Product sub-categoryProduct Name    Product nameSales           Sales amountQuantity        Quantity soldDiscount        Discount appliedProfit          Profit generated

🛠️ Technologies & Libraries

Python

Pandas -- Data cleaning, transformation and analysis

Plotly Express -- Interactive charts

Plotly Graph Objects -- Advanced/custom visualizations

Jupyter Notebook -- Development and analysis environment

🔄 Project Workflow

1. Import Libraries

import pandas as pd
import plotly.express as px
import plotly.graph_objects as go
import plotly.io as pio
import plotly.colors as colors

2. Load the Dataset

data = pd.read_csv("Sample - Superstore.csv", encoding="latin1")

3. Explore the Data

The project uses:

data.head()
data.describe()
data.info()

to understand the dataset structure and statistical information.

4. Convert Date Columns

data['Order Date'] = pd.to_datetime(data['Order Date'])
data['Ship Date'] = pd.to_datetime(data['Ship Date'])

Additional date-based columns are created for analysis:

data['Order Month'] = data['Order Date'].dt.month
data['Order Year'] = data['Order Date'].dt.year
data['Order Day of Week'] = data['Order Date'].dt.dayofweek

📈 Analysis & Visualizations

Monthly Sales Analysis

Sales are grouped by month:

sales_by_month = data.groupby('Order Month')['Sales'].sum().reset_index()

A Plotly line chart is used to understand monthly sales trends.

Sales by Category

Sales_by_Category = data.groupby('Category')['Sales'].sum().reset_index()

A donut/pie chart is used to compare sales across product categories.

Sales by Sub-Category

sales_by_subcategory = data.groupby('Sub-Category')['Sales'].sum().reset_index()

A bar chart is used to compare sales across sub-categories.

Monthly Profit Analysis

profit_by_month = data.groupby('Order Month')['Profit'].sum().reset_index()

A line chart is used to analyze monthly profit trends.

Profit by Category

profit_by_category = data.groupby('Category')['Profit'].sum().reset_index()

A pie/donut chart is used to visualize profit contribution by category.

📊 Planned Business Questions

This project is structured around practical business questions such as:

Which month generates the most sales?

Which month generates the least sales?

Which product category performs best?

Which category has the lowest sales?

Which sub-categories contribute most to sales?

Which month generates the highest profit?

Which categories and sub-categories generate the most profit?

How do sales and profit differ across customer segments?

What is the relationship between sales and profit?

📁 Project Structure

E-Commerce-Sales-Analysis/
│
├── E-commerce project.ipynb
├── Sample - Superstore.csv
├── E-Commerece da.pdf
└── README.md

▶️ How to Run the Project

1. Clone the Repository

git clone https://github.com/your-username/E-Commerce-Sales-Analysis.git

2. Open the Project

Open the project folder in VS Code or Jupyter Notebook.

3. Install Required Libraries

pip install pandas plotly nbformat

4. Run the Notebook

Open:

E-commerce project.ipynb

Make sure Sample - Superstore.csv is in the same project folder beforerunning the notebook.

💡 Skills Demonstrated

Data loading and exploration

Data cleaning and preprocessing

Date/time transformation

Pandas groupby() operations

Aggregation and summarization

Sales analysis

Profit analysis

Category and sub-category analysis

Data visualization

Interactive charts with Plotly

Business-oriented data interpretation

🚀 Future Improvements

The project can be extended by adding:

Customer segment sales and profit analysis

Sales-to-profit ratio analysis

Regional performance analysis

Top and bottom performing products

Discount vs. profit analysis

Year-over-year sales comparison

KPI dashboard

Power BI dashboard integration

👨‍💻 Author

Akash Shende

Aspiring Data Analyst | Python | SQL | Power BI | Data Visualization# E-Commerce-Sales-Analysis
