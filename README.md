# superstore-dataset-Retail
The main aim of this project is to analyze customer purchasing patterns, sales performance, and profitability using retail sales data to uncover meaningful business insights and support data-driven decision-making.


Dataset Information:-

Dataset Name: Superstore Dataset Final

Domain: Retail Sales Analytics

Source: Kaggle

Dataset Type: Structured CSV Dataset


Project Objectives :-

* Analyze overall sales performance across different categories, regions, and time periods.

* Evaluate profitability by identifying the most and least profitable products and categories.

* Study customer segments to understand purchasing behavior among Consumer, Corporate, and Home Office customers.

* Compare regional performance to identify top-performing and underperforming regions, states, and cities.

* Examine the impact of discounts on sales and profit to determine effective pricing strategies.

* Perform exploratory data analysis (EDA) to discover patterns, trends, and relationships within the dataset.

* Generate data-driven business recommendations to improve sales, profitability, and decision-making.

Phase 1 Report: Data Loading, Initial Overview

## Introduction

The first phase of the Superstore Sales Analysis project focused on understanding the dataset and preparing it for further analysis. This phase involved loading the dataset, exploring its structure, and performing necessary data cleaning and preprocessing operations to ensure data quality and consistency.

## 1. Data Loading and Initial Overview

The Superstore dataset was imported using the Pandas library in Python. Initial exploration was performed to understand the dataset's structure and contents.

### Procedures Performed

* Loaded the dataset into a Pandas DataFrame using `pd.read_excel()`.
* Determined the total number of rows and columns using the `shape` attribute.
* Examined column names and data types using the `info()` function.
* Viewed the first few records using `head()` to understand the dataset format.
* Generated descriptive statistics using `describe()` to summarize numerical variables.

### Observations

* The dataset contains sales transaction records including customer, product, order, shipping, and profit information.
* Numerical columns such as Sales, Quantity, Discount, and Profit were identified for statistical analysis.
* Categorical columns such as Category, Sub-Category, Region, and Segment were identified for grouping and comparison purposes.
# Phase 2 Report: Data Pre-processing

## Introduction

The second phase of the Superstore Sales Analysis project focused on data preprocessing. The primary objective was to clean, transform, and prepare the dataset for exploratory analysis. This phase ensured data quality, consistency, and reliability by handling potential issues and creating additional features that support deeper business analysis.

## 2. Data Pre-processing

Several preprocessing techniques were applied to the Superstore dataset to improve its usability and analytical value.

### 2.1 Handling Missing Values

The dataset was examined for missing or null values to ensure data completeness.

#### Procedures Performed

* Checked all columns for missing values using isnull().sum().
* Verified whether any null values existed in the dataset.

#### Outcome

* The dataset not contained any missing values.
* Data quality was maintained for accurate analysis.

### 2.2 Removing Duplicate Records

Duplicate records can affect statistical calculations and business insights.

#### Procedures Performed

* Identified duplicate entries using the `duplicated()` function.
* Removed duplicate rows using `drop_duplicates()`.

#### Outcome

* No duplicate records were existed
* Dataset consistency and accuracy were improved.

### 2.3 Correcting Data Types

Data types were verified and corrected to support efficient processing and calculations.

#### Procedures Performed

* Examined column data types using `info()`.
* Converted **Order Date** and **Ship Date** columns to datetime format.
* Verified numerical columns such as Sales, Quantity, Discount, and Profit.

#### Outcome

* Enabled date-based analysis and calculations.
* Improved overall data reliability.

### 2.4 Creating Derived Columns

To enhance analytical capabilities, three new columns were created from existing data.

#### Shipping Days

A new column called **Shipping Days** was created to calculate the delivery duration of each order.

**Formula:**

Shipping Days = Ship Date − Order Date

**Purpose:**

* Analyze shipping efficiency.
* Measure delivery performance across orders.

#### Order Year

A new column called **Order Year** was created by extracting the year from the Order Date column.

