# Recency Frequency and Monetary Analysis using SQL and Tableau
Dashboard created for this analysis can be found [here](https://public.tableau.com/app/profile/pat.dan/viz/RFMDashboard_2_0/Dashboard1?publish=yes)

SQL code for this project is uploaded [here](https://github.com/PatrycjaDanilczuk/RFM-and-Segmentation-using-SQL-and-Tableau/blob/main/RFM_SQL%20code_pdanil)

## Project description
Prepare RFM (Recency, Frequency, Monetary) analysis and customer segmentation based on the “rfm” data table hosted in BigQuery project. The dataset contains information on customer transactions, including their ID, purchase dates, quantity, and monetary value. Segment customers on RFM scores and provide insights for the marketing department.

## Steps applied
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
### Step 6: Visualization and Insights
Creating Tableau Dashboard for analysis.
Providing insights for customer engagement and retention strategies based on RFM segments.
