Website Performance Dashboard

Introduction
In today's digital age, understanding website performance is crucial for optimizing user experience and increasing conversion rates. This project analyzes key metrics — page views, session duration, bounce rate, and conversion rate — to uncover insights into user behavior and website efficiency. An interactive Power BI dashboard was built to visualize these metrics and support data-driven decisions.

Data Description
The dataset, website_performance_analytics.csv, contains the following variables:
Visitor_ID — Unique identifier for each visitor
Page_Views — Number of pages viewed by the visitor during a session
Session_Duration — Duration of the session in seconds
Bounce_Rate — Percentage of visitors who leave the site after viewing only one page
Conversion_Rate — Percentage of visitors who complete a desired action (e.g., purchase, sign-up)
Traffic_Source — Source from which the visitor arrived at the website (e.g., Direct, Organic Search, Paid Search)
Exit_Pages — Pages from which visitors exit the site
Load_Time — Time taken to load the webpage
Visitor_Type — Type of visitor (New or Returning)
Location — Geographic location of the visitor
Workflow

1. Data Preparation
Loaded website_performance_analytics.csv into Power BI
Converted Bounce_Rate and Conversion_Rate into percentage format with zero decimal points
Assigned the data category "City" to the Location variable

2. Dashboard Creation
Set the dashboard title to "Website Performance Dashboard"
Used Exit_Page as the key filter within the title bar
Built KPI cards for average Page_Views, Session_Duration, Bounce_Rate, and Conversion_Rate
Created the following visuals:
Two donut charts showing average Bounce_Rate and Conversion_Rate by Visitor_Type
A bar chart showing average Conversion_Rate by Traffic_Source
A map chart showing average Conversion_Rate by Location
A table of the top 100 visitors by average Conversion_Rate, with Visitor_ID, Page_Views, Session_Duration, and Conversion_Rate (sorted descending by Conversion_Rate, with cell-based data bars on all columns except Visitor_ID)

Dashboard
<img width="811" height="463" alt="image" src="https://github.com/user-attachments/assets/c859e2d5-ed06-4efb-909d-fb3836260d97" />


Key Findings
Bounce Rate and Conversion Rate are nearly identical between New and Returning visitors (~50% and ~5% respectively)
All traffic sources — Direct, Organic, Social Media, Referral — convert at a similar ~5% rate
The top 100 visitors by conversion rate all cluster around a 10% conversion rate, regardless of session duration or page views

Conclusion
This dashboard provides a clear, at-a-glance overview of website performance metrics. It helps identify trends across visitor types, traffic sources, and locations, and supports data-driven decisions to optimize the user experience and improve conversion rates going forward.