**Purpose:**

* Perform year-wise sales and profit analysis.
* Identify annual business trends and growth patterns.

#### Profit Margin

A new column called **Profit Margin** was created to evaluate profitability relative to sales.

**Formula:**

Profit Margin (%) = (Profit / Sales) × 100

**Purpose:**

* Measure profitability for each transaction.
* Identify highly profitable and low-profit orders.
* Support financial performance analysis.

#### Outcome

The newly created columns provided additional insights into business operations, shipping performance, annual trends, and profitability.

### 2.5 Data Filtering

Data filtering was performed to focus on specific business segments and categories.
* High profit orders
* furniture category orders
* orders with sales above 1000

#### Procedures Performed

* Filtered records based on profit,category and sales
* Extracted relevant subsets for detailed analysis.

#### Outcome

* Simplified data exploration.
* Enabled focused business analysis.


## Summary of Pre-processing Activities

| Activity                  | Purpose                           |
| ------------------------- | --------------------------------- |
| Missing Value Check       | Ensure data completeness          |
| Duplicate Removal         | Improve data quality              |
| Data Type Correction      | Enable accurate calculations      |
| Creation of Shipping Days | Analyze delivery performance      |
| Creation of Order Year    | Perform yearly trend analysis     |
| Creation of Profit Margin | Measure profitability             |
| Data Filtering            | Focus analysis on specific groups |
      
## Conclusion

Phase 2 successfully prepared the Superstore dataset for advanced analysis. Missing values and duplicate records were addressed, data types were corrected, and three new analytical features—Shipping Days, Order Year, and Profit Margin—were created. These preprocessing steps enhanced the dataset's quality and provided a strong foundation for Exploratory Data Analysis, visualization, and business insight generation in the subsequent phases of the project.

# Phase 3 Report: Exploratory Data Analysis (EDA)

## Introduction

The third phase of the Superstore Sales Analysis project focused on Exploratory Data Analysis (EDA). The objective of this phase was to examine the dataset, identify patterns and trends, and understand relationships among key business variables. Various analytical techniques such as univariate, bivariate, and multivariate analysis, along with groupby operations, correlation analysis, and statistical summaries, were used to generate meaningful business insights.

## 3. Exploratory Data Analysis (EDA)

EDA was conducted to uncover hidden patterns in sales and profit data and to support data-driven decision-making.

### 3.1 Univariate Analysis

Univariate analysis was performed to study individual variables independently.

#### Analyses Performed

##### Sales Distribution

* Analyzed the distribution of sales values across all transactions.
* Examined the variation and spread of sales data.

##### Profit Distribution

* Studied the distribution of profit values.
* Identified patterns in profitability across orders.

##### Category Frequency

* Calculated the frequency of each product category.
* Determined the most frequently occurring categories in the dataset.

#### Findings

* Sales values varied significantly across transactions.
* Profit values showed both positive and negative outcomes.
* Product categories were not evenly distributed, with some categories appearing more frequently than others.

### 3.2 Bivariate Analysis

Bivariate analysis was conducted to examine relationships between two variables.

#### Analyses Performed

##### Sales by Category

* Compared total sales across different product categories.

##### Profit by Region

* Evaluated profits generated in each region.
* Compared regional performance based on profitability.

##### Discount vs Profit

* Analyzed the relationship between discount and profit.
* Investigated the impact of discounts on business profitability.

#### Findings

* Product categories contributed differently to overall sales.
* Regional profit performance varied across the dataset.
* Higher discounts generally resulted in lower profits.

### 3.3 Multivariate Analysis

Multivariate analysis was performed to study interactions among multiple variables simultaneously.

#### Analyses Performed

##### Category and Region-wise Sales

* Examined sales performance across categories and regions.
* Compared category contributions within each region.

##### Category and Segment-wise Profit

* Analyzed profits generated by different customer segments within each category.
* Evaluated segment-level profitability patterns.

#### Findings

