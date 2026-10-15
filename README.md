# [POWER BI] Global-Superstore-Sales-and-Market-Analysis
## I. Introduction
This project uses **Power BI** to analyze Global Superstore’s sales performance, profitability, customer ordering behavior, and product returns across different markets and product categories. The interactive dashboard provides **an overview of business performance** and enables users to explore trends by time, geography, product, and customer segment to support data-driven decision-making.
## II. Objectives
- **Monitor business performance**: Track sales, profit, profit margin, average order value (AOV), and order trends over time.
- **Analyze market performance**: Compare sales, profitability, and return rates across markets, regions, and customer segments.
- **Evaluate product performance**: Identify high-performing products, profitable categories, and products generating high revenue but low or negative profit.
- **Assess returns**: Examine return rates across markets and product categories to identify potential areas for improvement.
- **Support business decisions**: Provide interactive visualizations and detailed breakdowns to help identify growth opportunities and profitability risks.
## III. Project Outcomes
- **Sales and profitability growth**: Sales and profit increased year over year, indicating positive business performance, while profit margins remained relatively stable.
- **Market performance**: APAC and EU were major sales contributors, although profitability and return rates varied across markets.
- **Product performance**: Technology contributed the largest share of profit, with Phones and Copiers among the leading sub-categories by sales.
- **Profitability risks**: Some products generated substantial revenue but recorded negative profits, highlighting potential issues with pricing, discounts, or operating costs.
- **Returns management**: Return rates differed across markets and categories, suggesting opportunities to investigate product-specific and regional return patterns.
## IV. Data Structures & Relationships
### 1. Data Structures
The dataset consists of three main tables:
- **Orders**: Stores transaction-level information, including order details, customer information, product categories, sales, and geographical attributes (**51,290 records**).
- **People**: Contains information about sales representatives assigned to different regions.
- **Returns**: Records returned orders and identifies which transactions were returned.
### 2. Data Relationships
<img width="580" height="358" alt="Screenshot 2026-10-14 210813" src="https://github.com/user-attachments/assets/827cca03-0b12-492f-9083-b0b6adc974fa" />

| **From Table** | **To Table** | **Join Key** | **Relationship Type** |
|---|---|---|---|
| `Calendar` | `Orders` | `Order Date` | One-to-Many (one calendar date can be associated with multiple order records) |
| `People` | `Orders` | `Region` | One-to-Many (one region can be associated with multiple order records) |
| `Return` | `Orders` | `Order ID` | One-to-Many (one return record can be associated with multiple order records) |

## V. Design Thinking Process
### 1. Stage 1: EMPATHIZE
<img width="1060" height="368" alt="Screenshot 2026-10-15 at 22 45 06" src="https://github.com/user-attachments/assets/155fdb13-2d0e-456d-86b2-d5c32aabf8fc" />
<img width="1061" height="399" alt="Screenshot 2026-10-15 at 22 44 40" src="https://github.com/user-attachments/assets/a42899c7-2cf5-4e0a-992b-7df2f931cbb6" />

### 2. Stage 2. DEFINE POV & NORTHSTAR METRICS
<img width="1052" height="507" alt="Screenshot 2026-10-15 at 22 45 38" src="https://github.com/user-attachments/assets/e78133a4-f9a1-4f72-acbb-f7f3b9f58a71" />

### 3. Stage 3. IDEATE

<img width="1065" height="484" alt="Screenshot 2026-10-15 at 22 45 53" src="https://github.com/user-attachments/assets/0daf466a-286e-4a0c-ade5-41d968605ba5" />
<img width="1062" height="456" alt="Screenshot 2026-10-15 at 22 46 09" src="https://github.com/user-attachments/assets/963bd683-c44b-47c0-9a00-38d87a972972" />

## VI. Visualisation
### 1. Executive Overview
<img width="802" height="455" alt="Screenshot 2026-10-15 at 20 20 12" src="https://github.com/user-attachments/assets/7317f46e-b3f6-48ba-9f62-1108d5b5d484" />

### Insights
- Total sales **grew by 24.5% YoY** to reach **$10M** (up from $8.34M in the previous year), while total profit increased by **26.5% YoY** to **hit $1M**.
- However, the overall profit margin **remained** nearly flat at **11.74%** (a modest 1.6% YoY change), indicating that business scaling is **primarily driven** by **an expansion in order volume** (rising 24.8% to 21K orders) rather than **enhanced operational cost efficiency**.
- Profit contribution is heavily skewed toward **Technology**, which commands **53.68% of total profits**. Furniture follows at **33.62%**, while Office Supplies contributes a distant **12.70%**. -> This reveals that **tech product lines** are the primary **value creators** for the enterprise.
- **APAC** leads all regions in sheer revenue scale at **$2.95M**, closely followed by the EU (**$2.46M**) and the US (**$1.81M**). A notable outlier is **Canada**, which achieves an exceptionally high profit margin of **27.41%** despite its **tiny revenue scale** (**$0.06M**). Conversely, **EMEA** lags behind with **low revenue ($0.67M)** and a **weak profit margin of 5.77%.** 

