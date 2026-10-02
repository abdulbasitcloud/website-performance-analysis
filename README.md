# Website Performance Dashboard

A Power BI dashboard that shows how visitors use a website: page views, session time, bounce rate and conversion rate.

## Overview
Understanding website performance helps a business improve user experience and increase conversions. This project analyses visitor data and presents the main metrics in one interactive dashboard, so a non-technical user can explore the results and filter by exit page.

## Dataset
File: `website_performance_analytics.csv` (5,870 visitors)
Source: Practice dataset from the Udemy course "72 Days of Data Analyst Bootcamp".

| Column | Meaning |
|---|---|
| Visitor_ID | Unique ID for each visitor |
| Page_Views | Pages viewed in the session |
| Session_Duration | Length of the session in seconds |
| Bounce_Rate | Bounce value for the visitor (a bounce means leaving after viewing one page) |
| Conversion_Rate | Conversion value for the visitor (a conversion is a desired action, such as a purchase or sign-up) |
| Traffic_Source | Where the visitor came from: Direct, Organic, Social Media or Referral |
| Exit_Pages | The page the visitor left from |
| Load_Time | Page load time |
| Visitor_Type | New or Returning |
| City | City of the visitor (used for the map) |

## Dashboard
<img width="910" height="520" alt="website-performance-dashboard" src="https://github.com/user-attachments/assets/730561b2-3feb-47d3-b595-3191496e28b9" />

## What I Built
- **Data preparation:** loaded the CSV into Power BI, formatted Bounce_Rate and Conversion_Rate as percentages, and set the data category of City so the map works.
- **Page buttons:** Blog, Checkout, Contact Us, Homepage and Product Page buttons filter the whole dashboard by exit page.
- **KPI cards:** average page views, average session duration, average bounce rate, average conversion rate, total visitors and high converter %.
- **Charts:** two donut charts (bounce rate and conversion rate by visitor type), a bar chart (conversion rate by traffic source) and a map (conversion rate by city).
- **Table:** top 100 visitors by conversion rate, with data bars on the numeric columns.

## DAX Measures
```
Avg Page Views = AVERAGE('website data'[Page_Views])
Total Visitors = DISTINCTCOUNT('website data'[Visitor_ID])
High Converters = CALCULATE(COUNTROWS('website data'), 'website data'[Conversion_Rate] >= 0.1)
High Converter % = DIVIDE([High Converters], COUNTROWS('website data'))
```
- `AVERAGE` gives the average page views for the visitors currently selected.
- `DISTINCTCOUNT` counts each visitor once.
- `CALCULATE` with `COUNTROWS` counts only the visitors with a conversion rate of 10% or more.
- `DIVIDE` calculates the percentage safely, without errors when the total is zero.

## Key Findings
- Bounce rate and conversion rate are almost the same for New and Returning visitors (about 50% and 5%).
- All traffic sources (Direct, Organic, Social Media, Referral) convert at a similar rate of about 5%.
- The top 100 visitors by conversion rate all cluster around 10%, whatever their session duration or page views.
- 276 of 5,870 visitors (about 4.7%) reach the 10% conversion level.

## Limitations and Next Steps
- The data is one flat table with no date field, so I could not analyse trends over time.
- Visitor type, traffic source and city show very similar results, so they do not explain differences in conversion.
- Next: analyse exit pages and load time against bounce rate, add a date field, and test whether any differences are statistically significant.

## Tools Used
Power BI Desktop, DAX


