# Solutions — Environment Setup လေ့ကျင့်ခန်းများ

## ၁။ Python Version စစ်ဆေးခြင်း

Terminal ထဲမှာ command ရိုက်၍ စစ်ဆေးရုံသာ ဖြစ်သည်:

```bash
python --version
# Expected output:
# Python 3.12.4
```

**Key idea** — `python --version` က သင့်ကွန်ပျူတာထဲက Python interpreter version ကို ပြသည်။

## ၂။ ပထမဆုံး Python File ရေးခြင်း

```python
# hello.py - your first Python file
print("Hello! My name is Aung Aung.")
print("I am learning Python for AI.")
```

```
Hello! My name is Aung Aung.
I am learning Python for AI.
```

Run ရန်:

```bash
python hello.py
```

**Key idea** — `print()` function က screen ပေါ်မှာ စာသား ပြသည်။ File ကို `python <filename>` ဖြင့် run သည်။

## ၃။ ကိုယ်ပိုင် AI Workspace ဖန်တီးခြင်း

```python
# intro.py - my AI learning goals
print("Goal 1: Understand Python basics")
print("Goal 2: Learn to work with data")
print("Goal 3: Build my first AI project")
```

```
Goal 1: Understand Python basics
Goal 2: Learn to work with data
Goal 3: Build my first AI project
```

**Key idea** — Project တစ်ခုကို folder သီးသန့်ခွဲ၍ စနစ်တကျ သိမ်းဆည်းခြင်းက project ကြီးလာသည့်အခါ ရှုပ်ထွေးမှု လျော့စေသည်။

## ၄။ Virtual Environment ဖန်တီးပြီး Activate လုပ်ခြင်း

```bash
# Create the virtual environment
python -m venv .venv

# Activate on Windows
.venv\Scripts\activate

# Activate on macOS / Linux
# source .venv/bin/activate

# Expected: (.venv) appears at the start of your terminal line
```

**Key idea** — Virtual environment တစ်ခုစီက package များကို သီးသန့် သိမ်းထားပေးသဖြင့် project တွေကြား ထိခိုက်မှု မရှိပါ။

## ၅။ Package Install လုပ်ပြီး အသုံးပြုခြင်း

ပထမ ဦးစွာ package ကို install လုပ်သည်:

```bash
pip install numpy
```

ထို့နောက် script ရေးသည်:

```python
# sum.py - calculate a sum using numpy
import numpy as np

# Create an array of numbers (like data for an AI task)
numbers = np.array([5, 10, 15, 20, 25])

# Calculate and print the total
total = numbers.sum()
print("The sum is:", total)
```

```
The sum is: 75
```

**Key idea** — `pip install` ဖြင့် အခြားသူများရေးထားသော package ကို ယူ၍ `import` ဖြင့် ကိုယ့် code ထဲမှာ အသုံ
