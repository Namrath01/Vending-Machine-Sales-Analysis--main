# Vending-Machine-Sales-Analysis-
Sales analysis of 3,475 vending machine transactions using Power BI dashboards and Python EDA — covering revenue trends, product performance, payment behavior, and machine comparison.

A data analytics project exploring **3,475 transactions** across **5 vending machines** over **8 months (Jan–Aug 2023)** to uncover sales patterns, product performance, and customer payment behavior. Built with **Power BI** for interactive dashboards and **Python** for exploratory data analysis.

---

## Project Overview

This project analyzes real-world vending machine transaction data to answer key business questions:

- Which product categories and individual products drive the most revenue?
- How do the 5 machines compare in performance?
- What are the preferred payment methods, and are there category-specific trends?
- Are there seasonal (monthly) or day-of-week sales patterns?
- What actionable recommendations can improve vending operations?

### Dataset Summary

| Metric | Value |
|--------|-------|
| Total Transactions | 3,475 |
| Total Revenue | ₹22,60,690 |
| Total Units Sold | 4,948 |
| Unique Products | 40 (10 per category) |
| Machines Tracked | 5 |
| Categories | 4 (Sandwiches, Crisps, Drinks, Snacks) |
| Payment Methods | 3 (Credit Card, Cash, Mobile) |
| Time Period | January 2, 2023 – August 31, 2023 |

---

##  Tech Stack

- **Power BI** — Interactive dashboard with slicers, drill-downs, and KPI cards
- **Python (pandas, matplotlib, seaborn)** — Exploratory data analysis and statistical summaries
- **Microsoft Excel** — Raw data storage and initial inspection
- **Git & GitHub** — Version control and project documentation

---

##  Repository Structure

```
vending-machine-sales-analysis/
│
├── README.md                          # Project documentation (this file)
├── .gitignore                         # Git ignore rules
│
├── data/
│   └── vending_machine_sales.xlsx     # Raw dataset (3,475 rows × 13 columns)
│
├── notebooks/
│   └── exploratory_analysis.ipynb     # Python EDA notebook
│
├── reports/
│   ├── vending_machine_analysis.pbix  # Power BI dashboard file
│   └── key_insights.md               # Summary of findings & recommendations
│
├── images/
│   ├── dashboard_overview.png         # Dashboard screenshot - main view
│   ├── category_breakdown.png         # Dashboard screenshot - category analysis
│   └── machine_comparison.png         # Dashboard screenshot - machine performance
│
└── scripts/
    └── data_preprocessing.py          # Data cleaning and transformation script
```

---

##  Key Findings

### 1. Category Performance

| Category | Revenue (₹) | Share (%) | Transactions | Avg Transaction Value (₹) |
|----------|-------------|-----------|--------------|--------------------------|
| Sandwiches | 7,85,810 | 34.8% | 859 | 915 |
| Crisps | 4,96,580 | 22.0% | 877 | 566 |
| Drinks | 4,93,210 | 21.8% | 897 | 550 |
| Snacks | 4,85,090 | 21.5% | 842 | 576 |

**Insight:** Sandwiches dominate revenue (34.8%) despite having the fewest transactions (859), thanks to a significantly higher average transaction value (₹915 vs ₹550–576 for other categories). Drinks lead in transaction volume but contribute only 21.8% of revenue.

### 2. Machine Performance

| Machine | Revenue (₹) | Share (%) | Transactions | Top Category |
|---------|-------------|-----------|--------------|-------------|
| Machine 1 | 4,82,320 | 21.3% | 751 | Sandwiches (₹1,73,200) |
| Machine 5 | 4,58,900 | 20.3% | 690 | Sandwiches (₹1,59,390) |
| Machine 4 | 4,49,970 | 19.9% | 679 | Sandwiches (₹1,46,930) |
| Machine 2 | 4,48,130 | 19.8% | 705 | Sandwiches (₹1,71,550) |
| Machine 3 | 4,21,370 | 18.6% | 650 | Sandwiches (₹1,34,740) |

**Insight:** Machine 1 is the top performer (21.3%), while Machine 3 underperforms by ₹60,950 compared to Machine 1. Machine 3 also has the lowest transaction count (650) — indicating either lower foot traffic or placement issues.

### 3. Payment Method Analysis

| Payment Method | Revenue (₹) | Share (%) | Transactions |
|---------------|-------------|-----------|--------------|
| Credit Card | 10,20,670 | 45.1% | 1,580 |
| Cash | 7,47,160 | 33.1% | 1,139 |
| Mobile | 4,92,860 | 21.8% | 756 |

**Insight:** Credit card is the dominant payment method (45.1% of revenue). Mobile payments account for only 21.8%, suggesting potential to grow digital adoption through promotions or UX improvements.

### 4. Monthly Revenue Trend

| Month | Revenue (₹) | Transactions | Avg Value (₹) | MoM Growth |
|-------|-------------|--------------|----------------|------------|
| January | 2,61,050 | 421 | 620 | — |
| February | 2,57,910 | 406 | 635 | -1.2% |
| March | 2,89,340 | 445 | 650 | +12.2% |
| April | 2,97,090 | 433 | 686 | +2.7% |
| May | 2,91,920 | 450 | 649 | -1.7% |
| June | 2,77,090 | 433 | 640 | -5.1% |
| July | 2,90,230 | 444 | 654 | +4.7% |
| August | 2,96,060 | 443 | 668 | +2.0% |

