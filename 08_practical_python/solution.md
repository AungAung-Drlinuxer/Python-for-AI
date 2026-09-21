# ဖြေရှင်းချက်များ

## ၁။ Project Folder Structure

Folder တွေကို `os.makedirs()` နဲ့ တည်ဆောက်ပြီး `exist_ok=True` က ရှိပြီးသားဖြစ်နေလျှင် error မထွက်စေပါ။

```python
import os

# Create project folders safely
os.makedirs("sales_analysis/data", exist_ok=True)
os.makedirs("sales_analysis/output", exist_ok=True)
print("Folders created!")
```

## ၂။ Path စစ်ချက်

`pathlib.Path` နဲ့ path တည်ဆောက်ပြီး `.exists()` နဲ့ ရှိမရှိ စစ်ပါတယ်။

```python
from pathlib import Path

# Build a path and check if the file exists
data_file = Path("data") / "sales.csv"

if data_file.exists():
    print("File found")
else:
    print("File missing")
```

## ၃။ CSV ရေးခြင်း/ဖတ်ခြင်း

`csv.writer` နဲ့ ရေးပြီး `csv.DictReader` နဲ့ dictionary ပုံစံ ပြန်ဖတ်ပါတယ်။

```python
import csv
import os

os.makedirs("data", exist_ok=True)

# Write a sample CSV file
with open("data/sales.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["product", "amount"])
    writer.writerow(["coffee", "5000"])
    writer.writerow(["tea", "3000"])
    writer.writerow(["juice", "7000"])

# Read it back row by row
with open("data/sales.csv") as f:
    reader = csv.DictReader(f)
    for row in reader:
        print(row)
```

## ၄။ Total တွက်ပြီး JSON Save

Amount တွေကို `int()` နဲ့ ပြောင်းပြီး ပေါင်းကာ `json.dump()` နဲ့ သိမ်းပါတယ်။

```python
import csv
import json

# Read amounts and sum them up
with open("data/sales.csv") as f:
    reader = csv.DictReader(f)
    total = sum(int(row["amount"]) for row in reader)

# Save the result as JSON
with open("output/summary.json", "w") as f:
    json.dump({"total": total}, f, indent=2)

print("Total saved:", total)
```

## ၅။ Function တွေအဖြစ် စုစည်းခြင်း

Function တစ်ခုချင်းစီက အလုပ်တစ်ခုပဲ လုပ်ပြီး `main()` က အစဉ်လိုက် ခေါ်ပါတယ်။

```python
import csv
import json

def read_sales(path):
    # Read CSV file and return rows as a list of dicts
    with open(path) as f:
        reader = csv.DictReader(f)
        return list(reader)

def calculate_total(rows):
    # Sum all amounts from the rows
    return sum(int(row["amount"]) for row in rows)

def save_summary(total, path):
    # Save the total into a JSON file
    with open(path, "w") as f:
        json.dump({"total": total}, f, indent=2)

def main():
    rows = read_sales("data/sales.csv")
    total = calculate_total(rows)
    save_summary(total, "output/summary.json")
    print("Done. Total =", total)

if __name__ == "__main__":
    main()
```

## ၆။ Product Report Function

Product တစ်ခုချင်းစီရဲ့ total ကို dictionary ထဲမှာ စုပြီး JSON အဖြစ် save လုပ်ပါတယ်။

```python
import csv
import json

def read_sales(path):
    # Read CSV file and return rows as a list of dicts
    with open(path) as f:
        reader = csv.DictReader(f)
        return list(reader)

def build_report(rows):
    # Add up amounts per product
    report = {}
    for row in rows:
        product = row["product"]
        amount = int(row["amount"])
        if product in report:
            report[product] += amount
        else:
            report[product] = amount
    return report

def save_report(report, path):
    # Save the report as JSON
    with open(path, "w") as f:
        json.dump(report, f, indent=2)

def main():
    rows = read_sales("data/sales.csv")
    report = build_report(rows)
    save_report(report, "output/report.json")
    print(report)

if __name__ == "__main__":
    main()
```

ဒီ function ခွဲရေးပုံစံက AI agent တစ်ခုကို စားပွဲပေးတဲ့ report လို data ပေးဖို့အတွက်လည်း တိုက်ရိုက် အသုံးဝင်ပါတယ်။
