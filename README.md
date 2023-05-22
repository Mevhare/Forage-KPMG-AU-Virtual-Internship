# KPMG Australia Virtual Internship
![KPMG logo](https://github.com/Mevhare/KPMG-Virtual-Internship/blob/main/Images/KPMG_logo.jpg)

This project was carried out as a requirement of the KPMG Data Analytics Virtual Internship in collaboration with Forage. I would like to specially thank KPMG Australia for giving me this opportunity to learn and also showcase my data analytics skills. For more information on the internship click [here](https://www.theforage.com/virtual-internships/theme/m7W4GMqeT3bh9Nb2c/KPMG-Data-Analytics-Virtual-Internship)

# Introduction
<img src= "https://github.com/Mevhare/KPMG-Virtual-Internship/blob/main/Images/Sprocket_logo.png" width="600" height="300">
Sprocket Central Pty Ltd , a medium size bikes & cycling accessories organisation, has approached Tony Smith (Partner) in KPMG’s Lighthouse & Innovation Team. Sprocket Central Pty Ltd  is keen to learn more about KPMG’s expertise in its Analytics, Information & Modelling team. 
Sprocket Central Pty Ltd needs help with its customer and transactions data. The organisation has a large dataset relating to its customers, but their team is unsure how to effectively analyse it to help optimise its marketing strategy. 


# Task 1 : Data Quality Accessment
Draft an email to the client identifying the data quality issues and strategies to mitigate these issues.
The client provided KPMG with 4 datasets:
- New Customer List
- Customer Demographic 
- Customer Addresses
- Transactions data in the past 3 months

Dataset link: [Sprocket Customer Data](https://github.com/Mevhare/KPMG-Virtual-Internship/blob/main/Data/KPMG_Sprocket_raw_data.xlsx)

Report Link: [Data Quality Accessment Email](https://github.com/Mevhare/KPMG-Virtual-Internship/blob/main/Solution/Task%201/Mevhare_Afe_Report_E-mail.pdf)


# Task 2 : Data Insights
Sprocket marketing team is looking to boost business by analysing their existing customer dataset to determine customer trends and behaviour. 

Using the existing 3 datasets (Customer demographic, customer address and transactions) as a labelled dataset, please recommend which of these 1000 new customers should be targeted to drive the most value for the organisation. 

In building this recommendation, we need to start with a PowerPoint presentation which outlines the approach which we will be taking. The client has agreed on a 3 week scope with the following 3 phases as follows - Data Exploration; Model Development and Interpretation.

## Data Cleaning and Transformation:

#### Customer Demographic
- Corrected inconsistency in gender column to ensure it only contains 3 enteries; Male, Female and U.
- Calculated age column from the DOB column.
- Filtered out ages greater than 91.
- Filtered out blanks in job title column.
- Deleted default column.
- Filtered out deceased customers.

#### Customer Address
- Corrected inconsistency in state column to ensure it only contains 3 enteries; VIC, NSW and QLD.

#### Transactions
- Filtered out blanks in online order column.
- Filterd out cancelled orders in order status column.
- Filtered out blank brands.
- Corrected product first sold format to date.
- Calculated profit column by subtracting standard cost from the list price.

#### New Customers
- Filtered out blank records in the DOB column.
- Filtered out blank records job title column.

### Merging Tables
After cleaning the data, The Customer Demographic table and Customer Address table was merged with the Transaction table using inner join in Power Query to get the "All Data" table. All data table contains 16,940 records compared to the original 20,000 records in the Transaction table.

## Customer Segmentation
Customer segmentation allows businesses to group customers into distinct segments based on their shared characteristics, behaviors, and preferences. By identifying these segments, Sprocket can gain valuable insights into its customer base, enabling targeted marketing campaigns, personalized offerings, and improved customer experiences.

In this context, we will employ the K-means clustering algorithm using RFM (Recency,Frequency and Monetary) features to segment Sprocket's customers based on their purchasing patterns, preferences, and interactions with the company. By utilizing this data-driven approach, Sprocket can develop more effective marketing strategies, enhance customer satisfaction, and drive business growth.

Using Pivot tables in Excel, a new sheet was created for RFM values for each customer in our data
![RFM_image](https://github.com/Mevhare/KPMG-Virtual-Internship/blob/main/Solution/Task%202/Images/RFM_table_excel.png)

Using Python, each customer was assigned to 4 groups;

|Cluster|Label|Description|
|:----|:----|:----|
|0|Need Attention|These customers have the second-poorest recency score (84.9), indicating that their last purchase was long ago. They also have a relatively low purchase frequency score (4.0) and relatively low monetary value (2013.1). They are considered low-spenders with a low number of orders.|
|1|Champion |These customers have the best recency score (9.3), indicating recent purchases. They also have a high purchase frequency score (6.5) and a high monetary value (3658.5). They are frequent buyers who spend a significant amount on your products.|
|2|Lost|These customers have the poorest scores across all three metrics (recency, frequency, and monetary value). They are characterized by poor recency (131.7), low frequency (2.2), and low monetary value (591.4). They represent customers who were once active but have become disengaged.|
|3|Loyal |These customers have a moderate recency score (62.8) but a high frequency (7.1) and high monetary value (4245.9). They are often spending good money on your products and are responsive to promotions.|

If you are interested in the full analysis, click [here.](https://github.com/Mevhare/KPMG-Virtual-Internship/blob/main/Solution/Task%202/Sprocket_Customer_Segmentation_KMeans.ipynb)

## Presentation
A powerpoint report was made on Data Exploration; Model Development and Interpretation. 
![PowerPoint](https://github.com/Mevhare/KPMG-Virtual-Internship/blob/main/Solution/Task%202/Images/Powerpoint.png)

Here is the link to the [Power Point Presentation.](https://github.com/Mevhare/KPMG-Virtual-Internship/blob/main/Solution/Task%202/Sprocket_Presenation.pptx)


# Task 3
 
