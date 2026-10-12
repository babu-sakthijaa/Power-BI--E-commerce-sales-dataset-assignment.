# 📊 E-commerce Sales Data Transformation & Data Modeling using Power BI

## 📌 Project Overview

This project focuses on preparing, cleaning, transforming, and modeling an E-commerce sales dataset using **Microsoft Power BI and Power Query Editor**.

The objective is to convert raw sales data into a structured and reliable data model by applying data cleansing techniques, calculated columns, data merging, aggregation, and relationship management.

This project is part of my learning journey as an **Aspiring Data Analyst**, where I am developing practical skills in data preparation, data integration, and data modeling.

## 🎯 Project Objectives

* Import multiple CSV datasets into Power BI.
* Transform and clean data using Power Query Editor.
* Standardize customer names and correct data types.
* Create calculated and conditional columns.
* Merge related datasets using Order ID.
* Identify and handle missing values and duplicate records.
* Sort and filter sales data for analysis.
* Perform grouping and aggregation operations.
* Establish and validate relationships between tables.

## 🛠️ Tools & Technologies

* **Microsoft Power BI** — Data modeling and data preparation
* **Power Query Editor** — Data transformation and cleansing
* **CSV** — Source data format
* **GitHub** — Project documentation and portfolio development

## 📂 Dataset Description

The project uses three datasets representing order information, product details, and sales targets.

### 1. List of Orders

Contains customer and order-level information.

| Column        | Description                  |
| ------------- | ---------------------------- |
| Order ID      | Unique order identifier      |
| Order Date    | Date the order was placed    |
| Customer Name | Customer's name              |
| City          | Customer's city              |
| State         | Customer's state             |
| Category      | Product category             |
| Amount        | Order amount                 |
| Profit        | Profit earned from the order |

### 2. Order Details

Contains product-level information associated with orders.

| Column       | Description          |
| ------------ | -------------------- |
| Order ID     | Order identifier     |
| Category     | Product category     |
| Sub-Category | Product sub-category |
| Quantity     | Quantity ordered     |
| Amount       | Sales amount         |
| Profit       | Profit earned        |

### 3. Sales Target

Contains category-wise monthly sales targets.

| Column              | Description         |
| ------------------- | ------------------- |
| Category            | Product category    |
| Month of Order Date | Target month        |
| Target              | Sales target amount |

## 🔄 Data Transformation & Preparation

### 1. Data Import and Data Types

* Imported all three CSV files into Power BI.
* Opened the datasets in Power Query Editor.
* Limited the List of Orders table to the first 500 rows.
* Converted Order Date to the Date data type.
* Changed Amount and Target to Fixed Decimal Number where applicable.

### 2. Text Standardization

* Converted customer names to Proper Case.
* Standardized text formatting to improve data consistency.

### 3. Custom Column Creation

**Location**

Combined City and State into a new column named `Location`.

Example: `Chennai, Tamil Nadu`

**Profit Margin**

Created a custom column named `Profit Margin` using:

`Profit Margin = Profit / Amount`

The result is expressed as a percentage. Zero or null Amount values should be handled appropriately to avoid invalid calculations.

### 4. Conditional Column

Created a column named `Profit Status` based on profit values.

| Condition  | Profit Status |
| ---------- | ------------- |
| Profit < 0 | Loss          |
| Profit = 0 | Break-Even    |
| Profit > 0 | Profit        |

### 5. Data Merging

Merged the List of Orders and Order Details tables using `Order ID`.

The merged query output was named `Orders Data`.

This integrates order-level information with product-level details for further analysis.

### 6. Missing Values and Duplicate Handling

* Identified missing values across all three datasets.
* Evaluated whether missing values should be replaced, retained, or removed.
* Considered the business meaning of null values before applying changes.
* Identified duplicate records and considered whether they represented genuine duplicates or valid multiple product lines within an order.

### 7. Sorting and Filtering

* Sorted Orders Data by Order Date in descending order.
* Applied a State filter to analyze orders from Tamil Nadu.

## 📈 Data Grouping & Aggregation

### Order Details Aggregation

Duplicated the Order Details query and performed the following operations:

* **Count of Order ID:** Counted order identifier occurrences.
* **Average Profit by Category:** Calculated average profit for each product category.
* **Total Amount by Sub-Category:** Summarized sales amounts by sub-category.

### Sales Target Aggregation

Duplicated the Sales Target query and grouped the data by month to calculate the total sales target for each month.

These aggregations help organize sales information into meaningful summaries for business analysis.

## 🧩 Data Modeling & Relationships

Established relationships between the datasets using Power BI's Manage Relationships feature.

| Table 1        | Table 2       | Relationship Key |
| -------------- | ------------- | ---------------- |
| List of Orders | Order Details | Order ID         |
| Order Details  | Sales Target  | Category         |

Validated that the relationships were active and correctly configured.

**Data modeling objective:** Maintain consistent connections between order records, product details, and sales targets while supporting reliable analysis.

The appropriate cardinality and filter direction should be validated against the actual data, especially where Order ID or Category appears multiple times.

## 📁 Project Structure

```text
Ecommerce-Sales-PowerBI/
│
├── README.md
├── Data Transformation & Data Modeling.pbix
├── PowerBI Assignment1 - Querying Data.pdf
├── List of Orders.csv
├── Order Details.csv
├── Sales Target.csv
└── Screenshots/
    ├── power-query-transformations.png
    ├── data-cleaning.png
    ├── aggregation-results.png
    └── data-model-relationships.png
```

*Note: The folder structure above is a suggested organization. Include only files and screenshots that you actually upload to your repository.*

## 📚 Key Skills Demonstrated

* Data Import and Preparation
* Data Cleaning and Validation
* Power Query Transformations
* Data Type Conversion
* Custom and Conditional Columns
* Data Merging and Integration
* Missing Value and Duplicate Handling
* Sorting and Filtering
* Grouping and Aggregation
* Relationship Management
* Data Modeling Fundamentals
* GitHub Project Documentation

## 💡 Business Value

The prepared data model provides a foundation for:

* Understanding sales and profitability across product categories.
* Identifying loss-making and break-even orders.
* Comparing sales performance across locations.
* Analyzing product sub-category sales.
* Organizing monthly sales targets for comparison with sales data.

These are potential analytical uses of the prepared dataset; actual business findings would require further analysis of the data.

## 🚀 Learning Outcomes

Through this project, I aim to strengthen my practical understanding of Power BI, Power Query Editor, data quality management, and relational data modeling.

This project represents one step in my journey toward becoming a Data Analyst and building a practical portfolio of data analytics projects.

## 👨‍💻 About Me

I am an **Aspiring Data Analyst** interested in learning how to transform raw data into structured information that supports business decision-making.

I am continuously developing my skills in data analysis, data cleaning, data modeling, and business intelligence.

**My portfolio goal:** Build practical projects that demonstrate my analytical thinking, technical skills, and continuous learning.

---

⭐ If you find this project useful, feel free to explore the repository and share feedback.
