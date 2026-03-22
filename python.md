# 🐍 Python for Finance: Building a Wealth Engine

## 1. Introduction (3 Mins)
* **Goal:** Create a reusable module to power your **Dual-Wealth Dashboard**.
* **Concept:** Clean, readable Python code for financial calculations.

---

## 2. Setting Up Your Workspace
1. **Check Version:** `python --version`
2. **Create Project Folder:** `mkdir wealth_engine`
3. **Open in VS Code:** `code .`

---

## 3. Building the EMI Logic (Functions)
Create a file named `calculators.py`:

```python
def calculate_emi(p, annual_rate, months):
    r = (annual_rate / 12) / 100
    n = months
    emi = (p * r * (1 + r)**n) / ((1 + r)**n - 1)
    return round(emi, 2)

# Test it
print(f"Monthly EMI: ₹{calculate_emi(500000, 9.5, 60)}")

Data Persistence: Saving to CSV
import csv

def save_result(data):
    with open('wealth_history.csv', mode='a', newline='') as file:
        writer = csv.writer(file)
        writer.writerow(data)

# Usage
save_result(["EMI", 500000, 9.5, 60, 10500.75])

Naming: Use snake_case (e.g., interest_rate).

Comments: Don't explain what the code does, explain why.

Validation: Always check if the user entered a negative number.

### 3. See the Preview
In **VS Code**, once you have pasted the text and saved the `.md` file, press:
* **Windows:** `Ctrl + Shift + V`
* **Mac:** `Cmd + Shift + V`

This will open a beautiful, formatted "Mosh-style" document that you can show your student while you teach.

**Would you like me to write the final Python code for that FD (Fixed Deposit) function so you have the answer key ready for your student?**
Think of it like a professional kitchen:

The Function is the recipe.

The Execution (calling the function) is the cooking.

You can't start cooking if the chef hasn't read the recipe yet!
