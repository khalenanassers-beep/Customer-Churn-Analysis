# 📙 Business Report: Churn Analysis
### Prepared for a Managers

---

## **1. Objective**

The management teams wants to understand why customers churn, how churn affects revenue, and which customer segments should be prioritized for retention efforts in the next quarter.

The goal is to determine:
- Which customer types and industries are most at risk
- How engagement, CLV, and CPC relate to churn
- Where the business should focus to reduce churn and protect revenue

## **2. Data Warning**
Before diving into the results, it’s important to acknowledge a few things about the dataset

- *We don’t know exactly where the data comes from or how it was collected.*
  
That means there could be some natural bias in what’s included (for example, Certain industries being over‑represented or the timeframe).

- *We also don’t know whether this is the full picture*
  
Some important variables may be missing, such as number of customers (which is key in the churn % calculation), customer satisfaction scores, support ticket history or competitor activity.

Even with these limitations, the dataset still gives enough clarity to explore the relationship between fuel type, mileage, and price, and to confidently answer the business owner’s main question.

## **3. Evidence & Insights**

### **Evidence**
The statistical analysis confirms that churn is strongly connected to several key variables:

<img width="947" height="506" alt="image" src="https://github.com/user-attachments/assets/06eafa59-18a6-4790-a979-c804a6c98f3a" />

Using the Spearman correlation test between selected variables and the numeric churn indicator (1 = churned) helps us understand how each feature behaves in relation to churn.
For example, the variable “How often did the customer check statistics” shows a small negative correlation with churn. This means that customers who rarely check their statistics throughout the year are more likely to churn, which is  a subtle but important behavioral signal.

This also helps us identify the key metrics that influence churn:

1. CLV (Customer Lifetime Value)
   <img width="947" height="506" alt="image" src="https://github.com/user-attachments/assets/82e4729e-419d-4db4-b52f-cf5bc7c7b2bf" />

- Churned customers have significantly lower CLV (below 2.73 years), while the retained customer have in average 4.47 years (+1.73 years mores).

2. Engagement (Traffic Contacts)
   <img width="947" height="506" alt="image" src="https://github.com/user-attachments/assets/4ee3df8b-3880-47cd-ba2b-d2d1caa300e1" />
- Logistic regression shows a clear negative relationship, as the traffic increases the churn probability dicreases and vice versa.
  
3. CPC (Cost per Click)
  <img width="947" height="506" alt="image" src="https://github.com/user-attachments/assets/e4b828a3-43d9-4f90-a98a-3bef30a12c3a" />
   
- Churned customers show a noticeably higher CPC at EU 5.61, which is EU 1.51 more than retained customers. When you compare this to typical search‑engine benchmarks — around $5.26 on Google Search and $1.50–$2.00 on Bing — both groups are already above market averages, but churned customers stand out even more.

4. Customer Type & Industry
  
  <img width="947" height="506" alt="image" src="https://github.com/user-attachments/assets/e6982ee0-1926-416c-b703-6312131dc275" />
  
- New customer (N) appear to have a higher churn rate 38% than old (A) customer, which the graphs allows us to see that old customer has a higher proportion of retained customers. 
  <img width="947" height="506" alt="image" src="https://github.com/user-attachments/assets/757860dc-72fa-41f1-ab58-3ef2563d7f86" />
  
- The four main industries show churn rates between 17% and 30%
- It’s also interesting that Products(Produkte) is the largest industry in the dataset (66% of the customers) and has a 20% churn rate. Because of its size, even small improvements in retention there could make a meaningful difference for the business.
- Customers without an industry category have an extremely high churn rate of 91.7% (there are only 24 customers). That’s a red flag worth highlighting but carefully due to size, since missing information often signals weaker relationships or poor data quality.
  
4. Financial Impact
   <img width="824" height="532" alt="image" src="https://github.com/user-attachments/assets/b2cd6360-ce98-4768-8f5f-d1451f28b87d" />
- With an expected order intake of EUR 9MM, the expected churn revnue for the next year its EUR 2.1 MM. Leaving a EU 7.8 MM expected revenue for next year. 
  
### Insights
The analysis reveals a clear pattern in how customer characteristics relate to churn:
-High churn rate its 21.22% (1068 customers) out of 5034 customers. 
  > Compared to an average industry estandar (B2B SaaS) which have a low churn rate of 10%. According to Focus Digital.
- Low‑engagement customers are at the highest risk.
- Low‑CLV (below 2 years) customers churn more frequently. Reinforce by the 38% churn rate that new customers have while old customers have a retained (more than +75% of old customers)
- High CPC customers are more likely to churn (above 5$ per click)
- The four main industries show churn rates between 17% and 30%, with the industry "Products" having the largest impact due to having 66% of the customers.
- Considering that 21% of the customers closed done the contracts this year, the revenue loss for the next years its $2.1 M. Which will affect cash flow and bottom line performance. 

---

## **Recommendation**
Based on the analysis, if the the management team wants:

To reduce churn and protect revenue:
Focus on high‑CLV, high‑engagement customers.
These customers are more profitable and more likely to stay when properly supported.

To improve acquisition efficiency:
Drive traffic to new customers, as these customers show higher churn risk.

To stabilize churn in vulnerable segments:
Prioritize retention efforts for:
- New customers
- Customer in the Product category and without one.
- High CPC
  
To maximize financial performance:
- To protect the old customer, ensure they are happy and work on improvements. 
- Reduced overall CPC
- Undestand the new customers type, needs and desire to increase retation.
  
This analysis gives a solid picture of what’s happening — but understanding why it’s happening will require a deeper dive. Factors like service quality, platform functionality, rapidly evolving digital business needs, and the growing role of AI in search all likely play a part.
To move from diagnosis to action, a targeted customer analysis is recommended. 
