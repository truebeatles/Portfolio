# Portfolio

Repositório dos Power BIs.

This project consists of an end-to-end Business Intelligence solution, transforming raw, disorganized retail data into a high-performance analytical dashboard. The project covers every stage of the data lifecycle: **ETL, Data Modeling, DAX Intelligence, and Data Visualization.**

## 🎯 Business Challenge

The primary goal was to clean and consolidate sales, customer, and product data from multiple sources, overcoming issues such as:

- Fragmented customer databases.
    
- Poorly formatted date/period columns.
    
- Inconsistent naming conventions and data entry errors.
    

## 🛠️ Technical Implementation

### 1. Data Transformation (ETL)

Using **Power Query (M language)**, I performed advanced data cleaning:

- **Unpivoting:** Transformed 12 monthly period columns into a normalized "Value" and "Period" structure for time-series analysis.
    
- **Data Sanitization:** Fixed inconsistent geographical and shipping data (e.g., standardizing "US/us" to "United States").
    
- **String Manipulation:** Cleaned `Customer_ID` keys by removing metadata suffixes via delimiter splitting.
    
- **Surrogate Keys:** Implemented **Surrogate Keys (SK)** using index columns to decouple the model from source system business keys, ensuring better referential integrity and performance.
    

### 2. Data Modeling (Star Schema)

The model follows the **Star Schema** best practices to optimize the VertiPaq engine performance:

- **Fact Table:** `Sales` (normalized and slimmed down).
    
- **Dimension Tables:** `Customers`, `Products`, and `Geography`.
    
- **D_Calendar:** Developed a dedicated Calendar Table to enable **Time Intelligence** functions, ensuring no gaps in date-based analysis.
    

### 3. DAX Intelligence

Advanced measures were created to provide deep business insights:

- **Time Intelligence:** `Value YoY %` using `CALCULATE` and `SAMEPERIODLASTYEAR`.
    
- **Pareto Analysis:** Implemented a `Running Total` measure to identify the "Vital Few" products/regions contributing to the majority of revenue.
    
- **Dynamic Aggregations:** Robust measures using `DIVIDE` and `FILTER` to ensure error-free calculations.
    

## 📈 Final Deliverables

- **Executive Summary:** Overview of total sales and growth trends.
    
- **Operational View:** Detailed performance by Category and Region.
    
- **Interactive Features:** Drill-downs and Tooltips for granular data exploration.
    

---

### 💡 Key Takeaway

By applying **Surrogate Keys** and a **Dedicated Calendar Table**, the model is not just a report, but a scalable **Data Asset** designed for performance and reliability.

![[Pasted image 20260206205748.png]]


![[Pasted image 20260206205819.png]]

