# E-Commerce-Sales-Funnel-Analysis
## Project Overview
This project analyzes e-commerce customer behavior using SQL to understand how users progress through the online shopping journey, from their first page view to completing a purchase.

Using event-level customer data, I explored funnel conversion rates, traffic source performance, time to conversion, and revenue metrics to identify potential areas of customer drop-off and opportunities for improving the purchasing experience.

## Business Questions
This analysis aims to answer the following questions:

- How many unique users reach each stage of the sales funnel?
- What percentage of users progress from one stage to the next?
- Where do the largest drop-offs occur in the purchasing journey?
- Which traffic sources generate the most purchases and have the highest conversion rates?
- How long does it take users to complete a purchase?
- How much revenue is generated, and what is the average order value?
- What opportunities exist to improve customer conversion and revenue?

## Dataset 
The dataset, user_events.csv, contains e-commerce user activity recorded at the event level.

It includes 9,381 event records and the following seven columns:

Column | Description
|-------|------------|
event_id | Unique identifier for an event
user_id	| Identifier for the user performing the event
event_type | Type of user activity
event_date | Timestamp when the event occurred
product_id | Identifier for the associated product
amount | Purchase amount, where applicable
traffic_source | Source through which the user arrived

## Tools & Technologies
MySQL — Data querying, aggregation, and analysis
SQL — Common Table Expressions (CTEs), conditional aggregation, COUNT(DISTINCT), date functions, and window/journey analysis
GitHub — Project documentation and version control

## Analysis
1. 


