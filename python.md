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
