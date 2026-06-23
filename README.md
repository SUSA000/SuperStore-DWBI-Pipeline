# 🛒 SuperStore Retail End-to-End DWBI Pipeline

## 📌 Project Overview
This project demonstrates a complete Data Warehousing and Business Intelligence (DWBI) solution for a retail organization[cite: 1]. It transforms raw transactional data into a structured format for high-performance analytical processing (OLAP) and business intelligence reporting[cite: 2].

## 📂 Repository Structure
* **`Data_Sources/`**: Contains the raw operational datasets (CSV/Excel) utilized for integration[cite: 1].
* **`Docs/`**: Architectural documentation, ETL logic explanations, and comprehensive project reports.
* **`Excel_OLAP/`**: Pivot tables and OLAP analysis connected directly to the SSAS cube for interactive drill-down and slicing operations[cite: 2].
* **`PowerBI_Dashboard/`**: Interactive dashboard utilizing a Live Connection to the SSAS cube, featuring cascading slicers and hierarchical drill-throughs[cite: 2].
* **`SSAS_Cube/SuperStore_SSAS/`**: SQL Server Analysis Services (SSAS) Multidimensional project files containing the OLAP cube, dimensions, and hierarchical structures[cite: 2].
* **`SSIS_ETL/`**: SQL Server Integration Services (SSIS) packages managing data extraction, staging, and data warehouse loading[cite: 1].

## ⚙️ Core Technical Phases

### Phase 1: ETL Pipeline & Data Modeling (SSIS)
* Extracts data from a normalized SQL Server OLTP database and external flat files (CSV) into a staging area[cite: 1].
* Implements a Star Schema with a central Accumulating Snapshot fact table (`FactSales`)[cite: 1].
* Handles Slowly Changing Dimensions (SCD Type 2) to accurately track historical demographic changes in customer addresses[cite: 1].
* Calculates total transaction processing time (`txn_process_time_hours`) dynamically within the ETL pipeline[cite: 1].

### Phase 2: SSAS Multidimensional Cube & OLAP
* Features custom user hierarchies such as Location_Hierarchy (Country -> State -> City)[cite: 2].
* Features custom temporal hierarchies such as Order_Date_Hierarchy (Year -> Month)[cite: 2].
* Successfully supports interactive OLAP operations in Excel, including Drill-down, Slice, Dice, and Pivot functionalities[cite: 2].

### Phase 3: Power BI Visualization
* Includes interactive matrix visuals utilizing Data Bars for conditional formatting[cite: 2].
* Implements cascading slicers allowing users to dynamically filter cities based on selected countries[cite: 2].
* Features hierarchical Drill-Down reporting for temporal data exploration[cite: 2].

## 🛠️ Tools & Technologies
* **Database**: SQL Server (SSMS)
* **ETL**: SQL Server Integration Services (SSIS)
* **OLAP**: SQL Server Analysis Services (SSAS)
* **Visualization**: Power BI, Microsoft Excel

---
**Author**: Sushan Tharuka  
*Data Science Undergraduate*