**Insight:** Revenue dipped in Feb (–1.2%) and June (–5.1%), with the strongest growth in March (+12.2%). April had the highest average transaction value (₹686), and the overall trend shows a gradual recovery from the mid-year dip.

### 5. Day-of-Week Patterns

| Day | Revenue (₹) | Transactions |
|-----|-------------|--------------|
| Wednesday | 3,38,060 | 507 |
| Thursday | 3,31,170 | 501 |
| Saturday | 3,23,430 | 489 |
| Sunday | 3,23,910 | 489 |
| Tuesday | 3,18,700 | 507 |
| Monday | 3,18,200 | 496 |
| Friday | 3,07,220 | 486 |

**Insight:** Wednesday is the highest-revenue day (₹3,38,060), while Friday is the lowest (₹3,07,220). Weekday sales are generally stable, with no dramatic weekend drop-off — suggesting these machines serve a consistent customer base.

### 6. Top & Bottom Products

**Top 5 by Revenue:**
| Product | Revenue (₹) | Units Sold |
|---------|-------------|-----------|
| Jimmy John's SpicyChipotle Wrap | 1,06,260 | 154 |
| McDonald's SeafoodSurprise | 91,080 | 132 |
| Subway TurkeyTango Melt | 89,600 | 128 |
| Panera VeggieDeluxe | 83,840 | 131 |
| Arby's CheesyRoast Beef | 83,820 | 127 |

**Bottom 5 by Revenue:**
| Product | Revenue (₹) | Units Sold |
|---------|-------------|-----------|
| Doritos TangyTomato | 36,050 | 103 |
| Ritz CheeseCrisps | 36,050 | 103 |
| Pepsi BerryBlast 16oz | 37,450 | 107 |
| Gatorade HerbalBoost 1L | 38,850 | 105 |
| Cheetos CheesyPuffs | 39,900 | 114 |

**Insight:** All top-5 revenue products are sandwiches, reinforcing the category's dominance. Bottom products are lower-priced snacks and drinks — they sell in decent volume but contribute less revenue per unit.

### 7. Tax Rate Impact

| Tax Rate | Transactions | Revenue (₹) | Categories |
|----------|-------------|-------------|------------|
| 18% | 2,578 | 17,67,480 | Crisps, Snacks, Sandwiches |
| 27% | 897 | 4,93,210 | Drinks only |

**Insight:** Drinks carry a higher tax rate (27% vs 18%), which inflates their price but doesn't translate to higher revenue share — suggesting price sensitivity in the beverage category.

---

##  Power BI Dashboard

>  The `.pbix` file requires [Power BI Desktop](https://powerbi.microsoft.com/desktop/) to open. Screenshots below provide a preview.

### Dashboard Features
- **KPI Cards:** Total Revenue, Total Transactions, Average Transaction Value, Total Quantity
- **Slicers:** Filter by Machine, Category, Payment Method, Month, Day of Week
- **Visuals:** Bar charts, line trends, donut charts, matrix tables, and drill-through pages
- **Interactivity:** Cross-filtering across all visuals for dynamic exploration

<!-- Add your actual screenshots here -->
![Dashboard Overview](images/dashboard_overview.png)

---

##  Business Recommendations

1. **Expand sandwich selection** — Sandwiches contribute 34.8% of revenue with the highest avg transaction value. Consider adding premium sandwich options.

2. **Investigate Machine 3** — It underperforms by ~₹61K vs Machine 1. Check placement, foot traffic, stock availability, or machine reliability.

3. **Boost mobile payments** — At only 21.8%, mobile payments are underutilized. Offer discounts or loyalty points for mobile transactions to drive adoption.

4. **Address the June dip** — Revenue dropped 5.1% in June. Investigate if this is seasonal or operational (stockouts, machine downtime).

5. **Optimize low-performing products** — Bottom-5 products (Doritos TangyTomato, Ritz CheeseCrisps, etc.) could be replaced with higher-margin alternatives.

6. **Wednesday promotions** — Leverage the natural Wednesday peak with combo deals to further maximize revenue.

7. **Drink pricing strategy** — Despite a higher tax rate (27%), drinks account for only 21.8% of revenue. Consider bundle deals (drink + sandwich) to improve category performance.

---

##  How to Run

### Power BI Dashboard
1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/)
2. Open `reports/vending_machine_analysis.pbix`
3. Use slicers to explore the data interactively

### Python Notebook
```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/vending-machine-sales-analysis.git
cd vending-machine-sales-analysis

# Install dependencies
pip install pandas matplotlib seaborn openpyxl jupyter

# Launch Jupyter
jupyter notebook notebooks/exploratory_analysis.ipynb
```

---

## 📝 Data Dictionary

| Column | Type | Description |
|--------|------|-------------|
| Timestamp | datetime | Date and time of the transaction |
| Machine | string | Machine identifier (Machine 1–5) |
| Model Number | string | Product model code (e.g., Chips 7, Drink 1) |
| Code | string | Transaction code |
| Product code | int | Unique product identifier |
| Product | string | Full product name |
| Tax Rate | int | Tax percentage (18% or 27%) |
| Category | string | Product category (Crisps, Drink, Sandwich, Snack) |
| Payment | string | Payment method (cash, credit card, mobile) |
| Quantity | int | Number of units purchased |
| Value | int | Transaction value in ₹ |
| Month | string | Month name |
| Day_of_Week | string | Day of the week |

