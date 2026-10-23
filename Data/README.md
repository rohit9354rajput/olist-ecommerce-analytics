# Data

The raw data is not stored in this repo. Download it from Kaggle:

**Brazilian E-Commerce Public Dataset by Olist**
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

## Files used

| File | Description |
|------|-------------|
| olist_orders_dataset.csv | Order status and timestamps |
| olist_order_items_dataset.csv | Items, prices and freight per order |
| olist_order_payments_dataset.csv | Payment details |
| olist_order_reviews_dataset.csv | Review scores |
| olist_customers_dataset.csv | Customer IDs and location |
| olist_sellers_dataset.csv | Seller IDs and location |
| olist_products_dataset.csv | Product category and attributes |
| product_category_name_translation.csv | Portuguese to English category names |

(Remove any file you did not load.)

## Setup

1. Download and unzip the dataset.
2. Place the CSV files in this `data/` folder.
3. Run `notebooks/01_load_to_postgres.ipynb` to load them into PostgreSQL.

CSV files are listed in `.gitignore` and will not be committed.
