# Data Dictionary

This document describes the datasets used in the **ABC Toys Business Analysis** project.

The project combines sales, product, store, and inventory data to analyze revenue performance, profitability, store strategy, and inventory risk.

---

## 1. Dataset Summary

| Dataset | File Name | Rows | Columns | Purpose |
|---|---:|---:|---:|---|
| Sales | `sales.csv` | 829,262 | 5 | Transaction-level sales records used to measure sales volume and revenue performance |
| Products | `products.csv` | 35 | 5 | Product master data used to calculate cost, price, profit, margin, and category performance |
| Stores | `stores.csv` | 50 | 5 | Store master data used to analyze performance by city, location type, and store maturity |
| Inventory | `inventory.xlsx` | 1,593 | 3 | Store-product inventory data used to identify stockout and overstock risks |

---

## 2. Sales Dataset

**File:** `sales.csv`

| Field | Data Type | Description | Example |
|---|---|---|---|
| `Sale_ID` | Integer | Unique identifier for each sales transaction record | `1` |
| `Date` | Date | Date when the sale occurred | `2022-01-01` |
| `Store_ID` | Integer | Unique identifier of the store where the sale occurred. Used to join with the Stores dataset | `24` |
| `Product_ID` | Integer | Unique identifier of the product sold. Used to join with the Products dataset | `4` |
| `Units` | Integer | Number of units sold in the transaction | `1` |

**Analytical use:**

- Measure total sales volume.
- Track sales performance over time.
- Analyze seasonality and revenue trend.
- Combine with product price and cost to calculate revenue, profit, and profit margin.

---

## 3. Products Dataset

**File:** `products.csv`

| Field | Data Type | Description | Example |
|---|---|---|---|
| `Product_ID` | Integer | Unique identifier for each product. Used to join with Sales and Inventory datasets | `1` |
| `Product_Name` | Text | Product name | `Action Figure` |
| `Product_Category` | Text | Product category or product group | `Toys` |
| `Product_Cost` | Currency / Text | Cost of one product unit | `$9.99` |
| `Product_Price` | Currency / Text | Selling price of one product unit | `$15.99` |

**Analytical use:**

- Identify revenue and profit contribution by product and category.
- Calculate unit profit and profit margin.
- Segment products into strategic groups such as Hero / Push, Review Margin, Scale Opportunity, and Low Priority.

---

## 4. Stores Dataset

**File:** `stores.csv`

| Field | Data Type | Description | Example |
|---|---|---|---|
| `Store_ID` | Integer | Unique identifier for each store. Used to join with Sales and Inventory datasets | `1` |
| `Store_Name` | Text | Store name | `Maven Toys Guadalajara 1` |
| `Store_City` | Text | City where the store is located | `Guadalajara` |
| `Store_Location` | Text | Store location type or format, such as Residential, Downtown, Commercial, or Airport | `Residential` |
| `Store_Open_Date` | Date | Date when the store opened | `1992-09-18` |

**Analytical use:**

- Compare store performance by city and location type.
- Analyze geographic concentration of revenue.
- Evaluate whether store maturity impacts revenue performance.
- Identify high-performing store formats and locations.

---

## 5. Inventory Dataset

**File:** `inventory.xlsx`

| Field | Data Type | Description | Example |
|---|---|---|---|
| `Store_ID` | Integer | Unique identifier of the store. Used to join with Stores and Sales datasets | `1` |
| `Product_ID` | Integer | Unique identifier of the product. Used to join with Products and Sales datasets | `1` |
| `Stock_On_Hand` | Integer | Number of product units currently available in the store | `27` |

**Analytical use:**

- Identify products with stockout risk.
- Detect overstock situations.
- Compare inventory availability with sales demand.
- Support inventory reallocation and replenishment recommendations.

---

## 6. Key Relationships

| Relationship | Join Key | Purpose |
|---|---|---|
| Sales → Products | `Product_ID` | Add product name, category, cost, and price to sales records |
| Sales → Stores | `Store_ID` | Add store city, location type, and open date to sales records |
| Inventory → Products | `Product_ID` | Identify inventory status by product |
| Inventory → Stores | `Store_ID` | Identify inventory status by store and location |

---

## 7. Main Calculated Metrics

| Metric | Formula / Logic | Purpose |
|---|---|---|
| Revenue | `Units × Product_Price` | Measure sales value |
| Cost | `Units × Product_Cost` | Estimate total cost of goods sold |
| Profit | `Revenue - Cost` | Measure profit contribution |
| Profit Margin | `Profit / Revenue` | Evaluate profitability efficiency |
| Profit Contribution | `Product Profit / Total Profit` | Measure how much each product contributes to total profit |
| Store Age / Store Maturity | Difference between analysis date and `Store_Open_Date` | Analyze whether store maturity affects performance |
| Stockout | `Stock_On_Hand = 0` or inventory unavailable while demand exists | Identify lost sales risk |
| Overstock | High inventory level or Days of Inventory above threshold | Identify working capital risk |
| Lost Revenue Estimate | Average daily sales × number of days × product price | Estimate revenue loss from stockout |

---

## 8. Notes

- `Product_Cost` and `Product_Price` are stored as currency-formatted text in the original file and may need cleaning before calculation.
- `Store_Open_Date` should be converted to date format before calculating store maturity.
- Inventory analysis should be interpreted together with sales demand, because high stock is not always overstock if the product has strong sales velocity.
- Stockout and overstock thresholds can be adjusted depending on business assumptions and dashboard settings.
