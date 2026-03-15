# Assignment 3: Python Functions Assignment

## Overview
This assignment covers essential Python function concepts including basic functions, recursion, lambda functions, and functional programming tools like `map()` and `filter()`. It also includes a practical menu-driven application combining all these concepts.

---

## Prerequisites
- Python 3.7 or higher
- A Python IDE or text editor (VS Code, PyCharm, Jupyter Notebook, etc.)

---

## How to Run

### Option 1: Run in Jupyter Notebook (Recommended)
1. Open the `functions_assignment.ipynb` file in Jupyter Notebook or VS Code with Jupyter extension.
2. Run each cell individually to see the results.
3. For Task 7 (menu), run the cell and follow the interactive prompts.

### Option 2: Run as a Python Script
1. Copy the code from the notebook into a `.py` file.
2. Open terminal/command prompt in the assignment directory.
3. Run: `python functions_assignment.py`

### Option 3: Run Individual Tasks
Copy any task code into a Python interpreter or script file and execute.

---

## Tasks Overview

### **Task 1: Basic Function - Price after Discount**
- **Function:** `apply_discount(price, discount_percentage)`
- **What it does:** Calculates the final price after applying a discount.
- **Example:**
  ```python
  apply_discount(1000, 10)  # Returns 900.0 (10% discount)
  ```

### **Task 2: Recursive Function - Factorial Utility**
- **Function:** `factorial(n)`
- **What it does:** Computes the factorial of a number using recursion.
- **Example:**
  ```python
  factorial(5)  # Returns 120 (5! = 5×4×3×2×1)
  ```

### **Task 3: Lambda Function - GST Calculator**
- **Function:** `gst = lambda price: price * 1.18`
- **What it does:** Adds 18% GST (Good and Services Tax) to a price.
- **Example:**
  ```python
  gst(100)  # Returns 118.0
  ```

### **Task 4: Using map() - Apply GST to List of Prices**
- **What it does:** Uses `map()` to apply GST to multiple prices at once.
- **Example:**
  ```python
  prices = [100, 250, 400]
  prices_with_gst = list(map(gst, prices))
  # Result: [118.0, 295.0, 472.0]
  ```

### **Task 5: Using filter() - Filter Expensive Products**
- **What it does:** Uses `filter()` to separate prices above and below 500.
- **Example:**
  ```python
  prices = [100, 250, 600, 1200]
  above_500 = list(filter(lambda p: p > 500, prices))
  # Result: [600, 1200]
  ```

### **Task 6: Combined Utility Function**
- **Function:** `process_price(prices)`
- **What it does:** Applies 10% discount using `map()` and filters results > 300.
- **Example:**
  ```python
  process_price([100, 500, 900])
  # Returns discounted list and filtered list
  ```

### **Task 7: Mini Problem - Menu Using Functions** ⭐
- **What it does:** Interactive menu system to manage a price list.
- **Features:**
  - Add prices to the list
  - Calculate average price
  - Find maximum price
  - Quit the program
  
- **How to use:**
  ```
  Menu:
  1. Add a price
  2. Get average price
  3. Get maximum price
  q. Quit
  
  Enter your choice: 1
  Enter the price to add: 500
  ```

---

## Input Validation
All user input is validated to ensure:
- Prices are numeric values (integers or decimals)
- Negative numbers are handled appropriately
- Invalid inputs display error messages and prompt for re-entry

---

## Expected Output Examples

### Task 1:
```
apply_discount(1000, 10)
# Output: 900.0
```

### Task 4:
```
Original prices: [100, 250, 400, 1200, 50]
Prices after GST: [118.0, 295.0, 472.0, 1416.0, 59.0]
```

### Task 5:
```
Prices above 500: [1200, 2000, 850]
Prices 500 or below: [100, 250, 400, 50]
```

### Task 7:
```
Menu:
1. Add a price
2. Get average price
3. Get maximum price
q. Quit

Enter your choice: 1
Enter the price to add: 500
Price 500 added. Current price list: [500]

Enter your choice: 2
Average price: 500.0

Enter your choice: q
Exiting the program.
```

---

## Key Function Concepts Covered

| Concept | Example |
|---------|---------|
| **Basic Functions** | `def apply_discount(price, discount)` |
| **Recursion** | `factorial(n) = n * factorial(n-1)` |
| **Lambda Functions** | `lambda x: x * 1.18` |
| **map()** | `list(map(gst, prices))` |
| **filter()** | `list(filter(lambda p: p > 500, prices))` |
| **Input Validation** | Check string format before conversion |

---

## Troubleshooting

### Kernel Crashes in Jupyter
- Avoid using `exit()` in notebook cells; use control flow instead.

### Float Precision Issues
- Results may show floating-point precision errors (e.g., `65.10000000000001`). This is normal in Python.

### Invalid Input Errors
- Ensure you enter numeric values when prompted.
- Decimal numbers (e.g., `500.50`) are accepted.

---

## Author Notes
- Keep all solutions within simple loops and conditionals.
- Avoid external libraries unless specifically instructed.
- Test with various input values to ensure robustness.

