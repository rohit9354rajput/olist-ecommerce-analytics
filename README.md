# Olist E-Commerce Analytics: RFM, Retention, GMV and Seller Performance

End-to-end analysis of the Brazilian E-Commerce Public Dataset by Olist
(~100K orders, 2016-2018) using Python and PostgreSQL.

## Workflow
Kaggle download → load into PostgreSQL (Python) → analysis in Python via SQLAlchemy `engine.connect()`

## Business Questions
1. How many customers come back, and who are the high-value customers at risk?
2. How does retention behave across monthly cohorts?
3. Which categories and sellers drive GMV?
4. How does delivery speed affect review scores?

## Key Findings
**Customers (RFM and Retention)**
- Only ~3% of customers ordered more than once.
- Less than 1% of any cohort orders again after 1, 3 or 6 months.
- "At risk (high value)" is 14.7% of customers but 28.8% of revenue.
- Monthly revenue stabilised at ~840K-980K from March 2018.

**Marketplace (GMV, Sellers, Delivery)**
- Top 5 categories drive ~40% of GMV (delivered orders only).
- Top 20% of sellers generate 82.3% of revenue.
- Delivery in 1-7 days averages 4.42 stars; 60+ days averages 2.0.

## Recommendations
1. Reactivate the high-value at-risk segment.
2. Protect top categories and top-tier sellers with strict health metrics.
3. Treat delivery speed as a growth lever.
4. Trigger offers within 30 days of the first purchase.

## Limitations
- Descriptive analysis only, not causal or predictive.
- RFM segment thresholds are my own rules and should be tuned.
- First and last months of data are incomplete.
- Revenue excludes freight.

## Visuals
![RFM](images/rfm_segmentation.png)
![Cohorts](images/cohort_retention_analysis.png)
![Delivery](images/delivery_reviews.png)
![Sellers](images/seller_health.png)

## How to Run
1. Download the dataset: [Kaggle link]
2. Put the CSVs in `data/`
3. `pip install -r requirements.txt`
4. Copy `.env.example` to `.env` and add your PostgreSQL credentials
5. Run the notebooks in order

## Author
Tanay Gandhi | [tanay.website]
