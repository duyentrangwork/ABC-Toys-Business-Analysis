# ABC Toys Business Analysis

## 1. Project Overview

**ABC Toys Business Analysis** is a business intelligence and data visualization project that analyzes the performance of ABC Toys, a toy retail chain in Mexico.

The project focuses on understanding business performance across revenue, profit, product portfolio, store strategy, and inventory health. The final goal is to identify where the business is losing money and provide actionable recommendations to support more sustainable and profitable growth.

The analysis was built in **Tableau** and presented as a business story from executive overview to product profitability, store location strategy, inventory diagnosis, and final recommendations.

---

## 2. Business Problem

ABC Toys showed strong revenue growth, but revenue growth alone does not fully reflect business health.

The analysis focuses on answering the key business question:

> **Where is ABC Toys losing money and where should the business focus to grow more profitably?**

Key issues explored in this project include:

* Revenue growth was not fully translating into profit growth.
* Some high-revenue products had weak profit margins.
* Store performance varied significantly by location and store type.
* Inventory was not fully aligned with demand, creating both stockout and overstock risks.
* The business needed clearer prioritization across products, stores, and inventory actions.

---

## 3. Project Objectives

The main objectives of this project are to:

* Analyze overall business performance through revenue, profit, profit margin, and sales volume.
* Identify key product categories and products that drive revenue and profit.
* Diagnose product-level profitability issues.
* Evaluate store performance by location, store type, and store maturity.
* Assess inventory risks, including stockout and overstock.
* Provide actionable recommendations for profitable growth and inventory optimization.

---

## 4. Tools Used

| Tool               | Purpose                                                         |
| ------------------ | --------------------------------------------------------------- |
| Tableau            | Dashboard development, visualization, and business storytelling |
| Excel              | Data preparation and initial data checking                      |
| Data Visualization | Trend analysis, ranking, comparison, and segmentation           |
| Business Analysis  | Insight generation and strategic recommendation                 |

---

## 5. Dataset Overview

The project uses four main datasets related to ABC Toys' business operations.

| Dataset   | File             | Key Information                                             | Analytical Role                                        |
| --------- | ---------------- | ----------------------------------------------------------- | ------------------------------------------------------ |
| Sales     | `sales.csv`      | Sales revenue, quantity, date, store, product               | Measure revenue performance and sales trend            |
| Products  | `products.csv`   | Product name, category, price, cost                         | Analyze product profitability and category performance |
| Stores    | `stores.csv`     | Store type, city, opening date / maturity                   | Compare store performance by format and location       |
| Inventory | `inventory.xlsx` | Stock quantity, inventory status, store-product combination | Detect stockout, overstock, and inventory imbalance    |

These datasets were connected and analyzed to provide a complete view of business performance across products, stores, and inventory.

---

## 6. Data Workflow

The project followed these main steps:

1. **Data Understanding**
   Reviewed the available sales, product, store, and inventory datasets to understand the business context and available fields.

2. **Data Preparation**
   Cleaned and connected datasets to support analysis across multiple business dimensions.

3. **Metric Creation**
   Created key metrics such as total revenue, profit, profit margin, product contribution, store performance, stockout risk, and overstock status.

4. **Dashboard Development**
   Built Tableau dashboards to analyze executive performance, product profitability, store strategy, and inventory health.

5. **Insight Generation**
   Interpreted dashboard results to identify business issues, performance gaps, and growth opportunities.

6. **Recommendation Development**
   Proposed strategic actions to improve profitability, store performance, and inventory efficiency.

---

## 7. Analysis Framework

The analysis was structured into four main layers:

### 1. Executive Overview

Provides a high-level view of ABC Toys' business performance, including revenue, profit, profit margin, sales quantity, and inventory status.

### 2. Product Profitability Diagnosis

Analyzes product and category performance to identify:

* High-revenue products
* High-profit products
* Low-margin products
* Products that require pricing, cost, or promotion review

### 3. Store Location Strategy

Examines whether store performance is mainly driven by:

* Store maturity
* Store type
* City performance
* Geographic concentration
* Local purchasing power

### 4. Inventory Health Analysis

Evaluates inventory risks and compares the business impact of:

* Stockout
* Overstock
* Inventory imbalance across stores and products

---

## 8. Key Insights

### Insight 1: Revenue increased, but profitability needs attention

ABC Toys achieved strong revenue growth, especially in 2023. However, profit margin showed signs of decline, indicating that revenue growth did not fully translate into efficient profit growth.

This suggests that the business should not only focus on increasing sales volume, but also monitor profit margin and product-level profitability.

---

### Insight 2: High revenue does not always mean high profitability

Some products generated strong revenue but had weaker profit efficiency. This means that high-selling products are not always the best products for profitable growth.

Products with high revenue but low margin should be reviewed in terms of:

* Pricing strategy
* Cost structure
* Promotion intensity
* Discount dependency

---

### Insight 3: Product investment should be prioritized by both revenue and margin

Products were grouped into four strategic segments:

