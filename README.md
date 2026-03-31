# Orange Telecom Churn

![orange-16463](https://github.com/user-attachments/assets/453fee86-50aa-46f0-b01e-f4c22924bbdc)


# Project Overview
This project focuses on analyzing the Orange Telecom Customer Churn dataset to identify patterns and factors that influence customer attrition. The dataset contains customer usage behavior, service plans, billing information, and customer service interactions, along with a target variable indicating whether a customer churned.

# Dataset Description
The dataset used in this analysis contains customer-level information from a telecom company (Orange Telecom) and is designed to support the study of customer churn behavior. Each record represents an individual customer and includes details on their service usage, subscription plans, customer service interactions, and churn status.

The dataset consists of **2,666** customers and captures key attributes that help explain why customers choose to stay or leave the service.

### Key Features in the Dataset
#### Customer Information
- State – Geographic location of the customer
- Area Code – Regional code associated with the customer
  
#### Account Details
- Account Length – Number of days the customer has been with the company (tenure)

#### Service Plans
- International Plan – Indicates whether the customer subscribes to an international calling plan.
- Voice Mail Plan – Indicates whether the customer has a voice mail subscription.

#### Usage Metrics
- Call Usage by Period (Day, Evening, Night) – Minutes and associated charges 
- International Usage (Minutes / Charges) – Total international call usage and cost.

#### Customer Service Interaction
- Customer Service Calls – Number of times the customer contacted customer support.
  
#### Target Variable
- Churn – Indicates whether the customer has left the service (True/False)

# Dashboard Overview
<img width="1563" height="654" alt="Telecom Churn Overview" src="https://github.com/user-attachments/assets/4772798d-199c-4a59-8f73-acf6ec305ec9" />

### Customer Service Plan Dashboard
<img width="1563" height="657" alt="Telecom churn Customers plan usage" src="https://github.com/user-attachments/assets/77d85c19-b1fc-4c8b-bb85-49adfa2e59d6" />


# Problem Statement
Orange Telecom is experiencing customer churn and lacks clear insight into the key factors driving customer attrition. This analysis aims to identify the impact of customer service interactions, plan subscriptions, usage patterns, and customer tenure on churn, in order to support data-driven strategies for improving customer retention and reducing churn rates.

# Key Performance Indicators (KPIs)
- **Total Customers: 2666** - Total number of customers.
- **Churn Rate: 14.55%** - Percentage of customers who have churned
- **Churned Customers: 388** - Total number of customers who left
- **Average Account Length: 100.62 Days** - Customers stay with the company for approximately 3.3 months on average.
- **Average Customer Service Calls: 1.56** - Average number of service calls made by customers


# Business Objectives
#### Customer Service Performance Objectives
- Determine how the frequency of customer service calls influences the probability of a customer churning.
- Find the tipping point (e.g., 3+ calls) where customers are most likely to become dissatisfied.
- Compare average service call frequency between churned and retained customers to uncover risk indicators.
- Identify states with high customer service activity that may indicate regional service quality issues.
- Determine the main factors (service calls, plans, usage, tenure) influencing customer attrition.

#### Plan & Usage Driver Objectives
- Evaluate whether customers subscribed to International Plans are more likely to churn compared to those without.
- Analyze whether total daily and international charges differ significantly between churned and retained customers.
- Assess whether customers with international plans have higher churn rates.
- Determine if newer customers are at higher risk and how account length affects churn probability.
- Investigate whether customers with voice mail plans are less likely to churn.
- Examine how call usage and charges influence customer churn behavior.

# Key Finding and Insights

#### Customer Service Calls Strongly Drive Churn
<img width="639" height="247" alt="Screenshot 2026-03-30 165946" src="https://github.com/user-attachments/assets/b01d21e3-bb1a-4d06-bbca-74933b70519c" />

Churn rate increases sharply as customer service calls increase
Customers with 6–8 calls show churn rates above 60%–100%
Low call frequency (0–2 calls) has very low churn (~10%)

👉 Insight:
Frequent complaints are a major predictor of churn

⚠️ 2. Critical Threshold Identified (4+ Calls)
Churn jumps significantly after 4 service calls (~48%+)
Continues rising beyond this point

👉 Insight:
There is a clear “tipping point” at 4 calls

📞 3. Churned Customers Contact Support More
Average service calls:
Churned customers: ~2.21
Retained customers: ~1.45

👉 Insight:
Churned customers are more engaged with support due to issues

🌍 4. Regional Differences Exist
Some states show higher churn concentration on the map

👉 Insight:
Possible:

Service quality issues
Network/infrastructure problems
Regional competition
📉 5. High Call Frequency Segment is Most At Risk
High frequency group → ~64% churn
Medium → ~24%
Low → ~11%

👉 Insight:
Customers with frequent complaints are high-risk segment

💳 6. International Plan Users Show Mixed Behavior
Majority of customers do NOT use international plan
Churn exists in both groups but needs closer rate comparison

👉 Insight:
International plan alone is not the strongest churn driver, but still relevant

📬 7. Voice Mail Plan Supports Retention
Majority of retained customers have voice mail plans

👉 Insight:
Voice mail plan may act as a retention factor

⏳ 8. New Customers Are More Likely to Churn
Highest churn observed in early tenure groups (e.g., 0–8 months)
Churn decreases as tenure increases

👉 Insight:
Customer loyalty improves over time

💰 9. Higher Charges Slightly Linked to Churn
Churned customers show slightly higher average daily charges

👉 Insight:
Pricing/value perception may influence churn

📊 10. Overall Churn Rate is Significant
Churn Rate: 14.55%
388 out of 2666 customers churned

👉 Insight:
Churn is moderate but important enough to act on


# Recommendation 
- Improve customer service efficiency by ensuring most issues are resolved within the first 2–3 interactions, reducing the need for repeated calls.
  
- Introduce an early warning system to flag customers who reach 3 or more service calls, and proactively engage them with support or retention offers before they churn.
  
- Provide targeted support for high-risk customers (those with frequent service calls or high usage) through personalized follow-ups, discounts, or service recovery actions.
  
- Strengthen the onboarding experience for new customers by offering early guidance, check-ins, and incentives within the first few months of subscription.

- Review and optimize pricing strategies, particularly for international plans and high-usage customers, to ensure customers perceive fair value for the services they receive.

- Promote the adoption of value-added services such as the voice mail plan through bundles, free trials, or awareness campaigns, as they appear to support customer retention.

- Investigate regions with higher churn or service call activity and address potential issues such as network quality, service availability, or local competition.

# Tools And Techniques
#### 🛠️ Tools
- *Power BI* – Used for data cleaning, transformation, modeling, and building interactive dashboards.
- *Microsoft Excel* - Used for initial data inspection and understanding dataset structure

#### 📊 Techniques
- *Data Cleaning & Transformation* – Handling data types, creating calculated columns (e.g., tenure groups, risk tiers)
- *DAX (Data Analysis Expressions)* – Creating measures such as:
  - Total Customers
  - Churn Rate
  - Churned Customers
  - Retained Customers
- *Data Visualization* – Using charts such as:
    - Bar charts
    - Column charts
    - Donut charts
    - KPI cards
- *Customer Segmentation* – Grouping customers based on:
    - Service call frequency
    - Tenure
    - Usage behavior
- *Exploratory Data Analysis (EDA)* – Identifying patterns, trends, and relationships between variables
- *KPI & Dashboard Design* – Creating key metrics and a user-friendly dashboard layout for insights

# Conclusion
Customer churn at Orange Telecom is primarily driven by poor customer service experience, particularly among customers having frequent interactions with customer support. A clear pattern shows that as the number of service calls increases, the likelihood of churn rises significantly, with a noticeable tipping point after multiple unresolved issues.

Additionally, newer customers are more vulnerable to churning, indicating gaps in early customer experience and onboarding. While factors such as pricing and plan subscriptions play a role, they are less influential compared to service-related issues. However, value-added services like the voice mail plan appear to support customer retention.

Overall, the findings highlight that improving customer service efficiency, proactively identifying at-risk customers, and enhancing early customer engagement are critical to reducing churn. By leveraging these insights, Orange Telecom can implement targeted strategies to improve customer satisfaction, strengthen loyalty, and drive long-term business performance.

