# E-Commerce Sales Data Transformation & Modeling (Power BI)

## Project Overview
This project is part of **Data Analytics Module 2: Power BI Assignment 1**, focusing on end-to-end data preparation, cleansing, transformation, aggregation, and relational data modeling using **Power BI** and the **Power Query Editor**[cite: 3]. The objective is to build an accurate, clean, and business-ready data model from multiple related e-commerce data files[cite: 3].

---

## Datasets Description
The project integrates three primary datasets representing order-level, product-level, and sales target information[cite: 3]:
1. **List of Orders**: Order ID, Order Date, Customer Name, City, State, Category, Amount, Profit[cite: 3].
2. **Order Details**: Order ID, Category, Sub-Category, Quantity, Amount, Profit[cite: 3].
3. **Sales Target**: Category, Month of Order Date, Target[cite: 3].

---

## Key Tasks & Implementation Steps

### 1. Data Import & Preparation
* **Data Loading**: Imported `List of Orders.csv`, `Order Details.csv`, and `Sales Target.csv` into Power BI via Power Query Editor[cite: 3].
* **Row Limiting & Data Types**: 
  * Restricted the *List of Orders* table to the first 500 rows[cite: 4].
  * Converted `Order Date` to the `Date` data type[cite: 4].
  * Changed `Amount` and `Target` columns to fixed decimal numbers[cite: 4].

### 2. Data Cleaning & Transformation
* **Text Formatting**: Cleaned and formatted the `CustomerName` column to **Proper Case** for consistent capitalization[cite: 4].
* **Custom Column Creation**:
  * **Location**: Merged `City` and `State` columns into the format `City, State`[cite: 4].
  * **Profit Margin**: Created a custom column calculated as `Profit / Amount` (expressed as a percentage)[cite: 4].
* **Conditional Logic**: Added a conditional column named `Profit Status`[cite: 4]:
  * If `Profit < 0` $\rightarrow$ `Loss`[cite: 4]
  * If `Profit = 0` $\rightarrow$ `Break-Even`[cite: 4]
  * If `Profit > 0` $\rightarrow$ `Profit`[cite: 4]
* **Data Integration**: Merged the *List of Orders* and *Order Details* tables using `Order ID` into a unified table named `Orders Data`[cite: 4].

### 3. Data Quality, Sorting & Filtering
* **Missing & Duplicate Data**: Validated all tables for missing values and duplicate rows, applying appropriate data cleaning and deduplication strategies based on business rules.
* **Sorting & Filtering**: Sorted the `Orders Data` table by `Order Date` in descending order and applied state-level filters (e.g., Tamil Nadu) for targeted regional analysis[cite: 5].

### 4. Grouping & Aggregations
Duplicated and aggregated source tables to analyze metrics:
* **Order Details Duplication**: Calculated Order ID counts, Average Profit by Category, and Total Amount by Sub-Category[cite: 5].
* **Sales Target Duplication**: Aggregated total Target by the Month of the order date[cite: 5].

### 5. Relational Data Modeling
* Established a primary relationship between **List of Orders** and **Order Details** using `Order ID`[cite: 5].
* Established a relationship between **Order Details** and **Sales Target** using `Category`[cite: 5].
* Managed active relationships within Power BI Model View to ensure model integrity and accurate cross-filtering[cite: 5].

---

## Skills & Competencies Demonstrated
* **Data Preparation & Import**: Power Query ETL workflows[cite: 6, 7].
* **Data Cleaning**: Handling data types, text formatting, and null/duplicate management[cite: 6, 7].
* **Business Logic & Custom Columns**: Conditional evaluation and metric derivation (Profit Margin, Profit Status)[cite: 6, 7].
* **Data Integration**: Table merging/joins[cite: 6, 7].
* **Data Aggregation**: Group-by operations and summarization[cite: 6, 7].
* **Data Modeling**: Star/relational schema design and active relationship management[cite: 6, 7].

---

## Project Deliverables
* **Power BI File (`.pbix`)**: Contains all imported data, Power Query steps, merged tables, and active data model relationships[cite: 5].
* **Documentation (`.pdf`)**: Includes workflow explanation and solution screenshots[cite: 5].
