# Assignment 3: Python - File Handling

## How to Run

### Option 1: Jupyter Notebook
1. Open `file_handling_assignment.ipynb` in Jupyter Notebook or VS Code
2. Run each cell individually to execute tasks
---

## Tasks

### **Task 1: Write Sales Records to File**
Write a list of sales to `sales_data.txt` (one per line), then read and display it. Optional: Write in comma-separated format to `sales_comma.txt`.

### **Task 2: Read Files in Different Ways**
Read `sales_data.txt` using three methods:
- `read()` - entire file
- `readline()` - first line only
- `readlines()` - all lines as list

### **Task 3: Append New Sales**
Append new sales values to `sales_data.txt` and display updated content. Optional: Count total lines.

### **Task 4: Generate Summary Report**
Read `sales_data.txt` and calculate:
- Total sales
- Highest sale
- Lowest sale
- Average sale

### **Task 5: Create Product Info File**
Ask user for 3 products and prices, write to `products.txt` in format `ProductName | Price`, then read and print.

### **Task 6: Read File Safely**
Ask user for a filename, check if it exists using `os.path.exists()`, read if found, show error if not.

### **Task 7: Mini Project - Export Discounted Prices**
Create a discount report:
- Ask user for discount percentage
- Loop through product dictionary using `.items()`
- Write to `discount_report.txt` as `ProductName | Original Price | Discounted Price`
- Read and display the report