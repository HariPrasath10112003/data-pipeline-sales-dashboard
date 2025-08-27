#  Azure Data Pipeline with Power BI Dashboard

##  Project Story
This project demonstrates how I built an **end-to-end data pipeline** using **Azure Data Factory, Azure SQL Database, and Power BI**.  
The goal was to take raw **sales CSV data**, process it through a modern data pipeline, and finally visualize meaningful business insights in Power BI dashboards.

---

##  Project Flow
1. **Source Data (CSV)**
   - A sales dataset (CSV file) containing `Date, StoreID, ProductID, Quantity, SalesAmount`.

2. **Azure Blob Storage**
   - Raw sales CSV file uploaded into a Blob container (`salesdata`).

3. **Azure Data Factory (ADF)**
   - Created a **Copy Data Activity** pipeline:
     - **Source**: Blob Storage (CSV file).  
     - **Sink**: Azure SQL Database staging table.  
   - Added an **Event-based Trigger** so whenever a new file is uploaded, the pipeline runs automatically.

4. **Azure SQL Database**
   - Data copied into a **SalesStaging** table.  
   - This staging table holds all sales transactions for analysis.

5. **Power BI**
   - Connected Power BI directly to Azure SQL Database.  
   - Performed **transformations** in Power Query (filtering, cleaning).  
   - Built interactive **dashboards**:
     -  Sales Trend (Line Chart)  
     -  Sales by Store (Bar Chart)  
     -  Top 5 Products (Table)  
     -  Monthly Revenue Summary  