### 2. Market Analysis
<img width="1306" height="749" alt="Screenshot 2026-10-15 at 23 19 39" src="https://github.com/user-attachments/assets/92181b4e-d26a-4f0c-83a9-e171013d25df" />

### Insights
- Total enterprise sales reached **$13M** with **$1M** in total profit, an average profit margin of **11.61%**, an Average Order Value (AOV) of **$504.99**, and **25K** total orders.
- The US **leads** national sales absolutely at **$2.3M**, vastly outperforming subsequent markets like Australia or France (**$0.9M each**). ->  The **US market** serves as the p**rimary strategic pillar** for transaction volume. 
- In product categories, **furniture** in Canada recorded a staggering **118.58%** YoY revenue growth rate. ->  Canada demonstrates massive market adoption and **future growth potential** during this period.
- The **Consumer** segment yields the **highest revenue** share across nearly all major geographic markets. -> Marketing and channel distribution campaigns should **focus heavily** on individual consumer groups to maximize sales.
- Order and return tracking show **high transactional activity** in Europe (**4.6K** orders with a **6.18%** return rate) compared to APAC (**5.4K** orders with a **5.44%** return rate), highlighting areas where logistics and product quality need **monitoring**.

### 3. Product Analysis
<img width="1333" height="767" alt="Screenshot 2026-10-15 at 23 38 05" src="https://github.com/user-attachments/assets/3f85ae98-6a83-40d9-898a-3ea644f762b1" />

### Insights
- Product sub-categories like **Phones ($1.7M)** and **Copiers ($1.5M)** top the total sales rank. -> These core items capture the **highest cash inflows** for the enterprise.
- **Office Supplies** handle a **massive** operational load, recording **13.8K** total orders and **680** returns. In contrast, **Technology** captures **higher monetary value** with fewer total orders (**2.5K** orders, **201** returns), pointing to different inventory handling needs per category.
- Individual regions (such as APAC, EMEA, and Canada) showcase **distinct product consumption** **patterns** (e.g., strong demand for **Appliances** and **Accessories** in **APAC**) -> Product supply portfolios should be **customized** locally to **match** regional preferences.

### 4. Product Segment
<img width="799" height="454" alt="Screenshot 2026-10-15 at 20 20 33" src="https://github.com/user-attachments/assets/c0aef24e-6eaa-4214-a7da-1e4a75b2c744" />


### Insights
- Flagship items like the **Canon imageCLASS 2200 Advanced Copier** yield **$61.6K** in revenue and **$25.2K** in profit at **over 40%** margin. Other reliable drivers include **the Hoover Stove, Red** (**$21,147 revenue, 48.92% margin**) and Nokia Smart Phone, Full Size -> These star products **must be prioritized** for supply chain stability and marketing push.
- Several **high-revenue** items **suffer** from severe **negative profits**, such as the **Lexmark MX611dhe Monochrome Laser Printer** results in a net loss of **-$4,590** at a **-27.27%** profit margin. Other loss-makers include the **Bevis Conference Table** (**-$2,684 loss at -12.95%**) and the **Cisco TelePresence System EX90** (**-$1,811 loss at -8.00%**). -> Cost structures must be **audited** immediately, **pricing adjusted**, or loss-making items **discontinued**.
- Multiple items achieve profit margins near 49–50% (such as the **Ativa V4110MDD Shredder**). -> **Cross-selling** these high-margin items alongside core products can successfully **boost** net profitability.

## VII. Conclusions & Recommendations
### 1. Conclusions
- Revenue and profits scaled **successfully** (**$10M–$13M** sales, **$1M** profit), but profit margins **stayed flat** (**~11.6%**), driven by higher order volume rather than operational efficiency.
- The **US**, **APAC**, and **Technology products** (specifically **Phones** and **Copiers**) dominate overall revenue and profit generation.
- Certain high-revenue items (e.g., **Lexmark printers, Bevis tables**) **suffer** from **negative profit margins**, actively eroding net earnings.
- Smaller markets like **Canada** show exceptional profitability (**27.4%** margin) and rapid growth (**118.58%** YoY) in **furniture** category.

### 2. Recommendations
- **Audit**, **reprice**, or **discontinue** negative-margin products like the **Lexmark printer** (-27.27%) and **Bevis table** (-12.95%).
- **Allocate resources** to high-yield regions like **Canada** while **maintaining** core strength in the US and APAC.
- **Cross-sell** near-50% margin products (e.g., **Ativa shredders**) alongside high-volume categories.
- **Monitor** inventory and logistics closely for high-order categories (**Office Supplies**) to manage return rates.
