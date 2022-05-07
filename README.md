# What is InsightsHub.AI?

InsightsHub.AI is a platform for restaurants to improve business performance through data driven decisions. It leverages business intelligence capability to generate deep insights on order data collected through point-of-sale terminals like ToastTab, Square, etc. We continue to add features like customer sentiment analyzer and sales forecasting leveraging various AI techniques including Natural Language Processing.

This code uses NLP algos to assess the sentiment of customer reviews and provide insights to the restaurants to be able to improve their customer service. 

# Testimonial from one of our clients

![image](https://user-images.githubusercontent.com/88556975/165400098-1768d4c9-d572-4916-a848-a087525baced.png)

# How does the product work?
1. Client uploads order history and order item level breakdown monthly files as is securely through InsightsHub.AI using their account (2 years history stored by POS terminal, and needed for seasonal trends)
2. Files stored in a database, provided as a service from go-daddy
3. Files are concatenated in Microsoft Excel (just stacking each monthly file - separately for order level (#1) and order item level (#2) files)
4. Google reviews are sourced through an online bot (https://botster.io/bots/google-maps-reviews-scraper) for usually under a couple of dollars
5. Developed machine learnings codes provide reasons of negative and positive sentiments (#3)
6. 3 files are input to a pre-built Tableau with over 30 preconfigured views and provide instant insights
7. Report shared with client with recommendations with the objective to generate concrete actions for improvements
8. Business Intelligence and ML insights provided deep insights into their business as reported by our clients 

# What Insights are provided by our platform

# How did I build this solution?

# Tableau Dashboards built to identify Trends and Insights

# Machine Learning models built to identify customer sentiments from their reviews and the topics of their positive and negative sentiments 

# Summary and Next Steps

# Extra Read: What was the motivation and the reasearch behind starting InsighsHub.AI for restaurant analytics?
