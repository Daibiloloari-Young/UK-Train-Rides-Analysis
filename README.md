# UK-Train-Rides-Analysis
An Excel project analyzing UK train ticket sales and operational performance. The dataset includes ticket purchases, pricing, travel details, and operational outcomes such as delays and refunds. The goal is to derive actionable insights to improve revenue, customer experience, and operational efficiency.

## Table of Contents
- [Project Overview](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#project-overview)
- [Project Scope](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#project-scope)
- [Project Objectives](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis#project-objectives)
- [Expected Outcome](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#expected-outcome)
- [Document Purpose](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#document-purpose)
- [Use Case](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#use-case)
- [Data Source](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#data-source)
- [Data Cleaning and Processing](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#data-cleaning-and-processing)
- [Data Analysis](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#data-analysis)
- [Data Visualization](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#dashboard-visualization)
- [Recommendation](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#recommendation)
- [Conclusion](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/edit/main/README.md#conclusion)

## Project Overview
This project involves an in-depth analysis of UK train ticket transactions using Microsoft Excel. The analysis focuses on uncovering patterns in revenue, customer purchasing behavior, peak travel periods, and operational challenges, including delays and refunds.

 ## Project Scope
The project covers a comprehensive analysis of train ticket transactions, including, Ticket purchases and pricing, Travel schedules and stations.The analysis spans multiple months and provides insights into both sales and operational efficiency.

## Project Objectives
The primary objectives of this analysis are:
- **Sales Analysis:** Understand revenue trends across months
- **Customer Behavior:** Identify preferred ticket types, classes, and payment methods
- **Operational Insights:** Analyze delays, cancellations, and refunds
- **Peak Analysis:** Identify busiest travel times and stations
- **Pricing Strategy:** Evaluate how ticket types impact revenue

## Expected Outcome
The analysis aims to provide:
- Total revenue generated
- Monthly sales trends
- Peak travel times
- Most profitable stations
- Customer purchasing patterns
- Refund and operational insights
- Business recommendations for improvement and promotional strategies.

## Document Purpose
This documentation serves as a guide for railway operators and stakeholders to improve revenue generation, customer experience, and operational efficiency.

## Use Case
Stakeholders Benefiting from the Analysis

**1. Transport Operators / Railway Management**
-	Identify high-revenue routes and stations to prioritize operations 
- Optimize pricing strategies based on ticket demand and customer behavior 
- Monitor refund patterns to reduce revenue loss

**2. Operations Team**
- Identify peak travel times to improve train scheduling 
- Allocate resources efficiently during high-demand periods 
- Reduce delays and cancellations by analyzing operational patterns
  
**3. Marketing & Revenue Team**
- Promote advance tickets to increase early bookings 
- Design targeted campaigns for railcard adoption 
- Optimize pricing and promotions based on customer preferences
  
**4. Customer Experience Team**
-	Analyze refund trends to improve service reliability 
-	Enhance passenger satisfaction by reducing delays 
-	Understand customer behavior to improve service offerings

This project simulates how a railway company can leverage data analytics to drive operational and revenue decisions for business growth and enhance customer satisfaction.

## Data Source
The dataset for this project is sourced from the Maven Analytics [website](https://app.mavenanalytics.io/datasets?search=uk) designed specifically for practice purposes. It is presented in an Excel file with a single table comprising 31,653 rows and 18 columns. The dataset includes key attributes essential for a comprehensive analysis, such as:

**Key Fields Include:**

- Transaction ID: Unique identifier for an individual train ticket purchase
- Date & Time of Purchase: Date the ticket was purchased
-	Ticket Type & Class: Time the ticket was purchased
-	Payment Type: Whether the ticket was purchased online or directly at a train station
-	Payment Method: Payment method used to purchase the ticket (Contactless, Credit Card, or Debit Card)
-	Railcard: Whether the passenger is a National Railcard holder (Adult, Senior, or Disabled) or not (None).
-	Ticket Class: Seat class for the ticket (Standard or First)
-	Ticket Type: When you bought or can use the ticket.
-	Price: Final cost of the ticket in USD
-	Departure Station: Station to board the train
-	Arrival Destination: Station to exit the train
-	Date of Journey: Date the train departed
-	Departure Time: Time the train departed
-	Arrival Time: Time the train was scheduled to arrive at its destination (can be on the day after departure)
-	Actual Arrival Time: Time the train arrived at its destination (can be on the day after departure)
-	Journey Status: Whether the train was on time, delayed, or cancelled
-	Reason for Delay: Reason for the delay or cancellation
-	Refund Request: Whether the passenger requested a refund after a delay or cancellation
  
Each of these variables contributes crucial insights, collectively painting a vivid portrayal of the UK Train Dataset.

## Data Cleaning and Processing

Ensuring data quality is an important step in any data analysis process, as it directly impacts the accuracy and reliability of insights, making sure they are free from errors. Clean data makes the analysis process smoother, helping researchers, analysts, and decision-makers to draw meaningful conclusions and make informed decisions based on the information. After thoroughly checking the data for quality and suitability, including looking for errors, inconsistencies, missing values, and duplicates. I found that the dataset is well-organized and consistent. However, several preprocessing and transformation steps were carried out to prepare the data for analysis.

**Data Cleaning Steps**

The following checks and cleaning steps were performed:

- **Missing Values Check:**
The dataset was checked for missing values across all columns. Most of the data was complete.
However, some columns, like Reason for Delay, had empty cells. These were not errors. They simply mean that the train was not delayed and arrived on time.
Because of this, the missing values were kept as they are, since they help show the difference between delayed and on-time journeys.

  #### Duplicate Records:
The dataset was checked for duplicate transaction records using the Transaction ID. No duplicates were identified.

#### Data Type Validation:
Ensured all columns had appropriate data types:

- Dates → Date format
-	Times → Time format
-	Price → Numeric format
  
#### Consistency Check:
Verified uniform naming across categorical fields such as:

- Payment Method (e.g., Contactless, Credit Card, Debit Card)
-	Ticket Type (Advance, Anytime, Off-Peak)
-	Ticket Class (Standard, First Class)
The dataset was well-structured and required minimal cleaning.

- **Additional Data Processing Steps**
  
**1. Creation of New Columns**
To enhance analysis and enable deeper insights, new columns were created:

- Month Column
Extracted from Date of Purchase using the formula below:

```=TEXT([Date of Purchase], "MMM")```

- Year Column
Extracted using using the formula below:

```=YEAR([Date of Purchase])```

**Why This Was Important**

-	It enabled monthly and yearly trend analysis
-	Allowed use of slicers for interactive dashboards
-	Simplified grouping of data for pivot tables
-	Improved readability compared to the raw date format
  
These columns were essential for analyzing sales trends over time and identifying seasonal patterns.

## Data Analysis

The primary aim of this analysis is to derive valuable insights from Pizza Sales Place data by conducting a comprehensive examination of key factors. This multifaceted exploration involves several pivotal objectives. Firstly, it seeks to know the total revenue and the sales trend, and how they change over time. Secondly, the analysis aims to identify the most used payment method by customers. Thirdly, a detailed investigation into the departure stations that generated the most revenue. Fourthly, to know the most used payment method to understand which the customer prefers. Lastly, to know the peak travel time.

Key Benefits Include, Revenue Optimization: Helps identify high-performing stations, ticket types, and peak periods to improve revenue generation, Customer Insights: Identify customer preferences in ticket types, payment methods, and travel times, Service Improvement: It highlights refund patterns and delays, helping to improve service reliability and customer satisfaction, Data-Driven Decision Making: It also enables stakeholders to make informed decisions based on real data rather than assumptions
As a result, this analysis provides insights addressing the following questions.

**1. What is the total revenue and sales trend?**

This question aims to assess the total annual revenue and identify any sales patterns that vary over time. This helps understand the financial performance of the UK Train Rides and reveals seasonal trends, providing insights into how sales fluctuate throughout the year.

To understand revenue performance, a pivot table was created using the Month column in the rows and Price in the values section (summed). A line chart was used to visualize the monthly sales trend. This visualization provides a clear picture of sales dynamics over the year, highlighting any recurring patterns or anomalies that require attention.

**Total Revenue: $741,921**

**Seasonality in Sales.**

![](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/blob/main/Monthly%20Sales%20Trend.png)

From the analysis above;
-	Revenue is highest in the early months of the year, particularly in January
-	There is a noticeable fluctuation in revenue across the months
-	A decline is observed toward the end of the year

**2. What are the most used payment methods?**

This question aims to understand customers’ preferences when it comes to payment methods. A pivot table was created using Payment Method as rows and Price as values (sum). A column chart was used for visualization.

![](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/blob/main/Sales%20By%20Payment%20Method.png)

From the analysis above;
-	Credit card is the most used payment method
-	Contactless payments also account for a large share
-	Debit card usage is relatively lower

**3. Which ticket types are most popular?**

This question aims to understand the ticket types the customer chooses to purchase. A pivot table was created using Ticket Type as rows and Price (summed) as values, giving the percentage of each ticket type. A pie chart was used to show the distribution.

![](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/blob/main/Percentage%20By%20Ticket%20Type.png)

From the analysis above;
-	Advance tickets are the most purchased
-	Off-peak and Anytime tickets follow
-	Customers are price-sensitive and prefer discounted tickets

**4. Which ticket class generates the most revenue?**

This question aims to understand the ticket class most customers go for and which generates the highest revenue. A pivot table was created using Ticket Class and Price (sum). A column chart was used for visualization.

![](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/blob/main/Sales%20By%20Ticket%20Class.png)

From the analysis above;
-	Standard class generates the majority of revenue
-	First class contributes less
-	Most passengers prioritize affordability over luxury

**5. Which stations generate the most revenue?**

This question aims to understand the top major stations used by customers that contribute significantly to total revenue, highlighting the importance of urban transit hubs. A pivot table was created using Departure Station and Price (sum). A bar chart was used to highlight top stations.

To enhance clarity and focus on significant insights, the filter pane was employed to display only the top 5 departure stations determined by Price.

![](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/blob/main/Top%205%20Departure%20Station.png)

From the analysis above;
-	Major stations such as London Kings Cross, London Euston, and Liverpool Lime Street contribute significantly to total revenue


**6. What are the peak travel times?**

The primary aim of this question is to identify the specific travel time when customers travel. Understanding peak hours is crucial.

To achieve this, a pivot table was created. The time column was placed in the row section, which was set to hours, and transaction_id was placed in the value section to count the number of transactions. The results were visualized using a column chart.

![](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/blob/main/Peak%20Travel%20Time.png)

From the analysis above;
-	Peak travel time occurs in the evening, especially around 7 PM
-	Morning hours also show high activity
-	Travel demand is highest during commuting hours
 

**7. KPI Metrics Creation**

To support quick insights on the dashboard, key performance indicators (KPIs) were created using Pivot Tables.
-	Total Refund Requests:
Calculated by counting the number of refund requests to measure customer dissatisfaction and service issues.
-	Total Departure Stations:
Calculated by counting the number of unique departure stations to understand how widely the service operates.
These KPIs were designed to give a high-level overview of operational performance and customer behavior, making it easier for stakeholders to quickly assess key trends without going through detailed charts.

## Dashboard Visualization

![](https://github.com/Daibiloloari-Young/UK-Train-Rides-Analysis/blob/main/UK%20Train%20Rides%20Dashboard.png)

## Recommendation

-	Based on the provided analysis, here are several recommendations for Pizza Sales Place:
-	Monitoring refund trends can help identify pain points in the customer journey and guide improvements in service delivery. 
-	Delays and refund requests indicate areas of service disruption. Addressing common causes of delays can improve customer satisfaction and reduce refund rates. 
-	Since most ticket purchases occur in the evening (around 7 PM), the system should be optimized to handle high traffic during this period to avoid delays or failed transactions. 
-	Stations with high ticket sales should be prioritized for better resource allocation, staffing, and service improvements. 
-	Insights on ticket types and purchase behavior can be used to design better pricing strategies and promotional offers.

## Conclusion

By Implementing these recommendations, UK Train Rides can help improve operational efficiency, increase revenue, and enhance overall customer satisfaction. 

I am open to Data Analyst roles in an organization where I can showcase my skills, take more responsibilities, grow professionally, and contribute to data-driven decision-making.
Thank you for reading.

You can reach me on (daibi616@gmail.com)

