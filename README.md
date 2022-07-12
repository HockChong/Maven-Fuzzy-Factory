# Project Introduction

You’ve just been hired as an eCommerce Database Analyst for Maven Fuzzy Factory, an online retailer which has just launched their first product.

As a member of the startup team, you will work with the CEO, the Head of Marketing, and the Website Manager to help steer the business.

You will analyze and optimize marketing channels, measure and test website conversion performance, and use data to understand the impact of new product launches.

✏️ THE OBJECTIVE

Use SQL to:

- Access and explore the Maven Fuzzy Factory database
- Become the data expert for the company, and the go-to person for mission critical analyses
- Analyze and optimize the business’ marketing channels, website, and product portfolio


# Table of Contents
- Entity Relationship Diagram

# Entity Relationship Diagram

![image](https://user-images.githubusercontent.com/64703507/177375965-aa86eaff-4cd0-47b5-b86e-ed198d5ff01f.png)

# Analyzing Traffic Sources
![image](https://user-images.githubusercontent.com/64703507/178546710-bce8c773-630a-4f1d-8302-d0d415e78871.png)

![image](https://user-images.githubusercontent.com/64703507/177376359-9dac0d02-186c-4ae8-9922-909c7bccc1f0.png)

```sql
SELECT 
	utm_source, 
  utm_campaign, 
  http_referer,
  COUNT(DISTINCT website_session_id) AS number_of_sessions
FROM website_sessions
WHERE created_at < '2012-04-12'
GROUP BY utm_source, utm_campaign, http_referer
ORDER BY number_of_sessions DESC
```

![image](https://user-images.githubusercontent.com/64703507/177377849-d3e890d1-5ef3-4a30-8f63-03bf590b9f3d.png)

![image](https://user-images.githubusercontent.com/64703507/178548028-6265cb11-ad16-42d8-a3ed-4f698b545be9.png)

![image](https://user-images.githubusercontent.com/64703507/178548135-a9c28b98-a573-4a3c-9ce8-dd3b1f13fc28.png)

# Bid Optimization & Trend
![image](https://user-images.githubusercontent.com/64703507/178547025-bd9002d6-e35a-42eb-b43f-85d25ba7784c.png)
