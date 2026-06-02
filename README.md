# customer-shopping-behavior-analysis
An end-to-end data analytics project analyzing customer shopping behavior across 3,900 transactions. Features data cleaning/engineering in Python, structured business querying in PostgreSQL, and an interactive Executive Dashboard in Power BI to drive strategic decisions.

Dataset Summary
Scale: 3,900 transactional records across 18 unique features.
Key Demographics: Customer Age, Gender, Location, and Subscription Status.
Transactional Attributes: Items purchased, Product Category, Purchase Amount ($), Season, Size, and Color. 
Behavioral Attributes: Discount/Promo usage, Purchase Frequency, Review Ratings, and Shipping Type.  

Tools & Tech Stack
Data Cleaning & EDA: Python (Pandas, NumPy, Jupyter Notebook)
Database Management: SQL (PostgreSQL / MySQL / SQL Server) 
Business Intelligence: Power BI Desktop 
Presentation & Reporting: Gamma App (AI-assisted presentation design) & Markdown

 Analytical Steps & Workflow
 1.Exploratory Data Analysis & Cleaning (Python)
 -Initial Assessment: Audited data structures using df.info() and evaluated summary statistics via df.describe(). 
 -Data Quality Handling: Identified and resolved 37 missing values in the Review Rating column by imputing category-specific medians. 
 -Feature Engineering: * Segmented customer ages into custom age_group brackets. 
     -Standardized column naming conventions to clean snake_case format.
     -Eliminated data redundancies by dropping promo_code_used in favor of discount_applied. 
 -ETL Pipeline: Established a local connection to the SQL database and exported the cleaned DataFrame into data tables.  

 2. Deep-Dive Database Querying (SQL)
 -Wrote optimized relational queries to answer critical business objectives:
 -Revenue Contributions: Broke down total gross revenue across demographics (e.g., Male vs. Female expenditure).
 -Behavioral Segments: Isolated high-spending customers who frequently use discount codes to monitor profit margins.
 -Performance Tracking: Evaluated top-rated products by category and calculated subscriber vs. non-subscriber value metrics.
 -Customer Retention: Categorized users into New, Returning, and Loyal cohorts using conditional logic based on purchase histories.

3. Reporting & Presentation
-Executive Summary: Synthesized technical findings into a business-facing strategic report.
-PPT Presentation (via Gamma): Created an AI-powered, high-impact slide deck tailored for stakeholders, highlighting key operational takeaways and ROI opportunities.

 Dashboard Architecture (Power BI)
 The interactive Power BI dashboard provides a centralized interface tracking high-level Key Performance Indicators (KPIs) and visual breakdown patterns: 
 -Core KPI Cards: Tracks total customer counts (3.9K), Average Purchase Amount ($59.76), and Average Review Rating (3.75). 
 -Demographic Filters: Sliceable visualizations across Gender, Subscription Status, and Product Categories. 
 -Revenue & Sales Charts: Displays categorical performance (with Clothing and Accessories leading) alongside demographic trends like revenue contribution by age     group. 

Key Results & Business Recommendations
-Optimize Subscription Funnels: While subscribers represent 27% of the customer base, their average ticket size is slightly lower than non-subscribers. 
-Recommendation: Introduce exclusive product drops to incentivize larger subscriber cart values. 
-Targeted Marketing Allocations: "Young Adults" represent the highest-revenue age group segment ($62,143 total revenue). Marketing spend should prioritize digital channels heavily indexed by this cohort. 
-Discount Policy Auditing: Certain items, such as Hats (50.00% discount rate) and Sneakers (49.66%), show extremely high discount dependencies. Recommendation: 
 Adjust baseline pricing or introduce tiered spending requirements to safeguard margins.  

 How to Run the Project
Prerequisites
Ensure you have the following installed on your system:

Python 3.8+ (with Jupyter Notebook)

SQL Database Instance (PostgreSQL)

Power BI Desktop

--Execution Setup--
1--Clone the Repository:

Bash
git clone https://github.com/yourusername/your-repository-name.git
cd your-repository-name

2--Process the Data (Python):--

Open notebooks/data_cleaning.ipynb in Jupyter Notebook.

Update your database credentials in the SQL connection cell.

Run all cells to clean the raw file and load it directly into your database engine.

3--Run Business Queries (SQL):--

Connect to your database client.

Open and execute the scripts found inside sql/business_queries.sql to verify data metrics.

4--View the Dashboard (Power BI):--

Double-click dashboard/shopping_behavior_dashboard.pbix to launch the interactive dashboard in Power BI Desktop.

