# CUSTOMER-SEGMENTATION-BEHAVIORAL-ANALYSIS-USING-POWER-BI

## PROJECT OVERVIEW
This project focuses on analysing a sales dataset to help understand the customer base of the business better. The analysis aims to identify patterns in customer growth, demographics, tenure, income, and professional profiles to make data-driven marketing and retention decisions. The analysis was done using Microsoft power BI for data cleaning and visualizations.



## DATASET DESCRIPTION
The dataset comprises customer segmentation dataset containing nine (9) columns and 500 rows with information on Customer ID, Name, Gender, Age, Region, Occupation, Income, Customer Segment and Join Date. The dataset was initially reviewed to understand its structure, variables, and overall quality before proceeding with the analysis.


## OBJECTIVES
The aim of the project is to analyse the dataset to understand customer growth, demographics, tenure, income, and professional profiles to make data-driven marketing and retention decisions. And to be able to do that, the analysis seeks to answer the following business questions:
•	Customer Growth Timeline
•	Region with the Highest Customers
•	Age Group with the Highest Average Age
•	Professional Profile of Customers
•	Customer Distribution Across Gender
•	Customer Segment Distribution


## TOOLS
•	Microsoft Power BI
•	Power Query
•	DAX


## METHODOLOGY
The dataset was cleaned and analysed using power query in using Microsoft Power BI.

Key steps included:

•	Duplicate records were identified and removed to ensure data integrity and prevent bias in the analysis.

•	All columns were reviewed to detect inconsistencies in spelling, formatting, and data types.

•	New columns were created using power query to aid in the analysis, which include;

    Year: Extracted from the customer Join_date to enable trend analysis over time.
      Date.Year([Join_Date])
	  
    Tenure: Calculated to measure customer loyalty and duration of engagement with the business.
      Date.Year(Date.From(DateTime.LocalNow())) - Date.Year([Join_Date])
    
	Age Group: Customers were segmented into meaningful demographic categories to support targeted insights and reporting
                        if [Age] < 25 then "Youth" 
                        else if [Age] <= 40 then "Young Adult" 
                        else if [Age] <= 60 then "Adult" 
                        else "Senior"
						
•	To support KPI tracking and summary insights, the following measures were also created;
	
	Total Customers: Provides the overall customer count in the dataset.
      COUNT(customers[Name])
	
	Average Age: Helps understand the general age distribution of customers.
      AVERAGE(customers[Age])   
	
	Average Tenure: Indicates the typical length of customer relationships, useful for retention analysis.
      AVERAGE(customers[Tenure])    
	   
	Average Income: Provides insight into the economic profile of the customer base.
      AVERAGE(customers[Income])
	  
•	Exploratory Data Analysis was conducted to understand the distribution, relationships, and patterns within the dataset. Summary statistics were used to identify trends and key metrics.

•	Visualizations such as bar charts and line chart, column chart and donut chart were also used to better interpret the data.


## KEY INSIGHTS
The analysis of the dataset revealed several important patterns related to product performance, regional sales distribution, and overall revenue generation.

# Customer Growth Timeline

The Total Customers by Year analysis reveals a generally positive growth trend over time, with a significant increase observed between 2015 and 2017, indicating a strong customer acquisition phase. Following this peak, there is a slight decline in 2018, after which customer numbers stabilize and fluctuate within a narrow range from 2019 to 2024, suggesting a period of maturity and consistent retention. However, a noticeable drop in the most recent year highlights a potential decline in customer acquisition or an increase in churn, signalling the need for further investigation into underlying factors affecting customer growth.

# Region with the Highest Customers
The customer distribution analysis shows that the South region leads with the highest number of customers. It is followed by the Eastern region with 133 customers and the Northern region with 120 customers, while the Western region has the lowest customer count at 110.

# Age Group with the Highest Average Age
The chart indicates a clear decline in average age across the defined groups, with Seniors having the highest average age, followed by Adults, Young Adults, and Youth with the lowest. This pattern reflects a consistent age gradient aligned with the categorization, confirming that the grouping accurately segments progressively younger populations.

# Professional Profile of Customers
The distribution shows that Engineers represent the largest customer segment, closely followed by Teachers and Retirees. In contrast, Traders account for the smallest share, indicating a potential opportunity to improve engagement within this group while maintaining strong performance among the top professions.

# Customer Distribution Across Gender
The gender distribution is nearly balanced, with females representing a slight majority at 51.2% (256 customers) compared to males at 48.8% (244 customers), indicating no significant gender disparity in the customer base.

# Customer Segment Distribution
The customer segmentation analysis indicates that the Retail segment dominates the customer base, accounting for over half of total customers (57.2%), making it the primary driver of business volume. The Corporate segment follows with a significant share (33.8%), contributing a substantial portion to overall customer distribution. In contrast, the Private segment represents a relatively small fraction (9%), highlighting a potential opportunity for targeted growth strategies to expand this underrepresented segment.


## RECCOMENDATION

The analysis indicates a maturing customer base with a recent decline in growth, highlighting the need to strengthen customer retention strategies and investigate potential causes of churn.

To drive expansion, the business should leverage the strong performance in the South region by replicating its successful strategies in lower-performing regions such as the Western and Northern regions. Additionally, while the Retail segment remains the primary driver, there is a clear opportunity to grow the underrepresented Private segment through targeted offerings and marketing.

From a customer profile perspective, the company should continue to focus on key segments such as Engineers, Teachers, and Retirees, while developing strategies to better engage Traders, who currently represent the smallest group.

Finally, to sustain long-term growth, the business should invest in innovation and targeted campaigns aimed at younger demographics, ensuring a balanced and inclusive approach across gender and customer segments.
