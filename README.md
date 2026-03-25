# Supply Chain Analytics Dashboard - PostgreSQL - Jupyter Notebook

## Project Overview

- This project is a complete end-to-end Supply Chain Data Analytics Dashboard designed to analyze, monitor, and optimize supply chain operations. It integrates PostgreSQL database management, Python-based data analysis, and interactive visualizations to deliver meaningful business insights.

- The system processes supply chain data such as product performance, supplier efficiency, logistics operations, and cost distribution. The objective of this project is to simulate a real-world industry use case where data-driven decisions improve operational efficiency, reduce costs, and enhance overall supply chain performance.

- This project is well-suited for roles such as Supply Chain Analyst, Data Analyst, and Business Analyst, demonstrating strong capabilities in SQL, Python, and data visualization.

## Tech Stack

- Database: PostgreSQL (Relational Database Management System)
- Analysis: Python (Pandas, NumPy)
- Visualization: Matplotlib, Seaborn, Plotly
- Environment: Jupyter Notebook
- Database Connectivity: psycopg2, SQLAlchemy

## Key Features

- Revenue analysis by product and category  
- Inventory and stock level monitoring  
- Shipping and logistics performance tracking  
- Supplier performance and defect rate analysis  
- Quality inspection and defect detection  
- Cost and profitability analysis  
- Lead time and operational delay tracking  

## Database Structure

The project uses a centralized table:

### Table: supply_chain_data

#### Columns

- product_type  
- sku  
- price  
- availability  
- number_of_products_sold  
- revenue_generated  
- customer_demographics  
- stock_levels  
- lead_times  
- order_quantities  
- shipping_times  
- shipping_carriers  
- shipping_costs  
- supplier_name  
- location  
- production_volumes  
- manufacturing_lead_time  
- manufacturing_costs  
- inspection_results  
- defect_rates  
- transportation_modes  
- routes  
- costs  

This structure captures the complete supply chain lifecycle from production to delivery.

## Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/your-username/supply-chain-dashboard.git
cd supply-chain-dashboard
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn plotly sqlalchemy psycopg2-binary
```

### 3. Setup PostgreSQL

- Install PostgreSQL  
- Create database: scm  
- Create table: supply_chain_data  
- Insert dataset into the table  

### 4. Run Jupyter Notebook

```bash
jupyter notebook
```

## Database Connection Example

```python
from sqlalchemy import create_engine

engine = create_engine('postgresql://postgres:1234@localhost:5432/scm')
```

## Data Analysis Workflow

1. Connect to PostgreSQL database  
2. Fetch data using SQL queries  
3. Load data into Pandas DataFrame  
4. Perform data cleaning and validation  
5. Generate KPIs and metrics  
6. Visualize insights using charts  

## Sample Analysis

### Total Revenue

```python
df['revenue_generated'].sum()
```

### Revenue by Product Type

```python
df.groupby('product_type')['revenue_generated'].sum()
```

### Supplier Defect Rate

```python
df.groupby('supplier_name')['defect_rates'].mean()
```

### Cost vs Revenue Analysis

```python
import matplotlib.pyplot as plt

plt.scatter(df['costs'], df['revenue_generated'])
plt.xlabel('Costs')
plt.ylabel('Revenue')
plt.title('Cost vs Revenue')
plt.show()
```

## Visualizations Included

- Bar chart for revenue by product type  
- Pie chart for shipping carrier distribution  
- Line chart for inventory trends  
- Scatter plot for cost versus revenue  
- Histogram for shipping cost distribution  

## Key Insights

- Identification of top-performing products  
- Detection of suppliers with high defect rates  
- Optimization opportunities in logistics and shipping  
- Analysis of cost-intensive routes and transportation modes  
- Identification of inventory imbalances such as overstock and stockout  

## Business Impact

This project helps organizations to:

- Improve supply chain efficiency  
- Reduce operational costs  
- Enhance supplier selection  
- Optimize inventory management  
- Enable data-driven decision-making  

## Future Enhancements

- Integration with Power BI dashboards  
- Development of a web-based dashboard  
- Real-time data integration using APIs  
- Implementation of machine learning models for demand forecasting  
- Automated reporting system  

## Author

Nagendra Arya  
Control Tower Executive I Supply Chain Analysis I Data Analysis

## Support

If you find this project useful, consider giving it a star on GitHub or contributing to its improvement.

## Contact

For collaboration or queries, feel free to connect.