* Sales performance differed across category-region combinations.
* Customer segments contributed differently to category profitability.
* Certain category and segment combinations generated higher profits than others.

### 3.4 GroupBy Analysis

GroupBy operations were used to aggregate and summarize business metrics.

#### Analyses Performed

##### Sales by Region

* Calculated total sales generated in each region.

##### Profit by Sub-Category

* Computed total profit earned by each product sub-category.
* Identified high-performing and low-performing sub-categories.

#### Findings

* Sales varied considerably among regions.
* Some sub-categories generated significantly higher profits than others.

### 3.5 Correlation Analysis

Correlation analysis was conducted to identify relationships among numerical variables.

#### Variables Analyzed

* Sales
* Profit
* Quantity
* Discount

#### Findings

* Sales and Profit showed a positive relationship.
* Discount exhibited a negative relationship with Profit.
* Quantity had a moderate association with Sales.
* The correlation matrix provided a clear visualization of these relationships.

### 3.6 Statistical Summary

Descriptive statistics were generated to summarize the numerical variables in the dataset.

#### Measures Calculated

* Count
* Mean
* Standard Deviation (Std)
* Minimum Value (Min)
* 25th Percentile (25%)
* Median (50%)
* 75th Percentile (75%)
* Maximum Value (Max)

#### Purpose

* Understand the central tendency and spread of the data.
* Identify variability and distribution patterns.
* Support conclusions drawn from exploratory analysis.

## Key Insights

1. Sales and profit distributions revealed significant variation across transactions.
2. Category frequency analysis identified the most common product categories.
3. Sales performance differed considerably among categories.
4. Profitability varied across regions.
5. Discounts had a negative impact on profit in many transactions.
6. Sales patterns differed across category-region combinations.
7. Customer segments contributed differently to profitability within product categories.
8. Certain sub-categories generated substantially higher profits than others.
9. Correlation analysis highlighted important relationships among numerical variables.

## Conclusion

Phase 3 successfully explored the Superstore dataset through univariate, bivariate, and multivariate analysis. GroupBy operations, correlation analysis, and descriptive statistical summaries provided valuable insights into sales performance, profitability, regional trends, and customer segments. The findings obtained from this phase establish a strong foundation for data visualization, business recommendations, and strategic decision-making in the subsequent stages of the project.

# Phase 4 Report: Data Visualization

## Introduction

The fourth phase of the Superstore Sales Analysis project focused on data visualization. The objective was to present the results of the exploratory data analysis in a graphical format using visualization libraries such as Matplotlib and Seaborn. Visualizations were used to identify trends, patterns, distributions, and relationships within the dataset, making the findings easier to interpret and communicate.

## 4. Data Visualization

Various charts and plots were created to visualize sales performance, profitability, regional contributions, customer behavior, and relationships among variables. Appropriate titles, labels, legends, and color schemes were applied to ensure clarity and readability.

### 4.1 Bar Plot – Sales by Category

A bar plot was created to compare total sales across different product categories.

#### Purpose

* Compare category-wise sales performance.
* Identify the highest and lowest revenue-generating categories.

#### Findings

* Sales varied significantly among product categories.
* Some categories contributed substantially more revenue than others.

### 4.2 Line Chart – Sales Trend Over Time

A line chart was generated to analyze sales trends over time.

#### Purpose

* Examine changes in sales across different years.
* Identify growth patterns and fluctuations.

#### Findings

* Sales performance showed variations over time.
* Certain periods recorded higher sales compared to others.

### 4.3 Pie Chart – Sales Contribution by Region

A pie chart was used to visualize the percentage contribution of each region to total sales.

#### Purpose

* Understand regional contribution to overall business sales.
* Compare the share of each region.

#### Findings

* Regional contributions were unevenly distributed.
* Some regions accounted for a larger proportion of total sales.

### 4.4 Histogram – Distribution of Sales

A histogram was created to examine the distribution of sales values.

#### Purpose

