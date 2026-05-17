## 🛠️ Point-in-Time Revenue Analytics with Historical Pricing (SCD Type 2 Modeling)
📓 <a href="https://github.com/cdsouza2701/cdsouza2701/blob/main/PP_(1_3)_Historical_Revenue_Analysis_Using_Python.ipynb" target="_blank" rel="noopener noreferrer">View Project Code</a>

### 🧩 Project Overview:
This project focuses on calculating historically accurate revenue for a business with changing product prices over time. The objective was to ensure that each transaction used the correct product price that was valid at the exact time of purchase, rather than incorrectly applying current pricing to historical sales data.

The project simulates a common real-world analytics challenge involving **temporal data**, **historical version tracking**, and **point-in-time analysis**. Using structured transactional and pricing datasets, the workflow explored how historical pricing logic can be implemented using Python and pandas.

Rather than relying on simple static joins, the project required time-aware analytical logic capable of preserving historical accuracy while handling changing business conditions over time.

---

### 📁 Dataset Description:
The project used multiple structured datasets representing customer transactions, product information, and historical pricing records.

The datasets were designed to simulate a real-world pricing environment where product prices evolve over time due to operational or business changes.

#### Tables Used

### Transactions Table
Contains transactional sales records.

#### Dataset Characteristics

- **Format:** CSV
- **Data Type:** Structured transactional data
- **Grain:** One row represents one order line item
- **Key Variables:** Order date, product ID, quantity sold

### Price History Table
Contains historical product pricing records.

#### Dataset Characteristics

- **Format:** CSV
- **Data Type:** Historical versioned data
- **Grain:** One row represents one historical price version for a product
- **Key Variables:** Product ID, effective date, historical price

### Products Table
Contains product reference information and current pricing.

#### ⚠️ Key Considerations

Several characteristics of the datasets influenced the analytical approach:

- Product prices changed over time
- Historical prices needed to remain preserved
- Transaction dates did not exactly match pricing effective dates
- Revenue calculations depended on valid historical pricing logic
- Incorrect joins could distort financial reporting

These conditions made the project well-suited for practicing **temporal analytics workflows** and understanding how historical business data should be modeled and analyzed.

---

### 🎯 Objectives:

- Calculate historically accurate revenue
- Match each transaction with the correct historical product price
- Implement point-in-time lookup logic
- Explore temporal joins using Python
- Validate uniqueness and historical version integrity
- Preserve historical revenue accuracy despite pricing changes

---

### 🛠 Tools & Technologies:

- Python
- pandas
- NumPy
- Jupyter Notebook / Google Colab
- CSV data sources

---

### 🔍 Data Exploration & Validation

The project began with exploratory analysis to better understand the structure, quality, and grain of each dataset.

Initial exploration steps included:

- Inspecting sample records using `head()`
- Reviewing dataset size and structure using `shape`
- Checking column data types using `dtypes`
- Identifying missing values using `isnull()`
- Detecting duplicate records using `duplicated()`
- Evaluating uniqueness and cardinality using `nunique()`

Key validation checks included:

- Confirming transaction records were unique
- Ensuring no duplicate historical price versions existed
- Verifying date columns were converted into datetime format
- Sorting datasets chronologically before temporal joins

These validation steps helped ensure the datasets were reliable and analytically consistent before implementing the revenue logic.

---

### ⚙️ Data Preparation
The project required several preprocessing steps before historical pricing logic could be applied.

Key preparation tasks included:

- Parsing date columns into datetime format
- Sorting datasets chronologically
- Verifying grain consistency across tables
- Validating composite key uniqueness within historical pricing data

Example preprocessing workflow:

```python
transactions = (
    pd.read_csv("transactions.csv", parse_dates=["order_date"])
    .sort_values("order_date")
)

price_history = (
    pd.read_csv("price_history.csv", parse_dates=["effective_date"])
    .sort_values("effective_date")
)
```

Chronological sorting was especially important because temporal joins require ordered date values to correctly identify historical matches.

---

### 🔗 Point-in-Time Revenue Logic

The core analytical challenge involved determining which product price was valid at the exact moment each transaction occurred.

A traditional merge could not be used because:

```text
order_date ≠ effective_date
```

Instead, the project implemented a **point-in-time lookup** using:

```python
pd.merge_asof()
```

This approach performs a time-aware merge capable of identifying the closest valid historical record based on chronological logic.

The workflow matched:

- transactions by `pizza_id`
- historical prices where:

```text
effective_date <= order_date
```

This ensured that each transaction received the latest valid historical price that existed at the time of purchase.

---

### 🧠 Understanding SCD Type 2 Modeling

The project reflects concepts commonly associated with:

> Slowly Changing Dimension Type 2 (SCD Type 2)

Instead of overwriting old prices when changes occur, historical pricing versions were preserved as separate records with their own effective dates.

Example:

| pizza_id | price | effective_date |
|---|---|---|
| 4 | 16.50 | 2026-01-01 |
| 4 | 18.50 | 2026-02-01 |

This structure preserves historical truth and allows revenue calculations to remain historically accurate.

---

### ⚙️ Core Python Workflow

The historical pricing logic was implemented using pandas:

```python
revenue = pd.merge_asof(
    transactions,
    price_history,
    by='pizza_id',
    left_on='order_date',
    right_on='effective_date',
    direction='backward'
).assign(
    line_total=lambda x: x.price * x.quantity
).line_total.sum()
```

The workflow:

1. Matched transactions and pricing records by product ID
2. Located the most recent valid historical price
3. Calculated transaction-level revenue
4. Aggregated all line totals into total revenue

---

### 🔄 Temporal Join Logic

The most important component of the project was:

```python
direction="backward"
```

This instructed pandas to:

> Search backward through time and retrieve the latest valid historical record.

Equivalent business logic:

```text
effective_date <= order_date
```

This prevented future prices from incorrectly applying to historical transactions and ensured revenue integrity across the dataset.

---

### 📐 Revenue Calculation

After historical prices were assigned, revenue was calculated using:

```text
price × quantity
```

The workflow generated transaction-level line totals before aggregating them into total historical revenue.

Final calculated revenue:

```text
161,144.35
```

This output represented historically accurate revenue based on valid pricing at the time of each transaction.

---

### ⚠️ Challenges Encountered

Several analytical challenges emerged throughout the project:

- Historical pricing required temporal rather than exact-match joins
- Transaction dates and price effective dates rarely aligned exactly
- Incorrect grain handling could duplicate revenue calculations
- Chronological sorting was required before temporal merging
- Revenue accuracy depended on preserving historical pricing versions

Addressing these issues required careful validation of uniqueness, cardinality, and historical business logic.

---

### 💡 Key Insights

- Historical pricing problems require time-aware analytical logic
- Temporal joins are more complex than standard relational joins
- Understanding dataset grain is critical before merging tables
- SCD Type 2 structures preserve historical business accuracy
- Point-in-time analysis is essential for reliable financial reporting

The project also demonstrated how business rules directly influence technical implementation decisions within analytics workflows.

---

### 📌 Skills & Business Impact

#### What This Project Demonstrates

- Strong understanding of temporal analytics
- Experience implementing point-in-time lookup logic
- Practical use of pandas for historical joins
- Understanding of SCD Type 2 modeling concepts
- Data validation and revenue integrity analysis
- Ability to work with historical versioned datasets

#### Why This Project Matters

Many real-world business systems rely on historical version tracking for pricing, subscriptions, payroll, finance, and customer lifecycle management.

This project demonstrates the ability to build analytical workflows that preserve historical accuracy while handling changing business conditions over time — a critical skill in analytics, business intelligence, finance, and data engineering environments.
