# 📦 E-Commerce Sales Funnel Analysis
## 🚀 Project Overview
This project analyzes e-commerce customer behavior using SQL to understand how users progress through the online shopping journey, from their first page view to completing a purchase.

Using event-level customer data, I explored funnel conversion rates, traffic source performance, time to conversion, and revenue metrics to identify potential areas of customer drop-off and opportunities for improving the purchasing experience.

## 🔎 Business Questions
This analysis aims to answer the following questions:

- How many unique users reach each stage of the sales funnel?
- What percentage of users progress from one stage to the next?
- Where do the largest drop-offs occur in the purchasing journey?
- Which traffic sources generate the most purchases and have the highest conversion rates?
- How long does it take users to complete a purchase?
- How much revenue is generated, and what is the average order value?
- What opportunities exist to improve customer conversion and revenue?

## 📊 The Dataset
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

## 🛠️ Tools & Technologies
1. MySQL — Data querying, aggregation, and analysis
2. SQL — Common Table Expressions (CTEs), conditional aggregation, COUNT(DISTINCT), date functions, and window/journey analysis
3. GitHub — Project documentation and version control

## 💡 Analysis
**The analysis tracks five primary funnel events:**
1. page_view
2. cart
3. checkout
4. payment
5. purchase

 ### 📌 Funnel Stage Analysis 
 Counts the number of distinct/ unique users at each stage of the sales funnel
   
 ### 📈 Conversion Rate Analysis 
 Conversion rates are calculated between each stage of the funnel:
 - View → Cart
 - Cart → Checkout
 - Checkout → Payment
 - Payment → Purchase
 - View → Purchase (overall conversion)

This helps identify where the largest proportion of users leave the funnel.

### 🚦 Traffic Source Analysis
Funnel performance is also segmented by the traffic sources to the e-commerce site
**Traffic Sources:**
- Paid Ads
- Social media
- Email
- Organic

Compare these values between each traffic source:
- Number of visitors
- Add-to-cart users
- Purchasers
- Cart conversion rate
- Purchase conversion rate
- Cart-to-purchase conversion rate

### ⏳ Time to Conversion Analysis 
For users who completed a purchase, the project calculates the **average amount of time between:**
- Page view → Add to cart
- Add to cart → Purchase
- Page view → Purchase

This provides additional context around the customer journey beyond simple conversion percentages.

### 💲 Revenue Analysis
The revenue analysis calculates:

- Total visitors
- Total buyers
- Total orders
- Total revenue
- Average order value
- Revenue per buyer
- Revenue per visitor

These metrics connect funnel activity to business outcomes.

## 🔑 Key Findings & Recommendations 
**1. Funnel Conversion and Drop-Off**
 - 4,268 unique users recorded a page view, while 708 unique users recorded a purchase, resulting in an overall page-view-to-purchase ratio of 16%.
 - The largest stage-to-stage drop-off occurred between page view and add to cart, where the number of distinct users decreased by 68%.
 - The payment-info-to-purchase transition had the highest observed stage-to-stage conversion rate at 92.19%.

These results identify the initial browsing-to-cart transition as a key area for further investigation.

**2. Marketing Strategy**
- Reduce the budget for social media for sales: Social media drives 1253 page viewers (website volume and traffic) but has the lowest purchase conversion rate of 7%
- Email had the highest observed purchase conversion rate at 34%, with 151 purchasers from 445 page viewers
- Double Down and Focus on Email Marketing: Email is the highest-converting channel. Try implementing an email capture pop-up for social media visitors to get them on the email list

**3. Revenue Performance**
- Total recorded purchase revenue was $76,037.93, generated from 708 purchase events
- Average order value was $107.40
- Revenue per page viewer was $17.82

**4. Customer Journey**
- Purchasers with recorded view and purchase timestamps had an average page-view-to-purchase interval of approximately 24.55 minutes
- The average view-to-cart interval was 11.19 minutes, while the average cart-to-purchase interval was 13.36 minutes

This analysis adds a time-based perspective to the customer journey and helps describe how quickly recorded purchasers progress through the funnel.
