📊 Market Analytics Dashboard
This project is a data-driven market analytics dashboard that provides insights into customer behavior, product performance, and review sentiment. It combines SQL for data extraction, Python for data enrichment, and Power BI for visual storytelling.

🚀 Project Overview
Objective:
To create an end-to-end analytics solution that helps marketing teams identify product trends, customer satisfaction levels, and sales insights using advanced sentiment analysis and business KPIs.

Key Features:

Customer sentiment analysis using natural language processing (NLP)
Visual performance metrics for products, customers, and regions
Power BI dashboard with interactive visualizations

🧰 Tech Stack
Python: Data cleaning, sentiment analysis with NLTK
SQL Server: Backend database with structured marketing data
Power BI: Dashboard creation and KPI visualization

🗃️ Dataset
Database: PortfolioProject_MarketingAnalytics

Main Table: fact_customer_reviews
Fields used:

ReviewID, CustomerID, ProductID
ReviewDate, Rating, ReviewText

🧠 Sentiment Analysis
Python Script: customer_reviews_enrich.py
Used VADER SentimentIntensityAnalyzer (from NLTK)
Calculated sentiment scores for each review
Combined score with review ratings to classify:
Positive, Negative, Mixed Positive, Mixed Negative, Neutral
Bucketed scores for visualization:
-1.0 to -0.5,
-0.49 to 0.0, 
0.0 to 0.49,
0.5 to 1.0
Output saved as: customer_reviews_enrich.csv

📈 Power BI Dashboard
File: Dashboard.pbix

Pages & Visuals:
Overview: KPIs for Total Sales, Total Reviews, and Average Ratings
Sentiment Analysis: Bar charts by sentiment category & bucket
Customer Insights: Region-wise and product-wise customer engagement
Review Trends: Monthly review trends and sentiment changes
Data Source: Connected to enriched data via SQL Server and CSV output.

⚙️ Setup Instructions
Install dependencies:

pip install pandas nltk pyodbc sqlalchemy
Configure your SQL Server instance in the script:

"Server=SATYAM\\SQLEXPRESS;"  
Run the Python script:

python customer_reviews_enrich.py
Open Dashboard.pbix in Power BI and refresh data sources.

💡 Note: If you're unable to install SQL Server, you can still review the Power BI dashboard and enriched CSV data for reference.

📌 Future Enhancements
Add demographic segmentation
Implement keyword extraction from reviews
Enable drill-throughs for advanced dashboard filtering
