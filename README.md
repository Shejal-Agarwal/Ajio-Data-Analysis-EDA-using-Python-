# Ajio-Data-Analysis-EDA-using-Python-
Exploratory Data Analysis (EDA) of Ajio e-commerce dataset using Python. Includes data cleaning, preprocessing, visualization, and business insights on sales trends, returns, discounts, brands, and customer behavior.

Notebook Link: https://colab.research.google.com/drive/1uaLeqfGB_P7EJAP07ElTmn5HoBTECBxX#scrollTo=E0cEh_Dv0AHn
**Problem Statement**
Ajio is one of India’s leading fashion and lifestyle e-commerce platforms. The business challenge is to understand customer behavior, sales trends, product returns, and discounting patterns to drive data-informed decisions.

This analysis helps Ajio answer questions like:

Which categories and brands generate the highest sales?

What are the return rates across categories/brands?

How do discounts impact sales and returns?

Which brands contribute the most to revenue?

What customer segments are more profitable?

The objective is to derive insights for sales optimization, return reduction, and better pricing strategies.

**Steps Followed**

**Step 1**: Imported required Python libraries – pandas, numpy, matplotlib, seaborn, and plotly.

**Step 2**: Loaded Ajio datasets into Pandas DataFrames (Orders, Products, Customers, Delivery Partners, etc.).

**Step 3**: Conducted initial exploration using:

df.info()
df.describe()
df.isnull().sum()


Checked for missing values, duplicate entries, and data types.

**Step 4**: Cleaned and preprocessed data:

Removed duplicate records.

Replaced/handled null values.

Standardized column names for consistency.

**Step 5**: Created new calculated fields:

**Discount Percentage**

df['Discount_Percentage'] = ((df['Price'] - df['Final_Price']) / df['Price']) * 100

**Return Rate (by Category/Brand)**

return_rate = (df.groupby('Category')['Returned'].mean()) * 100

**Revenue Contribution per Brand**

revenue = df.groupby('Brand')['Final_Price'].sum()

**Step 6**: Performed Exploratory Data Analysis (EDA) with visualizations:

Sales by Category – Bar Chart

Top 10 Brands by Sales – Horizontal Bar Chart

Return % by Category/Brand – Pie/Bar Chart

Discount Impact on Sales – Scatter Plot

Customer Purchase Distribution – Histogram

**Step 7**: Added interactive charts using Plotly for better insights.

**Step 8**: Documented observations and linked them with business outcomes.

**Insights**
**[1] Sales Performance**

Top-selling categories are Apparel and Footwear.

A few brands dominate sales, contributing over 60% of total revenue.

**[2] Returns**

Return rates are highest in apparel, indicating size/fit issues.

Brands with high discounts also show higher return percentages.

**[3] Discounts**

Products with 30–50% discounts sell the most.

However, steeper discounts correlate with higher returns.

**[4] Customer Behavior**

Repeat customers are more likely to purchase during sale seasons.

Price-sensitive customers tend to return more often when discounts are higher.

**Tools & Libraries Used**
Python – Data Wrangling & EDA
Pandas, NumPy
Visualization – Matplotlib, Seaborn, Plotly
Jupyter Notebook – Documentation + Analysis