* Analyze the frequency distribution of sales.
* Identify concentration and spread of sales transactions.

#### Findings

* Most sales transactions were concentrated within a specific range.
* A smaller number of transactions recorded very high sales values.

### 4.5 Box Plot – Profit by Category

A box plot was used to analyze profit distribution across product categories.

#### Purpose

* Compare profitability among categories.
* Detect outliers and variations in profit.

#### Findings

* Profitability differed among categories.
* Outliers indicated the presence of exceptionally high or low profit values.

### 4.6 Scatter Plot – Sales vs Profit

A scatter plot was generated to study the relationship between sales and profit.

#### Purpose

* Examine correlation between sales and profit.
* Identify trends and unusual observations.

#### Findings

* Sales and profit generally showed a positive relationship.
* Some transactions generated high sales but comparatively lower profits.

### 4.7 Heatmap – Correlation Analysis

A heatmap was created using the correlation matrix of numerical variables.

#### Variables Included

* Sales
* Profit
* Quantity
* Discount

#### Purpose

* Visualize relationships among numerical variables.
* Identify positive and negative correlations.

#### Findings

* Sales and Profit exhibited a positive correlation.
* Discount showed a negative relationship with Profit.

### 4.8 Count Plot – Orders by Ship Mode

A count plot was used to display the number of orders for each shipping mode.

#### Purpose

* Analyze the frequency of different shipping methods.
* Understand customer shipping preferences.

#### Findings

* Certain shipping modes were used more frequently than others.
* Order distribution varied across shipping methods.

### 4.9 Top 10 Sub-Categories by Sales

A bar chart was created to display the top 10 product sub-categories based on total sales.

#### Purpose

* Identify the best-performing sub-categories.
* Compare sales among leading product groups.

#### Findings

* A few sub-categories contributed a significant portion of overall sales.
* Sales performance varied considerably among the top-selling sub-categories.

### 4.10 Multiple Subplots

Multiple related visualizations were arranged using subplots for better comparison and presentation.

#### Purpose

* Display multiple charts in a single figure.
* Facilitate comparison between different business metrics.

#### Benefits

* Improved visual organization.
* Enhanced readability and analysis efficiency.

## Visualization Standards Followed

The following best practices were applied to all visualizations:

* Appropriate chart types selected based on the data.
* Clear and descriptive titles added.
* Axis labels provided for all plots.
* Legends included where applicable.
* Consistent color schemes used for readability.
* Subplots utilized for effective layout management.

## Conclusion

Phase 4 successfully transformed the analytical results into meaningful visual representations. Bar plots, line charts, pie charts, histograms, box plots, scatter plots, heatmaps, count plots, and subplot visualizations helped uncover important insights related to sales performance, profitability, regional contributions, shipping methods, and product categories. These visualizations enhanced understanding of the dataset and supported effective business decision-making.

### INSIGHTS AND REPORTS

Product-Level Insights A small number of sub-categories accounted for a large portion of sales. These products act as key revenue drivers for the business.
Business Impact: Prioritize inventory management and promotions for top-performing products.

Outlier Detection Box plots identified several extreme sales and profit values. These outliers may represent bulk purchases, premium products, or unusual transactions.
Business Impact: Investigate exceptional transactions to understand their business significance.

## RESULT

Higher sales generally contribute to higher profits. Increasing discounts tends to reduce profitability. Larger order quantities are associated with higher sales revenue.

Overall, the business can improve performance by:

Focusing on high-performing products and regions. Optimizing discount strategies to protect profit margins. Strengthening marketing efforts in underperforming regions. Leveraging seasonal sales patterns for better inventory planning. Conducting deeper analysis of loss-making transactions and product categories.

## RECOMMENDATIONS 

Build predictive models for sales forecasting. Perform customer segmentation using clustering techniques. Develop an interactive dashboard using Power BI or Tableau. Analyze customer lifetime value and retention trends. Investigate the root causes of negative-profit transactions.












  
