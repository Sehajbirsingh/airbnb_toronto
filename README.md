# Airbnb Data Analysis and Big Data Pipeline

## Overview
This project focuses on the analysis of a large dataset from Airbnb. The dataset includes key information about Airbnb listings in Toronto, such as details on properties, reviews, pricing, hosts, and availability. The main objective is to build a comprehensive big data pipeline to process, store, and analyze this data using various tools and technologies like MongoDB, SQL Server, SSMS, Power BI, and SSIS. The project’s goal is to perform Data Extraction, Transformation, and Loading (ETL) processes and generate visual insights that aid decision-making for Airbnb hosts and businesses.

## Dataset
The project uses the Airbnb dataset sourced from InsideAirbnb. The dataset contains the following key components:
- **Listings Data**: Details about properties listed on Airbnb, including location, price, room types, and amenities.
- **Reviews Data**: User comments and ratings for each listing.
- **Calendar Data**: Availability and pricing of listings over time, including minimum stay requirements.
- **Host Data**: Information on Airbnb hosts such as name, response rate, and host location.

## Project Workflow

### 1. **Data Import and Storage in MongoDB**
The first step involves loading raw Airbnb data into MongoDB, a NoSQL database, which allows for flexible schema-less storage. The collections used are:
- **listings**
- **reviews**
- **calendar**
- **hosts**

### 2. **Data Transformation and Cleaning**
- **Sentiment Analysis**: The `reviews` data undergoes sentiment analysis using the TextBlob library, categorizing each review as positive, negative, or neutral.
- **Handling Missing Values**: For columns like `license` and `has_availability`, missing values are replaced with appropriate defaults (e.g., 'unlicensed' for `license`).
- **Data Aggregation**: The `calendar` data is aggregated to calculate the total nights booked and average price per listing.

### 3. **Data Upload to SQL Server**
Once the data is cleaned and transformed, it's uploaded into an SQL Server database schema (`AirbnbDB`) using automated processes in Python. The cleaned data is saved in CSV format and loaded into the database for further analysis.

### 4. **Data Analysis in SQL Server**
Using SSMS (SQL Server Management Studio), the data is further analyzed by combining multiple tables, running queries to extract insights, and preparing the data for visualization.

### 5. **Data Visualization with Power BI**
The project uses Microsoft Power BI to create interactive visualizations, such as:
- **Price Distribution**: A histogram showing the distribution of Airbnb listing prices across neighborhoods.
- **Sentiment Distribution**: A pie chart showing the proportion of positive, negative, and neutral sentiments.
- **Seasonal Availability Trends**: A line chart displaying the number of available listing days across different months in 2023.

### 6. **Final Deliverables**
The deliverables include:
- **ETL Pipeline**: A fully functional ETL pipeline built using SSIS that processes and loads data.
- **SQL Server Database**: A structured database with cleaned and transformed data.
- **Data Visualizations**: Interactive dashboards presenting the insights gained from the data.
- **Reports**: A detailed report summarizing the methodology, findings, and insights.
- **Video Demonstration**: A video showing the execution and functionality of the ETL pipeline and visualizations.

## Conclusion
This project successfully demonstrates the ability to process and analyze large datasets using big data tools and ETL pipelines. By leveraging MongoDB, SQL Server, Power BI, and SSIS, the pipeline transforms raw data into valuable insights that can support decision-making related to pricing, customer sentiment, and listing availability. These insights will help Airbnb hosts and businesses optimize strategies for better performance and customer satisfaction.
