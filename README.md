# Experiment 1.B (`exp2.pdf`): Product Price Analysis Using Python Functions

## 🎯 Aim

To analyze quarterly product sales data across multiple products and quarters using 2D NumPy arrays and Python statistical functions.

## 📊 Dataset Representation

The sales data is structured as a $3 \times 4$ two-dimensional NumPy matrix (`sales`), where:
* **Rows (`axis=1`):** Represent 3 distinct products (`Product 1`, `Product 2`, `Product 3`).
* **Columns (`axis=0`):** Represent 4 financial quarters (`Q1`, `Q2`, `Q3`, `Q4`).

| Product | Q1 | Q2 | Q3 | Q4 |
| :--- | :---: | :---: | :---: | :---: |
| **Product 1** | 1000 | 1200 | 1150 | 1400 |
| **Product 2** | 800 | 950 | 1050 | 1300 |
| **Product 3** | 1500 | 1600 | 1550 | 1700 |

## ⚙️ Algorithm

1. **Start** the program.
2. **Import Library**: Import the `numpy` module as `np` for numerical array operations.
3. **Initialize 2D Sales Matrix**: Create a $3 \times 4$ NumPy array `sales` containing quarterly sales figures for 3 products across 4 quarters.
4. **Compute Product-Wise Totals**: Calculate the sum of sales across columns (`axis=1`) for each product using `np.sum(sales, axis=1)`.
5. **Compute Quarter-Wise Totals**: Calculate the sum of sales across rows (`axis=0`) for each quarter using `np.sum(sales, axis=0)`.
6. **Compute Overall Statistical Metrics**:
   * Calculate the overall mean sales across all entries using `np.mean(sales)`.
   * Identify the maximum sales figure using `np.max(sales)`.
   * Identify the minimum sales figure using `np.min(sales)`.
7. **Display Analysis Summary**: Print the original sales matrix, product-wise totals, quarter-wise totals, overall average, highest sale, and lowest sale.
8. **Stop** the program.

### 📝 Pseudocode

```text
BEGIN
    IMPORT numpy AS np

    INITIALIZE sales[3][4] ← [
        [1000, 1200, 1150, 1400],
        [ 800,  950, 1050, 1300],
        [1500, 1600, 1550, 1700]
    ]

    PRINT "Sales Data:", sales

    product_total ← SUM(sales, axis = 1)
    quarter_total ← SUM(sales, axis = 0)
    overall_avg   ← MEAN(sales)
    highest_sale  ← MAX(sales)
    lowest_sale   ← MIN(sales)

    PRINT "Total Sales per Product:", product_total
    PRINT "Total Sales per Quarter:", quarter_total
    PRINT "Overall Average Sales:", overall_avg
    PRINT "Highest Sale:", highest_sale
    PRINT "Lowest Sale:", lowest_sale
END
```

## 🛠️ Functions and Methods Used

| Category | Function / Method | Purpose / Description |
| :--- | :--- | :--- |
| **Array Creation** | `np.array()` | Initializes a 2D NumPy matrix storing product-by-quarter sales figures |
| **Aggregation** | `np.sum(..., axis=1)` | Computes row-wise totals (total annual sales per product) |
| | `np.sum(..., axis=0)` | Computes column-wise totals (total sales per quarter across all products) |
| **Statistical Analysis** | `np.mean()` | Calculates the arithmetic mean across the entire sales dataset |
| | `np.max()` | Finds the highest single quarterly sales figure |
| | `np.min()` | Finds the lowest single quarterly sales figure |

## 💻 Program / Code

```python
# Product Price & Quarterly Sales Analysis Using NumPy

import numpy as np

# Step 1: Create 2D array (Rows = Products, Columns = Quarters)
sales = np.array([
    [1000, 1200, 1150, 1400],
    [800, 950, 1050, 1300],
    [1500, 1600, 1550, 1700]
])

print("Sales Data (Rows=Products, Columns=Quarters):\n", sales)

# Step 2: Calculate Aggregations and Summary Statistics
product_total = np.sum(sales, axis=1)
quarter_total = np.sum(sales, axis=0)
overall_avg = np.mean(sales)
highest_sale = np.max(sales)
lowest_sale = np.min(sales)

# Step 3: Display Summary
print("\nTotal Sales per Product:", product_total)
print("Total Sales per Quarter:", quarter_total)
print(f"Overall Average Sales: {overall_avg:.2f}")
print("Highest Sale:", highest_sale)
print("Lowest Sale:", lowest_sale)
```

## 🖥️ Sample Output

```text
Sales Data (Rows=Products, Columns=Quarters):
 [[1000 1200 1150 1400]
 [ 800  950 1050 1300]
 [1500 1600 1550 1700]]

Total Sales per Product: [4750 4100 6350]
Total Sales per Quarter: [3300 3750 3750 4400]
Overall Average Sales: 1266.67
Highest Sale: 1700
Lowest Sale: 800
```

## ✅ Result

The program successfully analyzes quarterly product sales using 2D NumPy arrays and Python statistical aggregation functions.

## 🚀 How to Run

1. Install NumPy (if not already installed):
   ```bash
   pip install numpy
   ```
2. Run the script:
   ```bash
   python exp1b_product_sales_analysis.py
   ```