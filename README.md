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
- [Data Analysis]
- [Data Visualization]
- [Recommendation]
- [Conclusion]

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

- **Duplicate Records:**
The dataset was checked for duplicate transaction records using the Transaction ID. No duplicates were identified.

- **Data Type Validation:**
Ensured all columns had appropriate data types:

- Dates → Date format
-	Times → Time format
-	Price → Numeric format
  
- **Consistency Check:**
Verified uniform naming across categorical fields such as:

- Payment Method (e.g., Contactless, Credit Card, Debit Card)
-	Ticket Type (Advance, Anytime, Off-Peak)
-	Ticket Class (Standard, First Class)
The dataset was well-structured and required minimal cleaning.

- **Additional Data Processing Steps**
- 
**1. Creation of New Columns**
To enhance analysis and enable deeper insights, new columns were created:

- Month Column
Extracted from Date of Purchase using:

=TEXT([Date of Purchase], "MMM")
Year Column
Year Column
Extracted using:
=YEAR([Date of Purchase])

Why This Was Important
•	It enabled monthly and yearly trend analysis
•	Allowed use of slicers for interactive dashboards
•	Simplified grouping of data for pivot tables
•	Improved readability compared to the raw date format
These columns were essential for analyzing sales trends over time and identifying seasonal patterns.

Data Analysis
The primary aim of this analysis is to derive valuable insights from Pizza Sales Place data by conducting a comprehensive examination of key factors. This multifaceted exploration involves several pivotal objectives. Firstly, it seeks to know the total revenue and the sales trend, and how they change over time. Secondly, the analysis aims to identify the most used payment method by customers. Thirdly, a detailed investigation into the departure stations that generated the most revenue. Fourthly, to know the most used payment method to understand which the customer prefers. Lastly, to know the peak travel time.

Key Benefits Include, Revenue Optimization: Helps identify high-performing stations, ticket types, and peak periods to improve revenue generation, Customer Insights: Identify customer preferences in ticket types, payment methods, and travel times, Service Improvement: It highlights refund patterns and delays, helping to improve service reliability and customer satisfaction, Data-Driven Decision Making: It also enables stakeholders to make informed decisions based on real data rather than assumptions
As a result, this analysis provides insights addressing the following questions.

