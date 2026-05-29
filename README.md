#  Cross-Platform Engagement Analysis  
###  Reddit × Google Trends Data Analytics Project

---

##  Overview

This project analyzes the relationship between **public search interest (Google Trends)** and **community engagement (Reddit)** across multiple domains such as Technology, Healthcare, Sports, and Politics.

It helps answer:
-  What people are searching for (Demand)  
-  How communities are engaging (Activity)  
-  Where demand and engagement are misaligned  

---

##  Objectives

- Compare **public interest vs community engagement**
- Identify **high-demand but under-served domains**
- Analyze **engagement quality and virality**
- Study **time-based engagement patterns**
- Build a **cross-platform analytical framework**

---

##  Data Collection

### 🔹 Reddit Data
- Collected **9,000+ posts** using Reddit Public API (Python)
- Implemented:
  - Pagination handling  
  - Rate limiting  
- Extracted:
  - Score (upvotes)  
  - Comments  
  - Subreddit & Domain  
  - Timestamp  

### 🔹 Google Trends Data
- Collected **domain-wise search interest**
- Represents **public demand signal**
- Granularity: **daily data**

---

##  Data Preprocessing

- Cleaned and standardized datasets  
- Removed duplicates and null values  
- Converted timestamps to usable formats  
- Aggregated Reddit data:
  - **Post-level → Domain + Date level**
- Aligned both datasets on:
  - **Domain + Date**

---

##  Feature Engineering

Created key metrics:

- **Engagement Score**  
  `Score + 2 × Comments`

- **Engagement Buckets**  
  Low / Medium / High / Very High  

- **Demand Index**  
  Based on Google Trends  

- **Supply Index**  
  Posting activity per domain  

- **Interest–Activity Gap**  
  Difference between demand and engagement  

---

##  Dashboard & Analysis (Power BI)

Developed an interactive dashboard including:

### 🔹 Public Interest vs Engagement
- Scatter analysis of Google vs Reddit signals  

### 🔹 Demand–Supply Gap
- Identifies under-served domains  

### 🔹 Time Intelligence
- Daily and hourly engagement patterns  

### 🔹 Engagement Quality & Virality
- High engagement % and viral content distribution  

### 🔹 Domain Performance
- Comparative analysis across domains  

---

##  Key Insights

-  **Technology & Healthcare**  
  High search demand but lower engagement → opportunity areas  

-  **Sports & Science**  
  High engagement and strong virality  

-  **Politics & Society**  
  Discussion-driven engagement  

-  Engagement varies significantly by **time and posting behavior**  

---

##  Tech Stack

- Python (Pandas, NumPy)  
- Power BI  
- DAX  
- REST APIs (Reddit)  

---


