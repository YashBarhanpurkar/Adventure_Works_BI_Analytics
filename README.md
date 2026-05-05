# AdventureWorks Business Intelligence Solution

## Project Overview
This repository contains a comprehensive Power BI business intelligence dashboard for AdventureWorks, a fictional global manufacturing company. The project transforms raw data into actionable insights covering sales, revenue, profit, and returns across six countries (Australia, Canada, France, Germany, UK, and USA).

**Data Source:** Provided via Maven Analytics, derived from original Microsoft AdventureWorks sample databases.

**Timeline:** January 1, 2020 – June 30, 2022.

## Key Features & Views
*   **Executive Summary:** High-level KPIs for revenue, profit, orders, and return rates with drill-through capabilities.

*   **Map View:** Geospatial analysis of total orders per country to identify regional market share.

*   **Product Detail View:** Performance tracking against targets with "What-If" analysis for price adjustments.

*   **Customer Detail View:** Analysis of high-value customers and per-customer revenue trends.

*   **Custom UI:** Sleek navigation using a hidden filter pane and custom tooltips for category metrics.

## Technical Challenges & Solutions
This project involved significant "under-the-hood" engineering to ensure the report was robust and portable:

*   **Dynamic Data Pipelines:** Implemented a Folder Path Parameter in Power Query. This allows the entire report to be reconnected to local data sources on any machine with a single path update, rather than re-pointing every individual table.

*   **Recursive Dependency Resolution:** Diagnosed and resolved Cyclic Reference errors within the data model (specifically the Territory Lookup), ensuring a clean star-schema architecture.

*   **ETL Optimization:** Fixed "Table to Binary" conversion errors during the file combination process to successfully append multiple years of sales CSVs.

*   **Advanced DAX & M:** Created a rolling calendar using Power Query M-code and built complex DAX measures for YTD totals, rolling averages, and adjusted profit.

## Key Insights
*   **Financials:** Generated $24.9M in revenue and $10.5M in profit.

*   **Seasonal Trends:** Identified an exceptional revenue peak in December 2021 ($1.64M), suggesting highly effective seasonal promotions.

*   **Product Performance:** Tires and Tubes are the highest volume sellers, while Clothing and Accessories remain the most profitable categories.

*   **Market Analysis:** While the USA is the largest market by volume ($7.94M), Australia leads in efficiency with the highest revenue per customer ($2,131).

## Project Structure
*   **Report/:** Contains the .pbix Power BI file.

*   **AdventureWorks Raw Data/:** Raw CSV data files used for the analysis.

*   **Images/:** Screenshots of the dashboard views.

*   **Documentation/:** PDF export of the report and technical notes.
