# Table of Contents
1. [What is InsightsHub.AI?](#What-is-InsightsHub.AI?)
2. [Testimonial from one of our clients](#Testimonial-from-one-of-our-clients)
3. [How does the product work?](#How-does-the-product-work?) 
4. [What Insights are provided by our platform?](#What-Insights-are-provided-by-our-platform?)
5. [How did I build this solution?](#How-did-I-build-this-solution?)
6. [Our Future Roadmap](#Our-Future-Roadmap)

***
# 1. What is InsightsHub.AI?

InsightsHub.AI is a platform for restaurants to improve business performance through data driven decisions. It leverages business intelligence capability to generate deep insights on order data collected through point-of-sale terminals like ToastTab, Square, etc. We continue to add features like customer sentiment analyzer and sales forecasting leveraging various AI techniques including Natural Language Processing.

This code uses NLP algos to assess the sentiment of customer reviews and provide insights to the restaurants to be able to improve their customer service. 
***
# 2. Testimonial from one of our clients

![image](https://user-images.githubusercontent.com/88556975/165400098-1768d4c9-d572-4916-a848-a087525baced.png)
***
# 3. How does the product work?
**End-to-end steps** below starting with data upload to report generation:
>1. Client uploads order history and order item level breakdown monthly files as is securely through InsightsHub.AI using their account (2 years history stored by POS terminal, and needed for seasonal trends)

>2. Files stored in a database, provided as a service from go-daddy

>3. Files are concatenated in Microsoft Excel (just stacking each monthly file - separately for order level (#1) and order item level (#2) files)

>4. Google reviews are sourced through an online bot (https://botster.io/bots/google-maps-reviews-scraper) for usually under a couple of dollars

>5. Developed machine learnings codes provide reasons of negative and positive sentiments (#3)

>6. 3 files are input to a pre-built Tableau with over 30 preconfigured views and provide instant insights (links below)

>7. Report shared with client with recommendations with the objective to generate concrete actions for improvements

>8. Business Intelligence and ML insights provided deep insights into their business as reported by our clients 

**Tableau dashboard demo on InsightsHub.AI**: https://insightshub.ai/demo.php

**Tableau dashboard link on Public Tableau**: https://public.tableau.com/app/profile/vatsal.garg/viz/Restaurant_Analytics_Order_Level_Data_Tableau_Views/D8_CustReviews?publish=yes![image](https://user-images.githubusercontent.com/88556975/167741778-e903c711-cbc4-47aa-8bed-81c1dfc2ee95.png)

**Refer to files in our repository:**

> **Order Level Data** (Q1 2021 sample): https://github.com/vgrg13/InsightsHub.AI/blob/main/OrderDetails_2021_01_01-2021_03_31.csv

> **Order Item Level Data** (Jan 2021 sample): https://github.com/vgrg13/InsightsHub.AI/blob/main/ItemSelectionDetails_2021_01_01-2021_01_31.csv

> **Sentiment Topics output** from ML Codes : https://github.com/vgrg13/InsightsHub.AI/blob/main/sent_topics_df_final.csv
***
# 4. What Insights are provided by our platform?
**Business Intelligence**
* Sales Volume Trends and seasonal behavior
* Sales trends across Dining options (Lunch/Dinner, etc.) and Order sources (website, GrubHub, etc.) among other dimensions
* Menu items performance, items sales affinity to build creative combos
* Staffing recommendations based on dine-in traffic
* Promotion recommendations to boost sales especially on days with low traffic
* Take out patterns and food pre-preparation recommendations to process customer orders faster

**Insights based on Natural Language Artificial Intelligence/ML Model**
* Rate of Negative sentiments
* Topics of Negative Reviews

All insights, their interpretation and recommendations are provided through Tableau views. A couple of screenshots below for reference

**Customer Sentiments and Topics of Negative and Positive reviews**
![image](https://user-images.githubusercontent.com/88556975/167742045-85fbc56d-8e40-4941-9d56-ce01a84289f0.png)

**A sample of Executive Dashboard with select insights**
![image](https://user-images.githubusercontent.com/88556975/167743768-4beff8a2-169d-4f42-9e94-812de8dc7866.png)

***
# 5. How did I build this solution?

Most restaurants do not have understanding of basic data trends in their business, as simple as distribution of dine-in traffic in different hours of the day. Descriptive analysis using BI tool provides significant insights to businesses. In addition, for certain problems, one would need help from Artificial Intelligence  tools to unearth patterns. As an example, identifying the topics your customers are most dis-satisfied with require use of sophisticated Natural Language Processing AI/ML techniques.

I used Tableau to build a host of pre-configured views applicable to restaurants, and custom views are created as needed. I choose Tableau over other tools based on its ability to generate quality dashboards and its flexibility to create new fields using custom SQL. This Udemy course (https://www.udemy.com/course/tableau10/) was one of my sources to learn Tableau in detail along with youtube videos and tableau community (https://community.tableau.com/s/)

For my first AI use case, which required analyzing customer online reviews, I worked upon building models using Natural Language processing (a branch of machine learning for text analysis). I supplemented my data science skills through a number of online resources. As an example, I found the Youtube Playlist from Krish Naik (Senior Data Scientist with 10+ years of experience and cofounder of iNeuron.ai) very useful to understand the concept of different techniques. I did also tap into articles written by other data scientists on this topic.

NLP Playlist: https://www.youtube.com/playlist?list=PLZoTAELRMXVMdJ5sqbCK2LiM0HhQVWNzm
One of the NLP articles: https://towardsdatascience.com/sentiment-classification-in-python-da31833da01b

**Machine Learning Models**
>Codes are written in python
* Customer Review Sentiment Analysis to find out Rate of Negative Sentiments: https://github.com/vgrg13/InsightsHub.AI/blob/main/Restaurant_Reviews_Sentiment_Analysis.ipynb

* Topics of Negative Reviews: https://github.com/vgrg13/InsightsHub.AI/blob/main/Restaurant%20Reviews%20Topic%20Modeling.ipynb
>Over 10 different libraries are used including vaderSentiment, SentimentIntensityAnalyzer, textblob, gensim, pyLDAvis, pandas, numpy, nltk, re, sklearn, and matplotlib

**Tableau Dashboards Details**

7 distinct dashboards are built with 30+ different charts followed by Executive Summary Dashboard. Details below
* **1) Sales Trends**: High level sales trends (time series view and distribution by key dimensions)
* **2) Year-over-year Sales Trends**: Year over year performance assessment to avoid the seasonality bias
* **3) Order Source Trends**: Deep-dive by Dine in vs. delivery vs. take out
* **4) Meal Type Trends**: Deep-dive by dinner vs. lunch vs. breakfast
* **5) Menu Items Trends**: Deep-dive at 3 levels of menu items: menu groups (appetizer, entrée, etc.), menu subgroup (veg vs non-veg appetizers, salads vs soups, etc.) and lastly at the menu item level
* **6) Order Trends Summary**: Order scorecard including interesting dimensions like avg order size, % gratuity, % sale of beverages, etc.
* **7) Top Customer Complaints**: Negative and positive reviews distribution, topics of negative reviews and ability to read reviews

**Check out our demo**: https://insightshub.ai/demo.php


***
# 6. Our Future Roadmap

We want to include a number of other data sources to continue to unearth insights into topics important for restaurants
* **Optimize your menu** for profitability and reduction in food wastage: Need inventory and supplier purchase history data
* **Impact of weather** on order volume: Source weather forecast data (predictions for rain, storm, snow, etc.)
* **Root causes of delivery delays and insufficient staffing** scenarios: Collect staffing data and delivery timestamps 
* **Impact of price increase** on customer behavior: Collect pricing change data
* **Impact of external factors** on business: Collect Macro-economics trends (e.g., high unemployment rate, or covid infection rate) and Local Demographics data