| Segment           | Meaning                   | Business Action                      |
| ----------------- | ------------------------- | ------------------------------------ |
| Hero / Push       | High revenue, high margin | Prioritize and scale                 |
| Review Margin     | High revenue, low margin  | Review pricing, cost, or promotion   |
| Scale Opportunity | Low revenue, high margin  | Test growth opportunities            |
| Low Priority      | Low revenue, low margin   | Reduce investment or monitor closely |

This segmentation helps ABC Toys avoid investing equally across all products and focus resources on products with stronger business potential.

---

### Insight 4: Store performance is more location-driven than age-driven

Store age alone does not explain store performance. Some newer stores performed well, while some older stores did not necessarily generate stronger revenue.

The analysis suggests that store performance is more influenced by location, store type, and local purchasing power than by store maturity alone.

---

### Insight 5: Inventory issues create a double business loss

ABC Toys faces both stockout and overstock issues.

* **Stockout** leads to missed sales opportunities and direct revenue loss.
* **Overstock** locks working capital and creates inventory inefficiency.

Inventory decisions should therefore balance demand, replenishment priority, and product movement speed.

---

## 9. Strategic Recommendations

### 1. Optimize product portfolio

ABC Toys should prioritize products that contribute strongly to both revenue and profit.

Recommended actions:

* Push high-margin profit hero products.
* Review pricing and promotion for high-revenue but low-margin products.
* Scale selected high-margin products with growth potential.
* Reduce investment in low-priority products if performance does not improve.

---

### 2. Refine store expansion strategy

Store investment should be based on location quality and purchasing power rather than store age alone.

Recommended actions:

* Focus expansion on cities with strong sales potential.
* Maintain Downtown as a stable revenue base.
* Expand Airport stores selectively because they show strong performance but higher volatility.
* Monitor store formats by city to identify the best location-format combinations.

---

### 3. Improve inventory allocation

Inventory should be rebalanced to reduce both stockout and overstock risks.

Recommended actions:

* Reallocate products between stores before placing new orders.
* Prioritize replenishment for products with the highest lost revenue.
* Review inventory policy for categories with repeated stockout risks.
* Clear or redistribute slow-moving products to reduce overstock.

---

## 10. Interactive Dashboard

View the interactive Tableau dashboard here:

[Open Tableau Public Dashboard](https://public.tableau.com/app/profile/trang.nguyen8600/viz/ABC_Toys_Business_Analysis/Story)

---

## 11. Project Files

| File                                                                                                                          | Description                             |
| ----------------------------------------------------------------------------------------------------------------------------- | --------------------------------------- |
| [Interactive Tableau Dashboard](https://public.tableau.com/app/profile/trang.nguyen8600/viz/ABC_Toys_Business_Analysis/Story) | Interactive dashboard on Tableau Public |
| [Tableau Workbook](dashboard/ABC_Toys_Business_Analysis.twbx)                                                                 | Tableau packaged workbook               |
| [Final Report](reports/ABC_Toys_Business_Analysis.pdf)                                                                        | Final business analysis report          |
| [Data Dictionary](data_dictionary.md)                                                                                         | Explanation of datasets and key fields  |
| [Visuals](visuals/)                                                                                                           | Dashboard images     |

---

## 12. Dashboard & Report Preview

### Executive Overview

![Executive Overview](visuals/Executive%20Overview.png)

### Portfolio Diagnosis

![Portfolio Diagnosis](visuals/Portfolio%20Diagonosis.png)

### Portfolio Strategy

![Portfolio Strategy](visuals/Portfolio%20Strategy.png)

### Store Location Strategy

![Store Location Strategy](visuals/Store%20Loction%20Strategy.png)

### Store Maturity & Geographic Performance

![Store Maturity and Geographic Performance](visuals/Store%20Maturity%20%26%20Geographic%20Performance.png)

### Inventory Health

![Inventory Health](visuals/Inventory%20Health.png)

### Stockout Analysis

![Stockout Analysis](visuals/Stockout%20Analysis.png)

---

## 13. Repository Structure

```text
ABC-Toys-Business-Analysis/
│
├── README.md
│
├── dashboard/
│   └── ABC_Toys_Business_Analysis.twbx
│
├── data/
│   ├── inventory.xlsx
│   ├── products.csv
│   ├── sales.csv
│   └── stores.csv
│
├── reports/
│   └── ABC_Toys_Business_Analysis.pdf
│
├── visuals/
│   ├── Executive Overview.png
│   ├── Inventory Health.png
│   ├── Portfolio Diagonosis.png
│   ├── Portfolio Strategy.png
│   ├── Stockout Analysis.png
│   ├── Store Loction Strategy.png
│   └── Store Maturity & Geographic P.png
│
└── data_dictionary.md
```

---

## 14. Project Outcome

This project demonstrates the ability to turn business data into clear insights and actionable recommendations.

Key skills demonstrated in this project include:

* Business performance analysis
* Dashboard design
* Data visualization
* Product profitability analysis
* Store performance analysis
* Inventory diagnosis
* Insight generation
* Strategic recommendation

The final recommendation is that ABC Toys should move from pure sales growth toward **selective and profitable growth**, focusing on high-margin products, strategic store locations, and better inventory allocation.

---

## 15. Author

**Trang Nguyễn**
Data Analyst Portfolio Project

