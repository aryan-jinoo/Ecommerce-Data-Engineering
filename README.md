# E-Commerce Data Engineering & Analytics

An end-to-end data engineering and business intelligence project using Python, Databricks, PySpark, Delta Lake and Microsoft Power BI.

## Project Overview

This project processes the Brazilian E-Commerce Public Dataset by Olist through a Medallion Architecture. Raw CSV datasets are ingested into Databricks, cleaned and transformed, and converted into analytics-ready Gold tables. The Gold tables are then imported into Power BI for business analysis and visualization.

## Project Objectives

- Ingest multiple e-commerce datasets into Databricks.
- Implement Bronze, Silver and Gold data layers.
- Clean and transform data using PySpark.
- Create analytical tables for business reporting.
- Build an interactive Power BI dashboard.
- Maintain project code and documentation using GitHub.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Programming |
| PySpark | Data transformation |
| Databricks | Data engineering platform |
| Delta Lake | Data storage |
| SQL | Data querying |
| Power BI | Business intelligence and visualization |
| GitHub | Project hosting and documentation |

## Dataset

**Brazilian E-Commerce Public Dataset by Olist**

The project uses nine CSV files:

1. Customers
2. Geolocation
3. Order Items
4. Order Payments
5. Order Reviews
6. Orders
7. Products
8. Sellers
9. Product Category Translation

Dataset source: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

## Data Pipeline Architecture

```text
Olist CSV Datasets
        |
        v
Databricks Volume
        |
        v
BRONZE LAYER
Raw Delta Tables
        |
        v
SILVER LAYER
Cleaned and Standardized Tables
        |
        v
GOLD LAYER
Analytics-Ready Tables
        |
        v
Microsoft Power BI
        |
        v
E-Commerce Analytics Dashboard
```

## Medallion Architecture

### Bronze Layer

- Ingests nine CSV datasets.
- Stores raw data as Delta tables.
- Preserves source data for further processing.

### Silver Layer

- Cleans and standardizes data.
- Performs safe data type conversions.
- Removes duplicate records.
- Adds processing metadata.
- Creates nine Silver tables.

### Gold Layer

Creates six analytical tables:

| Gold Table | Description |
|---|---|
| gold_sales | Order-level sales analysis |
| gold_customers | Customer-level analysis |
| gold_products | Product performance |
| gold_payments | Payment type analysis |
| gold_deliveries | Delivery performance |
| gold_reviews | Review score analysis |

## Databricks Notebooks

The pipeline consists of three notebooks:

1. `01_Bronze_Ingestion`
2. `02_Silver_Transformation`
3. `03_Gold_Analytics`

Execute them in this order.

## Power BI Dashboard

The dashboard includes:

- Total Revenue
- Total Orders
- Revenue Trend
- Top 10 Product Categories
- Customer Analysis
- Delivery Status Analysis
- Payment Type Analysis
- Review Score Analysis
- Average Delivery Days

## Repository Structure

```text
Ecommerce-Data-Engineering/
│
├── notebooks/
│   ├── 01_Bronze_Ingestion.ipynb
│   ├── 02_Silver_Transformation.ipynb
│   └── 03_Gold_Analytics.ipynb
│
├── Ecommerce_Analytics_Dashboard.pbix
├── README.md
├── requirements.txt
└── .gitignore
```

## Running the Project

1. Download or clone this repository.
2. Install the Python dependencies using:

```bash
pip install -r requirements.txt
```

3. Open the Databricks workspace.
4. Upload the nine Olist CSV datasets to the required Databricks volume.
5. Import the three notebooks into Databricks.
6. Execute Bronze, Silver and Gold notebooks in sequence.
7. Import the Gold tables into Power BI to explore the analytics dashboard.

Note: The Databricks workspace, compute and data volume must be configured before running the notebooks. The current pipeline is executed through manually run notebooks.

## Project Outcomes

- Nine source datasets ingested.
- Nine Bronze Delta tables created.
- Nine Silver Delta tables created.
- Six Gold analytical tables created.
- Gold tables imported into Power BI.
- An e-commerce analytics dashboard developed.

## Future Improvements

- Automate execution using Databricks Workflows.
- Add automated data quality checks.
- Implement pipeline monitoring and logging.
- Improve dashboard interactivity.
- Add automated testing.

## Author

**Aryan**

GitHub: https://github.com/aryan-jinoo/Ecommerce-Data-Engineering

**Project:** E-Commerce Data Engineering & Analytics
