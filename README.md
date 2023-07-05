# S&P Top 500 Companies, Financial Analysis
Project

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
