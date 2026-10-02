# ☕ Café Sales Analysis

An end-to-end Data Analytics project that transforms raw café transactional logs into a clean, executive-ready performance dashboard. Using **Python**, **Pandas**, **Matplotlib**, and **Seaborn**, this project uncovers hidden business trends, evaluates channel density, and resolves critical data quality anomalies.

---

## 📊 Executive Dashboard Preview

Below is the generated 6-chart business intelligence matrix showcasing the café's performance overview:

![Café Sales Analysis](Café%20Sales%20Dashboard.png)

---

## 💡 Key Business Insights

### 1. Product Demand Breakdown (`Total Units Sold by Item`)
* **Top Performers:** **Coffee** and **Salad** are the clear volume drivers for the business, both crossing **3,800+ total units sold**.
* **Low Demand:** **Cookies** represent the smallest product share, indicating a potential need for bundling promotions (e.g., Coffee + Cookie combo).

### 2. Revenue Share Analysis (`Product Sales Share Percentage`)
* **Salad** dominates the café's financial core, accounting for **21.4% of total sales revenue**, followed closely by **Sandwiches at 15.4%**.
* While coffee drives high customer traffic volume, premium-priced items like salads generate the highest net monetary yield.

### 3. Financial Velocity (`Monthly Sales Trend Over Time`)
* **Peak Seasons:** **March** and **October** represent the highest historical sales peaks, where monthly revenue successfully broke above the **\$7,000 threshold**.
* **Low Seasons:** **February** experienced a sharp revenue contraction, establishing the lowest seasonal baseline for the year.

### 4. Revenue Channels & Friction (`Sales Breakdown by Payment Method`)
* **Digital Footprint:** Mobile and Digital Wallets capture a massive portion of high-value transactions, especially for core menu items like Salads and Smoothies.
* **Data Transparency:** Transactions with missing or unrecorded payment types are strictly isolated and tracked under **"Not Specified"** rather than being deleted, preserving financial integrity.

### 5. Fulfillment Density (`Sales Density Heatmap`)
* **In-Store Domination:** **In-store dining** consistently outperforms **Takeaway orders** across all menu items. 
* Food items like Sandwiches and Salads show the highest fulfillment density inside the café, highlighting the importance of seating capacity and dine-in customer experience.

### 6. Menu Economics (`Price Distribution Histogram`)
* The café operates on a distinct **Bi-modal pricing structure**:
  * **Value Tier:** Low-cost foundational items priced between **\$1.0 and \$2.2** (e.g., Tea, Cookies).
  * **Premium Tier:** High-margin meal options priced between **\$3.0 and \$5.0** (e.g., Salads, Smoothies).
* A noticeable structural gap exists between **\$2.3 and \$3.0** where no active products are currently offered.

---

## 🛠️ Data Quality & Clean-up Protocol

To ensure 100% accurate financial reporting, a multi-step data cleaning pipeline was engineered directly into the notebook execution:
* **Anomaly Containment:** Raw system errors (`ERROR`) and unassigned strings (`UNKNOWN`) in locations and products were mapped to a structured, neutral label (**'Not Specified'**) to keep total revenue counts exact without dropping rows.
* **Timeline Restoration:** Missing transaction timestamps were sequentially imputed using forward-filling (`ffill`) to prevent the artificial destruction of historical trends.
* **Time Aggregation:** Granular daily transaction noise was compiled into aggregate **Year-Month** periodic baselines, smoothing out structural charts for better executive readability.

---

## 🚀 Tech Stack Used
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
