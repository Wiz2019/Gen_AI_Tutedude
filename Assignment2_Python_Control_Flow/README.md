# Assignment 2: Python - Control Flow (Conditionals & Loops)

## Overview
This assignment focuses on control flow structures in Python including:
- **if/elif/else** statements for conditional logic
- **for loops** for iterating over sequences
- **while loops** with break/continue for advanced loop control

All solutions use **only conditionals and loops**—no functions, classes, or external libraries.

---

## Prerequisites
- Python 3.7 or higher
- Jupyter Notebook, VS Code with Jupyter extension, or any Python IDE
- No external libraries required

---

## How to Run

### Option 1: Run in Jupyter Notebook (Recommended)
1. Open `control_flow_assignment.ipynb` in Jupyter Notebook or VS Code
2. Run each cell individually to see the results
3. For interactive tasks (Tasks 1 and 3), follow the prompts in the notebook

### Option 2: Run as a Python Script
1. Copy task code into a `.py` file
2. Open terminal/command prompt in the assignment directory
3. Run: `python control_flow_assignment.py`

### Option 3: Run Individual Tasks
Copy any task code snippet directly into a Python interpreter (IDLE, IPython, etc.)

---

## Tasks Overview

### **Task 1: Discount Rules (if/elif/else)**

**Objective:** Apply discount rules based on order amount and calculate tax.

**Requirements:**
1. Read an integer order amount from user
2. Apply discount rules:
   - Order ≥ 2000 → 15% discount
   - 1500 ≤ Order < 2000 → 10% discount
   - 1000 ≤ Order < 1500 → 7% discount
   - Otherwise → 0% discount
3. Validate input (must be numeric)
4. Calculate and display final amount after discount
5. (Optional) Add 5% tax and show subtotal, tax, and final total

**Example Run:**
```
Enter the order amount: 2500
The final amount after discount is: 2125.0
The subtotal after discount is: 2125.0
The tax amount is: 106.25
The final total after adding tax is: 2231.25
```

**Invalid Input Handling:**
```
Enter the order amount: abc
Invalid input. Please enter a numeric value for the order amount.
```

---

### **Task 2: Process Multiple Orders (for loop)**

**Objective:** Process multiple orders at once using a for loop.

**Requirements:**
1. Given a list of orders: `[1200, 2500, 800, 1750, 3000]`
2. Apply discount rules to each order
3. Print order amount, discount percentage, and final amount for each
4. Calculate and print total revenue after all discounts
5. (Optional) Count orders that received a discount (≥ 1000)

**Example Output:**
```
Order Amount: 1200, Discount: 7%, Final Amount: 1116.0
Order Amount: 2500, Discount: 15%, Final Amount: 2125.0
Order Amount: 800, Discount: 0%, Final Amount: 800
Order Amount: 1750, Discount: 10%, Final Amount: 1575.0
Order Amount: 3000, Discount: 15%, Final Amount: 2550.0
Total Revenue After Discounts: 8166.0
Number of Orders that Received a Discount: 4
```

---

### **Task 3: User Menu (While Loop + break/continue)** ⭐

**Objective:** Create an interactive menu-driven system using while loop.

**Requirements:**
1. Create a menu with options:
   - `1` → Add order amount to a running list
   - `2` → Show all orders and totals after applying discounts
   - `q` → Quit program
2. Use `continue` for invalid options
3. Use `break` to exit on 'q'
4. Use inline if/elif/else (no functions allowed)

**Example Interaction:**
```
Enter options as '1' or '2' or 'q' to exit: 1
Enter the new order amount: 500
New order added. Current Orders: [500]

Enter options as '1' or '2' or 'q' to exit: 1
Enter the new order amount: 2500
New order added. Current Orders: [500, 2500]

Enter options as '1' or '2' or 'q' to exit: 2
Order -> Discount% -> Final Amount
500 -> 0% -> 500
2500 -> 15% -> 2125.0
Total revenue after discounts: 2625.0

Enter options as '1' or '2' or 'q' to exit: q
Exiting the program.
```

---

### **Task 5: Loop Control with Conditions (break & continue)**

**Objective:** Use break and continue statements effectively.

**Requirements:**
1. Given daily sales list: `[200, 150, 0, 400, 50, -1, 300]`
2. Rules:
   - `-1` indicates corrupted data → break and stop
   - `0` indicates no sales → continue to next
   - Any other value → add to total
3. Print running total for each valid sale
4. Print final total after loop completes (or stops)

**Example Output:**
```
Total Sales: 200
Total Sales: 350
No sales for the day.
Total Sales: 750
Total Sales: 800
Corrupted data found. Stopping the process.
Total Sales after the complete loop: 800
```

---

## Key Control Flow Concepts

| Concept | Example | When to Use |
|---------|---------|------------|
| **if/elif/else** | `if x >= 2000: ... elif x >= 1500: ...` | Multiple conditional paths |
| **for loop** | `for order in orders:` | Iterate over a sequence |
| **while loop** | `while True:` | Repeat until condition met |
| **break** | `if sale == -1: break` | Exit loop immediately |
| **continue** | `if sale == 0: continue` | Skip to next iteration |

---

## Restrictions
✅ **Allowed:**
- `if`, `elif`, `else` statements
- `for` and `while` loops
- `break` and `continue`
- Input/output (input(), print())
- Basic arithmetic and comparisons

❌ **NOT Allowed:**
- Function definitions (`def`)
- Classes
- File I/O operations
- External libraries/imports

---

## Expected Behaviors

### Input Validation
- Non-numeric input should display an error message
- Program continues after invalid input (except in Task 5 where -1 triggers break)

### Discount Calculation
All tasks use the same discount rules:
- ≥ 2000: 15%
- 1500-1999: 10%
- 1000-1499: 7%
- < 1000: 0%

### Loop Control
- Menu loops until user enters 'q'
- Invalid menu choices repeat the menu
- Task 5 uses break on corrupted data and continue on zero sales

---

## Troubleshooting

### Jupyter Kernel Crashes
- Avoid using `exit()` in notebook cells
- Use `break` to exit loops cleanly

### Loop Not Terminating
- Ensure `break` statement is reachable
- Check that exit condition ('q') is being checked

### Incorrect Discounts
- Verify elif conditions: `1500 <= order < 2000` not `1500 <= or order < 2000`
- Use correct operators: `<` and `<=`

### Float Precision Issues
- Results may show floating-point precision errors (e.g., `2231.25` instead of `2231.25`)
- This is normal in Python; no fix needed

---

## Tips for Success
1. **Test with boundary values** (999, 1000, 1499, 1500, 1999, 2000) to verify discount rules
2. **Use meaningful variable names** (`order`, `discount`, `total`) for clarity
3. **Indent consistently** to avoid syntax errors
4. **Test invalid inputs** ('abc', negative numbers, etc.)
5. **Trace through loops manually** to ensure logic is correct

---

## Sample Test Cases

### Task 1 - Test Cases:
- Input: `2500` → Expected: `2125.0` (15% discount)
- Input: `1750` → Expected: `1575.0` (10% discount)
- Input: `999` → Expected: `999` (0% discount)
- Input: `abc` → Expected: Error message

### Task 3 - Menu Test:
1. Add order 500
2. Add order 2500
3. Show all orders (should display discounts and total)
4. Quit

---

## Author Notes
- Keep all solutions simple and readable
- Focus on correct control flow logic
- Test with multiple inputs before submission

