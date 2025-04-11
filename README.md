# Online Retail Data Analysis

## 1. Project Overview

This project analyzes the Online Retail Dataset (UCI) using Python to perform data cleaning, create a pivot table, calculate key metrics, highlight top-performing countries, and visualize monthly revenue trends. The analysis aims to provide insights into sales performance and customer behavior.

## 2. Dataset

- [click here](https://archive.ics.uci.edu/dataset/352/online+retail)

###   2.1. Description

    The dataset used is the Online Retail Dataset (UCI), which contains transactional data for an online retail store, including customer information, product details, and sales quantities.



## 3. Files

## 3.1. Core Files

   * `online_retail_analysis.ipynb` (or similar name): This Jupyter Notebook contains the Python code for the data analysis.

    * `Online Retail.xlsx`: The dataset file used in the analysis.

    * `README.md`: This file, providing an overview of the project, methodology, and results.


## 4. Libraries and Dependencies

The following Python libraries are required to execute the code:

* `pandas`: For data manipulation and analysis.

* `matplotlib`: For creating visualizations.

* `seaborn`: For enhanced statistical visualizations.

* `openpyxl`: For reading and writing Excel files.


## 5. Methodology

##5.1. Data Loading

The dataset was loaded using `pd.read_excel()` from the specified file path (`/content/Online Retail.xlsx`). **Note:** This file path may need to be adjusted.

## 5.2. Data Cleaning

* **Missing Value Handling:** Rows with any missing values were removed using `df.dropna()` to ensure data integrity.

* **Duplicate Removal:** Duplicate rows were removed using `df.drop_duplicates()` to prevent redundant data.

* **Total Price Calculation:** A new column, `TotalPrice`, was calculated by multiplying the `Quantity` and `UnitPrice` columns.

* **Date Conversion and Month Extraction:**

    * The `InvoiceDate` column was converted to datetime objects using `pd.to_datetime()`.

    * A `YearMonth` column was created by extracting the year and month from the `InvoiceDate` and converting it to a string format (`YYYY-MM`).

## 5.3. Pivot Table Creation

A pivot table (`pivot_sales`) was created using `pd.pivot_table()` to summarize total sales by country and month:

* `index='Country'`: Country was used as the row index.

* `columns='YearMonth'`: YearMonth was used as the column index.

* `values='TotalPrice'`: TotalPrice was used as the values to aggregate.

* `aggfunc='sum'`: The sum of TotalPrice was calculated for each country and month combination.

* `fill_value=0`: Missing values in the pivot table were filled with 0.

## 5.4. Metric Calculations

* **Average Order Value (AOV):**
    * The total price for each order was calculated by grouping the data by `InvoiceNo` and summing the `TotalPrice`.

    * The average order value (`avg_order_value`) was calculated by taking the mean of these order totals.

* **Percentage Contribution of Each Country to Total Sales:**

    * Total sales for each country (`country_sales`) were calculated by grouping the data by `Country` and summing the `TotalPrice`.

    * The total sales across all countries (`total_sales`) were calculated.

    * The percentage contribution of each country (`country_sales_pct`) was calculated by dividing each country's sales by the total sales and multiplying by 100. The results were sorted in descending order.

## 5.5. Highlighting Top 5 Countries

* The total revenue for each country was sorted in descending order.

* A function (`highlight_top_5`) was defined to apply a background color (light green) to the top 5 countries based on their rank.

* The `style.apply()` method was used to apply this formatting to the DataFrame.

## 5.6. Monthly Revenue Trend Visualization

* Monthly revenue (`monthly_revenue`) was calculated by grouping the data by `YearMonth` and summing the `TotalPrice`.

* A line plot was created using `matplotlib.pyplot` and `seaborn.lineplot()` to visualize the monthly revenue trend.

* The plot includes:
    * Title: 'Monthly Revenue Trend'
    * X-axis label: 'Month'
    * Y-axis label: 'Revenue'
    * Markers to highlight data points
    * Rotated x-axis labels for readability
    * Gridlines

## 6. Results

_This section should contain a summary of the key findings from the analysis._

For example:

* "The pivot table provides a clear breakdown of monthly sales performance for each country."

* "The average order value was calculated to be \[Average Order Value]."

* "The percentage contribution analysis revealed that \[Top Country] contributed the most to total sales, followed by \[Second Top Country] and \[Third Top Country]."

* "The top 5 countries by revenue were highlighted, allowing for easy identification of key markets."

* "The monthly revenue trend chart shows \[Describe the trend, e.g., a general upward trend with seasonal fluctuations]."

## 7. Conclusion

This analysis provides insights into sales patterns, customer behavior, and key revenue contributors within the online retail business. The findings can be used to inform business decisions related to sales strategies, marketing efforts, and resource allocation.








