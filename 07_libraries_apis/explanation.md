# External Tools — Packages & APIs (ရှင်းလင်းချက်)

ဒီ file မှာ module ရဲ့ သင်ခန်းစာ (၃) ခုကို အဆင့်ဆင့် ရှင်းပြထားပါတယ်။

---

## သင်ခန်းစာ ၁ — Importing Modules

### ဘာကို ဆိုလိုတာလဲ

Import လုပ်တယ်ဆိုတာ Python ရဲ့ အသင့်ရှိပြီး code တွေကို ကိုယ့် program ထဲမှာ သုံးခွင့်ပေးလိုက်တာပါ။ Python မှာ module နှစ်မျိုးရှိပါတယ် — built-in module (Python နဲ့အတူ ပါလာတဲ့အရာ) နဲ့ external package (သီးခြား download လုပ်ရတဲ့အရာ) ပါ။

### ဘာကြောင့် လဲ

အားလုံးကို ကိုယ်တိုင်ရေးစရာမလိုပါဘူး။ တခြားသူတွေ ရေးထားပြီးသား စမ်းသပ်ထားတဲ့ code တွေကို ပြန်သုံးခြင်းအားဖြင့် အချိန်ကုန်သက်သာပြီး ပိုမိုတိကျတဲ့ ရလဒ်တွေ ရနိုင်ပါတယ်။ External package တွေကတော့ venv (virtual environment) ထဲမှာ download လုပ်ပြီးသုံးရပါတယ်၊ Python သာမက system တစ်ခုလုံးကိုပါ မဝေရောက်စေဖို့ ဒီနည်းက လုံခြုံပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Built-in module ကို `import` keyword နဲ့ ယူသုံးပါတယ်။ External package ကိုတော့ အရင်ဆုံး `pip install` နဲ့ install လုပ်ပြီးမှ import လုပ်ရပါတယ်။

### ဥပမာ

```python
# Built-in module: math comes with Python already
import math

# Use the sqrt function from the math module
result = math.sqrt(25)
print(result)  # Expected output: 5.0

# Built-in module: random
import random
random.seed(1)  # Fix the seed so the result is predictable
print(random.randint(1, 10))  # Expected output: 3 (with seed 1)
```

External package တစ်ခုကို install လုပ်ချင်ရင် terminal မှာ ဒီလိုရိုက်ပါ —

```text
pip install requests
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI project တိုင်းမှာ တစ်စုံတစ်ယောက်ရေးထားတဲ့ package တွေကို သုံးရပါတယ်။ `openai` package မရှိရင် OpenAI model တွေကို ချိတ်ဆက်လို့မရပါဘူး။ ဒါကြောင့် package တွေကို install လုပ်တတ်ဖို့၊ import လုပ်တတ်ဖို့က အခြေခံဖြစ်ပါတယ်။

---

## သင်ခန်းစာ ၂ — Working with APIs

### ဘာကို ဆိုလိုတာလဲ

API (Application Programming Interface) ဆိုတာ web service တစ်ခုနဲ့ စကားပြောနိုင်တဲ့ လမ်းကြောင်းပါ။ ဥပမာ — ရာသီဥတု service တစ်ခုက မိမိရဲ့ data တွေကို API ကနေတစ်ဆင့် ပေးပါတယ်၊ website ပေါ်မှာ လူတွေကြည့်သလို Python program တွေကလည်း API ကနေ data တွေယူနိုင်ပါတယ်။

### ဘာကြောင့် လဲ

AI ခေတ်မှာ အချက်အလက်တွေဟာ အွန်လိုင်းမှာ နေကြပါတယ်။ Model တွေကို train လုပ်ဖို့၊ AI service တွေကို သုံးဖို့အတွက် API နဲ့ ဆက်သွယ်တတ်ဖို့က မရှိမဖြစ် လိုအပ်ပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

`requests` package ကိုသုံးပြီး HTTP request လုပ်ပါတယ်။ အများအားဖြင့် response က JSON format နဲ့ ပြန်လာပြီး၊ `.json()` method နဲ့ Python dictionary အဖြစ် ပြောင်းလို့ရပါတယ်။ API key လိုအပ်တဲ့ service တွေအတွက် `python-dotenv` package နဲ့ `.env` file ထဲမှာ key ကို သိမ်းထားပြီး ခေါ်သုံးပါတယ်၊ code ထဲမှာ တိုက်ရိုက်မရေးသင့်ပါဘူး။

### ဥပမာ

```python
# Install first: pip install requests
import requests

# Send a GET request to a free public API
response = requests.get("https://api.exchangerate-api.com/v4/latest/USD")

