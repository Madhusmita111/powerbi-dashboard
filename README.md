::: {align="center"}
# Cross-Platform Engagement Analysis

### Reddit × Google Trends Data Analytics

**Connecting public search interest with community engagement**
:::
Overview
This project analyzes the relationship between public search interest
on Google Trends and community engagement on Reddit across domains
such as Technology, Healthcare, Sports, Science, and Politics & Society.

By bringing these two data sources together, the project explores what
people search for, how communities engage with topics, and where search
interest and Reddit activity may differ.
Questions explored
- Which domains attract the strongest Reddit engagement?
- How does public search interest compare with community activity?
- Which domains show high engagement and viral-post activity?
- How do engagement patterns vary over time?
- Where are there potential gaps between search interest and community
  engagement?
Dashboard Highlights
1. Engagement Overview
A high-level view of engagement metrics and domain performance.

2. Domain Performance
Compares engagement across domains and highlights differences in average
engagement, comments, and viral-post performance.

3. Engagement Quality and Virality
Explores engagement distribution and viral-post patterns across domains.

4. Time Intelligence
Examines daily and hourly engagement patterns to identify changes in
Reddit activity over time.

5. Public Interest vs. Community Engagement
Compares Google Trends search-interest signals with Reddit engagement to
explore where the two signals differ.

6. Interest--Activity Gap Analysis
Highlights differences between search interest and Reddit activity by
domain. These gaps are indicators for further investigation, not direct
proof of unmet demand.

Data Collection
Reddit Data
Collected 9,000+ Reddit posts using the Reddit Public API with
Python.

Fields included: - Post score (upvotes) - Comment count - Subreddit and
domain - Timestamp

The collection process included pagination handling and rate limiting.
Google Trends Data
Collected daily, domain-level search-interest data to represent public
interest over time.
Methodology
1. Data Preprocessing
- Cleaned and standardized both datasets.
- Removed duplicate and null records.
- Converted timestamps into usable date/time fields.
- Aggregated Reddit activity from post level to domain + date
  level.
- Aligned Reddit and Google Trends data using domain and date.
2. Feature Engineering
  Metric                              Definition / purpose
  Engagement Score                    Score + (2 × Comments)

  Engagement Buckets                  Groups posts into Low, Medium,
                                      High, and Very High engagement

  Demand Index                        Represents relative search interest
                                      from Google Trends

  Supply Index                        Represents posting activity by
                                      domain

  Interest--Activity Gap              Compares search-interest and
                                      engagement signals to identify
                                  potential misalignment
The Demand Index, Supply Index, and Interest--Activity Gap are
project-defined measures. Their interpretation depends on the
calculations and normalization used in the underlying model.
3. Power BI Data Modeling
Used Power Query for data preparation and built a Power BI data model
with separate fact tables and shared domain/date dimensions. Developed
DAX measures for engagement, virality, and time-based analysis.

Key Insights
- Sports showed strong average engagement and viral-post
  performance in the dashboard.
- Technology and Healthcare showed differences between search
  interest and Reddit engagement, suggesting areas for further
  analysis.
- Politics & Society showed discussion-driven engagement patterns.
- Engagement varied across domains and time periods, making
  domain-level and time-based comparisons useful.
These findings describe patterns in the collected data and should not be
interpreted as proof of causation or as a direct measure of real-world
demand.
Technology Stack
- Languages & data processing: Python, Pandas, NumPy
- Data sources / APIs: Reddit Public API, Google Trends
- BI & visualization: Power BI
- Data preparation: Power Query
- Analytics: DAX, feature engineering, time-based analysis
Skills Demonstrated
- API-based data collection
- Data cleaning and transformation
- Data aggregation and feature engineering
- Dimensional data modeling
- KPI development with DAX
- Cross-platform trend analysis
- Interactive dashboard design
- Analytical insight communication
Repository Image Files
The screenshots are referenced using relative paths from the
repository root. Keep these image files in the same folder as
README.md:
powerbi-dashboard/
├── README.md
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
If you move the images into a folder such as screenshots/, update each
image link to include that folder, for example
![Engagement overview](screenshots/engagement-overview.png).
Conclusion
This project combines public search-interest data and Reddit community
activity in a shared analytical framework. By preparing and aligning
data from two platforms, creating domain-level metrics, and building an
interactive Power BI dashboard, it supports structured exploration of
engagement, virality, and changes in audience interest.
