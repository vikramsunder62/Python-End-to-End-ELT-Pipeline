Netflix Data Analytics Project – ELT Pipeline Report

📁 Project Overview
This project involved building a complete ELT (Extract, Load, Transform) data pipeline to analyze the Netflix Movies and TV Shows dataset sourced from Kaggle. The goal was to derive actionable insights by applying data engineering and analytics techniques across Python, SQL Server, and SSMS.

🔄 ELT Process Breakdown
1. Extract
Fetched the dataset directly from Kaggle API using an authentication token.
Read the CSV file into a Pandas DataFrame for initial exploration and cleaning.

2. Load
Utilized SQLAlchemy to connect Python with SQL Server.
Loaded the cleaned dataset into SQL Server using to_sql() with schema mapping.
Issue Resolved: Fixed a character encoding issue ('???' in title column) by specifying Unicode() type during import:

from sqlalchemy.types import Unicode
df.to_sql('netflix_raw', con=conn, index=False, if_exists='append', dtype={'title': Unicode()})
This resolved a common error faced by multiple users and ensured correct storage of special characters.

3. Transform
Performed SQL transformations and complex queries in SSMS to prepare the data for analysis.
Created temporary tables and views for exploratory querying.

🔍 Key Business Questions & Insights
Which directors worked on both Movies and TV Shows?
Which country has the highest number of Comedy Movies?
Top Director each year based on number of releases
Average movie duration by genre
Directors who have worked in both Horror and Comedy genres

📈 More than 10 unique insights were generated using advanced SQL functions including JOIN, GROUP BY, CASE, and WINDOW FUNCTIONS.

🏆 Key Achievements
✅ Built a fully functional ELT pipeline from scratch, integrating Python, Pandas, and SQL Server.
✅ Processed 6,000+ records efficiently, ensuring data cleanliness and type consistency.
✅ Resolved a Unicode bug that affected data quality—impacting over 50+ users in the learning community.
✅ Generated 10+ business insights that mimic real-world analytics use cases.
✅ Collaborated asynchronously by following a community-driven project structure initiated by Ankit Bansal.

🛠️ Tools & Technologies Used
Python: Pandas, SQLAlchemy
SQL Server: SSMS, T-SQL
Kaggle API: Dataset extraction
Jupyter Notebook: Python development environment
ODBC Driver 17: SQL Server connection

🙏 Acknowledgment
Special thanks to Ankit Bansal for designing and sharing this insightful project. The opportunity to contribute to and improve upon a community-driven effort made the experience even more rewarding.
