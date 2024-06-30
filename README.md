# Recency Frequency and Monetary Analysis using SQL and Tableau

## Access to the project

Dashboard created for this project can be found here: [RFM analysis Tableau Dasboard](https://public.tableau.com/app/profile/pat.dan/viz/RFMDashboard_2_0/Dashboard1?publish=yes)

SQL code for this project is uploaded here [RFM SQL Code](https://github.com/PatrycjaDanilczuk/RFM-and-Segmentation-using-SQL-and-Tableau/blob/main/RFM_SQL%20code_pdanil)

## Project description
Prepare RFM (Recency, Frequency, Monetary) analysis and customer segmentation based on the “rfm” data table hosted in BigQuery project. 

Customer segmentation is the process of dividing customers into groups based on common characteristics so companies can market to each group effectively and appropriately. 
Segmentation allows marketers to better tailor their marketing efforts to various audience subsets. Those efforts can relate to both communications and product development. 
Specifically, segmentation helps a company:

- Create and communicate targeted marketing messages that will resonate with specific groups of customers, but not with others (who will receive messages tailored to their needs and interests, instead)

- Select the best communication channel for the segment, which might be email, social media posts, radio advertising, or another approach, depending on the segment
  
- Identify ways to improve products or new product or service opportunities

- Establish better customer relationships
  
- Test pricing options
  
- Focus on the most profitable customers
  
- Improve customer service
  
- Upsell and cross-sell other products and services

## About the dataset

The rfm dataset is hosted in BigQuery. The table contains information on customer transactions, including their ID, purchase dates, quantity, and monetary value. Segment customers on RFM scores and provide insights for the marketing department.

The rfm dataset contains 541.909 rows and 8 columns.

**rfm schema**

| Field name | Type | Mode |
|---------------|-----------|-----------|
| InvoiceNo | STRING | NULLABLE |
| StockCode | STRING | NULLABLE |
| Description | STRING | NULLABLE |
| Quantity | INTEGER | NULLABLE |
| InvoiceDate | TIMESTAMP | NULLABLE |	
| UnitPrice | FLOAT | NULLABLE |
| CustomerID | INTEGER | NULLABLE |
| Country | STRING | NULLABLE	|


## SQL code

Transformed rfm data (451.909 transactions) into table of distinct customers (4.300 rows) with applied RFM score and Segment name. Retrieved additional tables with Country and Products for more in-depth analysis.

### Step 1: Data Preparation
Identifying necessary columns for RFM Analysis.
Filtering transactions for the time span from 2010-12-01 to 2011-12-01.
Excluding transactions with null CustomerID, likely indicating purchases made without creating an account.
Calculating RFM measures: Frequency, Monetary, and Recency.
Validating the number of distinct customers.
### Step 2: Assigning RFM scores
Applying quartiles and assigning scores from 1 to 4 for Recency, Frequency, and Monetary
Assigning RFM score
### Step 3: Segmenting Customers
Creating customer segments: Best Customers, Loyal Customers, Potential Loyalists, Recent Customers, Big Spenders, About to Sleep, Can’t Loose Them, Lost Customers
### Step 4: Final Data Selection
Selecting all relevant columns for the final analysis table.
### Step 5: Getting additional data
Creating additional tables with Country and Products for more in-depth analysis.

## Visualization and Insights
Creating Tableau Dashboard for analysis.
Providing insights for customer engagement and retention strategies based on RFM segments.
