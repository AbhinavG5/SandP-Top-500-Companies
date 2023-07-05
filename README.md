# Financial Analysis of S&P Top 500 Companies

This project aims to provide insights into the financial performance and trends of the companies listed in the S&P 500 index. The analysis involves data cleansing and processing using SQL and Excel, followed by visualization and reporting using Power BI.

Project Overview
The objective of this project is to analyze the financial data of the S&P 500 companies to identify key trends, patterns, and performance indicators. By leveraging SQL, Excel, and Power BI, we can perform comprehensive financial analysis and present the findings in an interactive and visually appealing manner.

Tools Used
SQL: Structured Query Language (SQL) is used for data extraction, transformation, and loading (ETL) processes. It enables us to retrieve relevant financial data from databases efficiently.

Excel: Excel is utilized for data cleansing, processing, and calculations. It offers a wide range of functionalities such as formulas, sorting, filtering, and pivot tables, which are essential for preparing the data for analysis.

Power BI: Power BI enables to create visually compelling reports and dashboards. It allows to visualize and explore the financial data, generate interactive visualizations, and share insights with stakeholders.

Project Steps
Data Acquisition: Gather financial data for the S&P 500 companies from reliable sources such as financial databases or APIs.

Data Cleansing: Use Excel to clean the raw data, remove duplicates, handle missing values, and ensure consistency and accuracy.

Data Storage: Store the processed data in a suitable database system using SQL. This facilitates efficient data retrieval for analysis.

Analysis and Visualization: Import the processed data into Power BI and create interactive visualizations, charts, and reports. Identify key performance indicators, trends, and insights regarding the financial performance of S&P 500 companies.

### Power BI Dashboard
![(T-500 Companies Power BI Dashboard.png)](https://github.com/AbhinavG5/SandP-Top-500-Companies/blob/main/T-500%20Companies%20Power%20BI%20Dashboard.png)

## SQL Queries in Text with Output
Q1. Query to find companies with a market capitalization abouve $1 billion and a price-to-book ratio less than 1

Query: 
SELECT Symbol, Name, Market_Cap, Price_or_Book
FROM top_500_sp_companies
WHERE Market_Cap > 100000000 AND Price_or_Book < 1;

![(S&P 500 Companies - Q1.png)](https://github.com/AbhinavG5/SandP-Top-500-Companies/blob/main/S%26P%20500%20Companies%20-%20Q1.png)

Q2. Calculate the total earning per share (EPS) for each sector

Query:
SELECT Sector, SUM (Earnings_or_Share) AS Total_Earnings_Per_Share
FROM top_500_sp_companies
GROUP BY Sector;

![(S&P 500 Companies - Q2.png)](https://github.com/AbhinavG5/SandP-Top-500-Companies/blob/main/S%26P%20500%20Companies%20-%20Q2.png)

Q3. Calculate the market capitalization to EBITDA ratio for each company

Query:
SELECT Symbol, Name, Market_Cap / EBITDA AS Market_Cap_to_EBITDA_Ratio
FROM top_500_sp_companies

![(S&P 500 Companies - Q3.png)](https://github.com/AbhinavG5/SandP-Top-500-Companies/blob/main/S%26P%20500%20Companies%20-%20Q3.png)

Q4. Find the top 5 companies with the lowest dividend yield

SELECT Symbol, Name, Dividend_Yield
FROM top_500_sp_comapnies
ORDER BY Dividend_Yield ASC
LIMIT 5;

![(S&P 500 Companies - Q4.png)](https://github.com/AbhinavG5/SandP-Top-500-Companies/blob/main/S%26P%20500%20Companies%20-%20Q4.png)

Q5. Find companies with a price-to-earnings ratio greater than 20 and a price-to-sales ratio less than 1

Query:
SELECT Symbol, Name, Price_or_Earnings, Price_or_Sales
FROM top_500_sp_companies
WHERE Price_or_Earnings > 20 AND Price_or_Sales < 1;

![(S&P 500 Companies - Q5.png)](https://github.com/AbhinavG5/SandP-Top-500-Companies/blob/main/S%26P%20500%20Companies%20-%20Q5.png)
