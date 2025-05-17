# Global Electronics Retailer

## The Situation
You've just been hired as a Data Analyst for Maven Electronics, a global retailer that sells computers, cell phones, TVs, cameras, appliances and more, both online and in-store.

## The Assignment
Revenue has been on a downward trend since 2020, and management needs your help consolidating the data to conduct an exploratory analysis.
Your goal is to use the CSV files provided to build a data model and interactive report that the management team can use to explore performance.

## The Objectives
1. Profile and prepare the data
2. Build a relational data model
3. Enrich and explore the data
4. Build an interactive report

## The Data Set

#### Global Electronics Retailer
Sales data for a fictitious global electronics retailer, including tables containing information about transactions, products, customers, stores and currency exchange rates.


#### Recommended Analysis
1. What types of products does the company sell, and where are customers located?
2. Are there any seasonal patterns or trends for order volume or revenue?
3. How long is the average delivery time in days? Has that changed over time?
4. Is there a difference in average order value (AOV) for online vs. in-store sales?

#### Objective 1: Profile & prepare the data
Your first objective is to ingest the data from raw CSV files, conduct some data profiling, feature engineering and QA, and build a custom calendar to track performance by day, week, month, quarter and year.

* Connect to the Sales CSV file and profile the data. How many orders were recorded? Over what time period? Do you notice anything interesting about delivery dates? Add a TransactionKey field to uniquely identify each row.
* Connect to the Products CSV file and profile the data. What does the company sell? How many distinct categories and subcategories do you see?
* Connect to the Stores CSV file and profile the data. How many stores does Maven Electronics operate? Do you notice any that aren’t like the others?
* Connect to the Exchange_Rates CSV file and profile the data. What information does this table contain, and how could it be used?
* Connect to the Customers CSV file and profile the data. How many customers has the company served? Where are customers primarily located?
* Remove the Zip Code column, and transform the City field to capitalize the first letter of each word.
* Add a new column to calculate Customer Age in years, then add a conditional column to calculate Age Range, where >60 = "Senior", >30 = "Adult" and >18 = "Young Adult".
* Create a Calendar table that contains a list of contiguous dates (no gaps) and reflects the same date range as the Sales table, then add new columns for Day Name, Start of Week/Month/Quarter, and Year.

#### Objective 2: Build a relational model
Your second objective is to build a data model by connecting the foreign keys in the Sales table to the primary keys in each dimension table via 1:many relationships.

* Create relationships from the Sales table to Customers, Stores, Products and Calendar.
* What happens when you try to connect Sales to Exchange Rates? Add a new column to both tables named ExchangeKey and use that field to relate them via a 1:many relationship.
* Hide all foreign keys from the Sales table.
* BONUS: Split the Products table into category and subcategory-level dimension tables, and update the data model to relate these new tables.

#### Objective 3: Enrich & explore the data
Your third objective is to enrich the data model by adding calculated measures to track key business metrics, including total orders, revenue, average order value and delivery time.

* Add a blank, dedicated measures table.
* Create a new measure to calculate Total Orders, based on Order Number. How has order volume trended over time? Do all product categories show a similar trend?
* Calculate Total Revenue (USD), based on Quantity and Unit Price (USD). Which stores generate the most revenue? Which individual products? (BONUS: Create another version to calculate revenue in local currency).
* Calculate Average Order Value (AOV), based on Total Revenue (USD) and Total Orders. How does AOV compare across product categories? Are there differences based on customer age?
* Calculate Average Delivery Time, in days. Which types of products tend to be delivered fastest or slowest? Have delivery times improved or gotten worse?

#### Objective 4: Build an interactive report
Your fourth and final objective is to design an interactive report that the Maven Electronics leadership team can use to explore performance by store and over time.

* Show orders, revenue, AOV and average delivery time as KPI cards (or similar).
* Show revenue by month as a line chart, and by Product Category as a bar chart.
* Add slicers for StoreKey and Year, connected to all cards and visuals.
* Adjust formatting and polish for clarity and readability (consistent colors/themes, proper number formats, minimal clutter, etc.)
* What trends and patterns do you see? Where would you suggest digging deeper?

#### [Project Link]()