# Convert the JSON response into a Python dictionary
data = response.json()

# Read one value from the data
usd_to_mm = data["rates"].get("MMK", "Not found")
print("1 USD =", usd_to_mm, "MMK")
# Expected output: 1 USD = 2100.0 MMK (rate may change over time)
```

API key ကို လုံခြုံစွာ သုံးပုံကတော့ —

```python
# Install first: pip install python-dotenv
import os
from dotenv import load_dotenv

# Load variables from the .env file
load_dotenv()

# Read the API key (never write the key directly in code)
api_key = os.getenv("MY_API_KEY")
print("Key loaded:", api_key is not None)
# Expected output: Key loaded: True (if .env has the key)
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI application တိုင်းလိုလိုဟာ model API တွေကို ခေါ်သုံးကြပါတယ်။ `openai` package ကိုသုံးပြီး chat model တွေနဲ့ စကားပြောတာ၊ data တွေကို summarize လုပ်တာတို့ဟာ ဒီ API အသိအမှတ်ပြုချက်ပေါ်မှာ တည်နေပါတယ်။

---

## သင်ခန်းစာ ၃ — Working with Data

### ဘာကို ဆိုလိုတာလဲ

API ကနေရထားတဲ့ data တွေကို ဖတ်၊ စစ်၊ နှိုင်းယှဉ်တတ်ဖို့က ဒီသင်ခန်းစာရဲ့ ရည်ရွယ်ချက်ပါ။ `pandas` package က data table (DataFrame ဟုခေါ်တဲ့) တွေကို လွယ်လွယ်ကူကူ ကိုင်တွယ်ခွင့်ပေးပါတယ်။

### ဘာကြောင့် လဲ

Raw data တွေက မကြာခဏ ကြီးမားပြီး ရှုပ်နေတတ်ပါတယ်။ `pandas` က စဉ်းစားရခက်တဲ့ list တွေကို table format နဲ့ ဖတ်လို့သလို ပြောင်းပေးပြီး filter လုပ်၊ sort လုပ်၊ ပျမ်းမျှ တွက်တာတွေကို တစ်ကြောင်းတည်းနဲ့ လုပ်နိုင်စေပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

JSON data တွေကို `pd.DataFrame()` ထဲ ထည့်လိုက်ရုံပါ။ ဒါဆို table ဖြစ်သွားပြီး column နဲ့ row တွေအလိုက် ရွေးချယ်စစ်ဆေးနိုင်ပါတယ်။

### ဥပမာ

```python
# Install first: pip install requests pandas
import requests
import pandas as pd

# Get a list of users from a free public API
response = requests.get("https://jsonplaceholder.typicode.com/users")
users = response.json()

# Turn the list of dictionaries into a DataFrame table
df = pd.DataFrame(users)

# Show only the name and email columns
print(df[["name", "email"]].head(3))
# Expected output:
#                name                          email
# 0     Leanne Graham        Sincere@april.biz
# 1   Ervin Howell         Shanna@melissa.tv
# 2  Clementine Bauch  Nathan@yesenia.net
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI project တွေမှာ ဒေတာကျွမ်းကျင်မှုဟာ အခြေခံပါ။ Model ကို ဘာ feed လုပ်မလဲ၊ model ရဲ့ output တွေကို ဘယ်လို စစ်မလဲဆိုတာတွေဟာ data handling နဲ့ ချိတ်နေပါတယ်။ API က data ယူတာ၊ pandas က သန့်စင်တာ၊ ဒီနှစ်ခု ပေါင်းလိုက်တော့ တကယ့် project တွေမှာ အလုပ်လုပ်နိုင်တဲ့ pipeline တစ်ခု ဖြစ်သွားပါတယ်။

---

## အနှစ်ချုပ်

- Built-in module တွေကို `import` နဲ့ တန်းသုံးလို့ရပါတယ်၊ external package တွေကတော့ venv ထဲမှာ `pip install` လုပ်ရပါတယ်
- API ဆိုတာ web service ကနေ data ယူတဲ့ လမ်းကြောင်းပါ၊ `requests` package နဲ့ ခေါ်ယူပါတယ်
- API key တွေကို `.env` file ထဲမှာ သိမ်းပြီး `python-dotenv` နဲ့ ဖတ်ပါ
- `pandas` က data table တွေကို analyze လုပ်ရတာ လွယ်ကူစေပါတယ်

နောက်ဆုံး အဆင့်မှာ လက်တွေ့ လေ့ကျင့်ခန်းတွေ လုပ်ရန် `exercise.md` ကို ဆက်ဖတ်ပါ။
