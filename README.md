::: {align="center"}
# Cross-Platform Engagement Analysis

### Reddit × Google Trends Data Analytics

**Connecting public search interest with community engagement**

[Overview](#overview) · [Dashboard](#dashboard-highlights) ·
[Methodology](#methodology) · [Key Insights](#key-insights) · [Tech
Stack](#technology-stack)
:::

![Project banner](assets/project-banner.png)

## Overview

This project explores the relationship between **public search interest
on Google Trends** and **community engagement on Reddit** across
multiple domains, including Technology, Healthcare, Sports, Science, and
Politics & Society.

The analysis brings two signals together to investigate what people
search for, how communities respond, and where search interest and
Reddit activity may not align.

### Questions explored

-   Which domains attract the strongest Reddit engagement?
-   How does public search interest compare with community activity?
-   Which domains show high engagement or viral-post activity?
-   How do engagement patterns change over time?
-   Where might there be gaps between search interest and community
    engagement?

## Dashboard Highlights

### 1. Engagement Overview

A high-level view of the dataset, total engagement, average engagement
per post, and top-performing domains.

![Engagement overview](assets/engagement-overview.png)

### 2. Domain Performance Analysis

Compares engagement across domains and highlights differences in average
engagement, comments, and viral-post performance.

![Domain performance](assets/domain-performance.png)

### 3. Engagement Quality and Virality

Explores engagement distribution, viral-post patterns, and how
engagement quality varies by domain.

![Engagement quality and
virality](assets/engagement-quality-virality.png)

![Virality breakdown](assets/virality-breakdown.png)

### 4. Time Intelligence

Examines daily and hourly engagement patterns to identify when Reddit
activity changes.

![Time intelligence](assets/time-intelligence.png)

![Time and domain comparison](assets/time-domain-comparison.png)

### 5. Public Interest vs. Community Engagement

Compares Google Trends search-interest signals with Reddit engagement to
identify domains where the two signals differ.

![Public interest versus
engagement](assets/public-interest-vs-engagement.png)

### 6. Interest--Activity Gap Analysis

Highlights differences between search interest and Reddit activity at
the domain level. These gaps can help identify areas for further
investigation rather than serving as a direct measure of unmet demand.

![Interest activity gap](assets/interest-activity-gap.png)

## Data Collection

### Reddit

Collected **9,000+ Reddit posts** using the Reddit Public API with
Python.

Fields included: - Post score (upvotes) - Comment count - Subreddit and
domain - Timestamp

The collection process included pagination handling and rate limiting.

### Google Trends

Collected daily, domain-level search-interest data to represent public
interest over time.

## Methodology

### 1. Data preprocessing

-   Cleaned and standardized both datasets.
-   Removed duplicate and null records.
-   Converted timestamps into usable date/time fields.
-   Aggregated Reddit activity from post level to **domain + date**
    level.
-   Aligned Reddit and Google Trends data using **domain and date**.

### 2. Feature engineering

  -----------------------------------------------------------------------
  Metric                              Definition / purpose
  ----------------------------------- -----------------------------------
  Engagement Score                    `Score + (2 × Comments)`

  Engagement Buckets                  Groups posts into Low, Medium,
                                      High, and Very High engagement

  Demand Index                        Represents relative search interest
                                      from Google Trends

  Supply Index                        Represents posting activity by
                                      domain

  Interest--Activity Gap              Compares search-interest and
                                      engagement signals to identify
                                      potential misalignment
  -----------------------------------------------------------------------

*Note: The Demand Index, Supply Index, and Interest--Activity Gap are
project-defined analytical measures. Their interpretation depends on the
normalization and calculation used in the underlying model.*

### 3. Data modeling and dashboarding

Built an interactive Power BI dashboard with separate fact tables and
shared domain/date dimensions. Used Power Query for data preparation and
DAX for analytical measures and KPIs.

![Power BI data model](assets/power-bi-data-model.png)

## Key Insights

-   **Sports** showed strong average engagement and viral-post
    performance in the dashboard.
-   **Technology and Healthcare** showed areas where search interest and
    Reddit engagement differed, warranting further investigation.
-   **Politics & Society** showed discussion-driven engagement patterns.
-   Engagement varied across domains and time periods, making time-based
    and domain-level comparisons useful.

The findings describe patterns in the collected data and should not be
interpreted as proof of causation or as a direct measure of real-world
demand.

## Technology Stack

-   **Languages & data processing:** Python, Pandas, NumPy
-   **Data source / APIs:** Reddit Public API, Google Trends
-   **BI & visualization:** Power BI
-   **Data preparation:** Power Query
-   **Analytics:** DAX, feature engineering, time-based analysis

## Skills Demonstrated

-   API-based data collection
-   Data cleaning and transformation
-   Data aggregation and feature engineering
-   Dimensional data modeling
-   KPI development with DAX
-   Cross-platform trend analysis
-   Interactive dashboard design
-   Analytical insight communication

## Repository Structure

``` text
cross-platform-engagement-analysis/
├── README.md
└── assets/
    ├── project-banner.png
    ├── engagement-overview.png
    ├── domain-performance.png
    ├── engagement-quality-virality.png
    ├── virality-breakdown.png
    ├── time-intelligence.png
    ├── public-interest-vs-engagement.png
    ├── interest-activity-gap.png
    ├── time-domain-comparison.png
    └── power-bi-data-model.png
```

## Conclusion

This project combines public search-interest data and Reddit community
activity in a single analytical framework. By preparing and aligning
data from two platforms, creating domain-level metrics, and building an
interactive Power BI dashboard, it supports structured exploration of
engagement, virality, and changes in audience interest.

------------------------------------------------------------------------

::: {align="center"}
**Cross-Platform Engagement Analysis \| Reddit × Google Trends**
:::
