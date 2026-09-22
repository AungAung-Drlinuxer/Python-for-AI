# Practical Python — အသေးစိတ်ရှင်းပြချက်

ဒီ module မှာ topic ၄ ခုကို အဆင့်ဆင့် ရှင်းပြပါမယ်။ တစ်ခုချင်းစီကို ဥပမာနဲ့ တွဲပြီး လေ့လာကြပါစို့။

## ၁။ Project Structure

### ဘာကို ဆိုလိုတာလဲ

Project structure ဆိုတာ ကိုယ့် program ရဲ့ ဖိုင်တွေ၊ folder တွေကို စနစ်တကျ စုစည်းခြင်းကို ဆိုလိုပါတယ်။

### ဘာကြောင့် လဲ

Script တစ်ခုတည်းနဲ့ စတင်လျှင် ရပါတယ်။ ဒါပေမယ့် project ကကြီးလာလျှင် code, data, output တွေ ရောနေပြီး ရှာခက်လာပါတယ်။ စနစ်ရှိမှ နောက်ပိုင်း ထိန်းသိမ်းရလွယ်ပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Project တစ်ခုကို folder သပ်သပ်ခွဲပါတယ်။ data ထည့်ဖို့ folder၊ code ထားဖို့ folder၊ ရလဒ်ထုတ်ဖို့ folder စသဖြင့် ခွဲပါတယ်။

ဥပမာ structure ကို အောက်မှာ ကြည့်ပါ။

```text
sales_analysis/
 data/
 sales.csv
 output/
 analysis.py
```

### ဥပမာ

```python
import os

# Create the folder structure for our project
os.makedirs("data", exist_ok=True)
os.makedirs("output", exist_ok=True)
print("Folders created!")
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI/data project တိုင်းမှာ data file တွေ အများကြီး ပါလာပါတယ်။ Structure စနစ်ရှိမှ ကိုယ့်ဘာသာလည်း မရှုပ်၊ တခြားသူတွေလည်း နားလည်လွယ်ပါတယ်။

## ၂။ Python Paths

### ဘာကို ဆိုလိုတာလဲ

Path ဆိုတာ computer ထဲက file တစ်ခုရဲ့ နေရာကို ဖော်ပြတဲ့ စာကြောင်းကို ဆိုလိုပါတယ်။

### ဘာကြောင့် လဲ

Python နဲ့ data file ဖတ်ချင်ရင် ဒီ file ဘယ်နေရာမှာ ရှိလဲဆိုတာ ပြောပြပေးရပါမယ်။ Path မမှန်ရင် FileNotFoundError ထွက်ပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Path နှစ်မျိုးရှိပါတယ်။ Absolute path က computer ရဲ့ အစကနေ အပြီး ဖော်ပြတာပါ။ Relative path က လက်ရှိ အလုပ်လုပ်နေတဲ့ folder ကနေ အစပြုပါတယ်။ `pathlib` module က path တွေကို လွယ်လွယ်ကူကူ handle လုပ်ပေးပါတယ်။

### ဥပမာ

```python
from pathlib import Path

# Current working directory
print(Path.cwd())
# Expected output: something like /home/user/sales_analysis

# Build a path to a data file
data_file = Path("data") / "sales.csv"
print(data_file)
# Expected output: data/sales.csv
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Program တစ်ခုက မတူတဲ့ computer တွေမှာ အလုပ်လုပ်ဖို့ အတွက် path ကို မှန်ကန်စွာ handle ရပါတယ်။ Windows နဲ့ Mac/Linux က path ရေးပုံ မတူလို့ `pathlib` သုံးတာ အဆင်ပြေပါတယ်။

## ၃။ Working with Files (CSV, JSON)

### ဘာကို ဆိုလိုတာလဲ

CSV က data တွေကို comma နဲ့ ခွဲထားတဲ့ ဖိုင်ပုံစံပါ။ JSON က data တွေကို structured ပုံစံနဲ့ သိမ်းတဲ့ ဖိုင်ပုံစံပါ။

### ဘာကြောင့် လဲ

Data analysis လုပ်ရင် data ကို ဖတ်ရပါတယ်။ ရလဒ်တွေကို နောက်ထပ် သုံးစွဲဖို့ JSON အနေနဲ့ သိမ်းထားတာ အဆင်ပြေပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Python မှာ CSV ဖတ်ဖို့ `csv` module ရှိပါတယ်။ JSON ရေးဖို့/ဖတ်ဖို့ `json` module ရှိပါတယ်။ CSV ရဲ့ row တစ်ခုချင်းစီက dictionary တစ်ခု ဖြစ်လာအောင် ဖတ်လို့ရပါတယ်။

### ဥပမာ

```python
import csv

# Sample data written first
with open("data/sales.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["product", "amount"])
    writer.writerow(["coffee", 5000])
    writer.writerow(["tea", 3000])

# Read the CSV file row by row
with open("data/sales.csv") as f:
    reader = csv.DictReader(f)
    for row in reader:
        print(row)
# Expected output:
# {'product': 'coffee', 'amount': '5000'}
# {'product': 'tea', 'amount': '3000'}
```

JSON အနေနဲ့ save လုပ်ပုံကို ဒီလို ရေးပါတယ်။

```python
import json

result = {"total": 8000}

# Save the result as a JSON file
with open("output/summary.json", "w") as f:
 json.dump(result, f, indent=2)
print("Saved to output/summary.json")
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI project တွေမှာ data အများစုက CSV ဒါမှမဟုတ် JSON ပုံစံနဲ့ ရောက်လာပါတယ်။ ဒီနှစ်မျိုးကို ဖတ်တတ်ရေးတတ်ရင် data တော်တော်များများကို ကိုင်တွယ်နိုင်ပါတယ်။

## ၄။ Organizing Code into Functions

### ဘာကို ဆိုလိုတာလဲ

Code တွေကို function တွေအဖြစ် ခွဲပြီး ရေးခြင်းကို ဆိုလိုပါတယ်။ Function တစ်ခုက အလုပ်တစ်ခုကိုပဲ လုပ်သင့်ပါတယ်။

### ဘာကြောင့် လဲ

Code အားလုံး တစ်နေရာတည်း ရောထားရင် ဖတ်ခက်ပြီး ပြင်လို့လည်း ခက်ပါတယ်။ Function ခွဲရင် တူတဲ့အလုပ်ကို နေရာများများက ပြန်ခေါ်သုံးလို့ရပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Function တစ်ခုကို အလုပ်တစ်ခု အာရုံစိုက်ရေးပါတယ်။ ဥပမာ — CSV ဖတ်တာ တစ်ခု၊ total တွက်တာ တစ်ခု၊ JSON save လုပ်တာ တစ်ခု။ ပြီးရင် `main()` function ကနေ အစဉ်လိုက် ခေါ်သုံးပါတယ်။

### ဥပမာ

```python
def calculate_total(rows):
    # Sum up all the amounts
 return sum(int(row["amount"]) for row in rows)

rows = [{"product": "coffee", "amount": "5000"},
        {"product": "tea", "amount": "3000"}]
print(calculate_total(rows))
# Expected output: 8000
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Project ကြီးလာလို့ data source ပြောင်းချင်ရင် function တစ်ခုပဲ ပြင်ရပါတယ်။ ဒါက program ကို ထိန်းသိမ်းရလွယ်စေပါတယ်။ AI agent တွေ ရေးတဲ့အခါလည်း တာဝန်တစ်ခုချင်း function တစ်ခု ခွဲရေးတဲ့ ပုံစံက အသုံးဝင်ပါတယ်။
