# SALES-CUSTOMER-RETENTION-ANALYSIS
This analysis evaluates sales performance, customer loyalty, and operational efficiency across 7  interconnected data tables
📋 Project Overview
This project performs an end-to-end sales and customer retention analysis using a relational SQLite database spanning 7 interconnected tables. The goal is to surface actionable business insights around customer loyalty, product-level return rates, regional engagement, and pricing strategy.

🔍 Key Findings
MetricValueRepeat Users15,089One-Time Users2,327Retention Rate86.6%Top Product CategoryAccessories (33,607 orders)Accessories Return Rate3.36%Highest-Volume RegionAustralia (12,409 orders)Highest Repeat-Purchase RegionCanada (11.61%)

🗂️ Data & Methodology
The dataset consists of 7 relational tables queried via SQLite. Before analysis, a rigorous data cleaning pipeline was applied:

Null & Invalid Key Handling — Validated all foreign keys; removed invalid ("botched") customer entries to prevent downstream mapping errors.
Format Standardization — Converted text-based date strings into standardized SQLite-compatible formats for accurate time-series calculations.
Deduplication — Verified uniqueness across OrderNumber fields to prevent artificially inflated volume metrics.


📈 Analysis Sections
1. User Behavior — The Retention Leaderboard
With an 86.6% repeat purchase rate, the business is driven by strong brand loyalty. Only 13.4% of customers are one-time buyers, significantly reducing long-term customer acquisition costs.
2. Product Sales Performance
Accessories dominate order volume at 33,607 orders — more than Bikes (13,929) and Clothing (8,510) combined — while maintaining a stable return rate of 3.36%.
CategoryOrdersReturn RateAccessories33,6073.36%Bikes13,9293.08%Clothing8,5103.16%

⚠️ Note: The Components category (14 sub-categories) recorded zero retail sales — flagged for inventory/data audit.

3. Regional Activity Distribution
Australia leads in total orders, but Canada stands out with a disproportionately high repeat purchase rate.
RegionTotal OrdersRepeat RateReturn RateAustralia12,4091.65%3.26%US Southwest11,4630.12%3.16%US Northwest8,2670.17%3.27%Canada6,87511.61%3.46%United Kingdom6,4231.26%3.18%Germany5,2891.00%3.08%France5,2391.95%3.55%
4. The Price Effect on Sales
Return rates vary by price tier, with medium-tier products posing the greatest dollar-value risk.
Price TierOrdersReturn RateLow (< $50)66,0411.90%High (> $500)13,9293.08%Medium ($50–$500)4,2043.35%

💡 Strategic Recommendations

Loyalty Tier Program — Reward the 15,000+ repeat buyers with a structured loyalty program to prevent churn to competitors.
Medium-Tier Quality Audit — Investigate the 3.35% return rate on $50–$500 items; the dollar-value loss per return is substantially higher than low-tier returns.
One-Time User Conversion — Converting just ~500 of the 2,327 one-time users would increase the monthly active customer base by approximately 4%.
Components Inventory Audit — Determine whether the Components category (14 sub-categories, zero sales) represents internal-only stock, a listing error, or a data-tracking gap.


🛠️ Tech Stack

Database: SQLite
Language: SQL
Visualization: Custom charts (PowerPoint/presentation layer)

