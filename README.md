# FoodHub Order Analysis

Exploratory data analysis on 1,898 food delivery orders to surface operational bottlenecks, customer behavior patterns, and revenue opportunities for a NYC-based food delivery platform.

## Business Problem
FoodHub needed to understand where orders were slowing down, which cuisines and restaurants were driving volume, and how to increase post-delivery rating capture rates — over 38% of orders had no rating recorded.

## Dataset
- `foodhub_order.csv` — 1,898 rows × 9 columns
- Key columns: `order_id`, `customer_id`, `restaurant_name`, `cuisine_type`, `cost_of_the_order`, `day_of_the_week`, `rating`, `food_preparation_time`, `delivery_time`

## Approach
1. Data ingestion and sanity checks — no duplicates; `'Not given'` ratings converted to NaN
2. Univariate analysis — distributions of cost, prep time, delivery time, cuisine type
3. Bivariate and multivariate analysis — weekend vs weekday patterns, cost vs prep time correlations
4. Business-focused aggregations — top restaurants by volume, high-commission order identification, promotional eligibility

## Key Findings
- **Prep time:** Min 20 min / Avg 27.4 min / Max 35 min — low variance overall, but restaurants above the mean are SLA candidates
- **Ratings gap:** 736 of 1,898 orders (38.8%) have no rating — a significant feedback blind spot
- **Weekend demand:** Order volume and cuisine mix shift meaningfully on weekends, signalling staffing and promotional opportunities
- **Top 3 customers** by order volume are identifiable and eligible for loyalty incentives
- **Revenue model:** Platform charges 25% on orders >$20 and 15% on orders >$5; net revenue calculated across all 1,898 orders

## Recommendations
- Audit restaurants with avg prep time >30 min to reduce tail latency
- Add in-app rating nudges (e.g., coupon on next order) to raise the 61.2% rating completion rate
- Pre-position more delivery partners during weekend peaks; run targeted cuisine promotions

## Technologies
Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## Code
Notebook: [`Chinmay_Learner_Notebook_Full_Code.ipynb`](Chinmay_Learner_Notebook_Full_Code.ipynb)

---
*Author: Chinmay Rozekar*
