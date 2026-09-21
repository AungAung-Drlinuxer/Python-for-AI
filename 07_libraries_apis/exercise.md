# လက်တွေ့ လေ့ကျင့်ခန်းများ — External Tools: Packages & APIs

အောက်မှာ လေ့ကျင့်ခန်း (၅) ခုရှိပါတယ်။ အလွယ်ကနေ ခက်ခဲအထိ စီထားပါတယ်။ တစ်ခုစီ ကြိုးစားလုပ်ပြီးမှ `solution.md` ကို ကြည့်ပါ။

---

## လေ့ကျင့်ခန်း ၁ — Built-in Module သုံးခြင်း

**Task:** `math` module ကို import လုပ်ပြီး —
1. 25 ရဲ့ square root တွက်ပါ
2. `math.pi` တန်ဖိုးကို ပုံနှိပ်ပါ

**Hints:** `import math` နဲ့ စပါ၊ `math.sqrt()` function ကို သုံးပါ။

**Expected behavior:** Square root အတွက် `5.0` နဲ့ pi အတွက် `3.141592653589793` ပေါ်လာပါ။

---

## လေ့ကျင့်ခန်း ၂ — External Package Install လုပ်ခြင်း

**Task:** Terminal မှာ `requests` package ကို install လုပ်ပြီး၊ Python script တစ်ခုရေးပြီး `requests` import လုပ်ကာ `requests.__version__` ကို ပုံနှိပ်ပါ။

**Hints:** Install လုပ်ရန် command က `pip install requests` ပါ၊ `__version__` က ဘယ် version ဖြစ်နေလဲ ပြပါတယ်။

**Expected behavior:** ကိုယ့်မှာ install လုပ်ထားတဲ့ requests version နံပါတ် တစ်ခု ပေါ်လာပါ (ဥပမာ `2.31.0`)။

---

## လေ့ကျင့်ခန်း ၃ — API ကနေ Data ယူခြင်း

**Task:** `https://api.exchangerate-api.com/v4/latest/USD` ကနေ USD currency rate တွေကို ယူပြီး —
1. USD ကနေ MMK (Myanmar Kyat) rate ကို ပြပါ
2. USD ကနေ JPY (Japan Yen) rate ကို ပြပါ

**Hints:** `requests.get()` နဲ့ request လုပ်ပါ၊ `.json()` နဲ့ dictionary အဖြစ် ပြောင်းပါ၊ `"rates"` key ထဲမှာ rate တွေပါတယ်။

**Expected behavior:** MMK rate တစ်ခု၊ JPY rate တစ်ခု ပေါ်လာပါ (တန်ဖိုးတွေက အချိန်ပေါ်မူတည်ပြီး ပြောင်းနိုင်ပါတယ်)။

---

## လေ့ကျင့်ခန်း ၄ — API Key ကို လုံခြုံစွာ သုံးခြင်း

**Task:** `.env` file တစ်ခု ဖန်တီးပြီး ထဲမှာ `MY_API_KEY=hello123` လို့ ရေးထားပါ။ ပြီးရင် `python-dotenv` package ကို သုံးပြီး ဒီ key ကို Python ကနေ ဖတ်ပြပါ။

**Hints:** `load_dotenv()` နဲ့ `.env` file ကို load လုပ်ပါ၊ `os.getenv()` နဲ့ key ကို ဖတ်ပါ။ `pip install python-dotenv` ကို မမေ့ပါနဲ့။

**Expected behavior:** Terminal မှာ `hello123` ဆိုတဲ့ key ပေါ်လာပါ။

---

## လေ့ကျင့်ခန်း ၅ — API Data ကို pandas နဲ့ Analyze လုပ်ခြင်း

**Task:** `https://jsonplaceholder.typicode.com/users` ကနေ user စာရင်းကို ယူပြီး `pandas` DataFrame အဖြစ် ပြောင်းကာ —
1. User စုစုပေါင်း ဘယ်နှစ်ယောက်ရှိလဲ ရေထားပါ
2. Name နဲ့ Email column နှစ်ခုကိုသာ ပြပါ

**Hints:** `pd.DataFrame(users)` နဲ့ ပြောင်းပါ၊ `len(df)` နဲ့ အရေအတွက်ရပါတယ်၊ `df[["name", "email"]]` နဲ့ column ရွေးပါ။

**Expected behavior:** `Total users: 10` နဲ့ name/email ပါတဲ့ table တစ်ခု ပေါ်လာပါ။

---

## လေ့ကျင့်ခန်း ၆ — AI Agent အတွက် Data Pipeline (Bonus)

**Task:** အထက်ပါ user data (၅) ယောက်ရဲ့ name တွေကို API ကနေ ယူပြီး တစ်ယောက်ချင်းစီအတွက် "User: <name>" ဆိုတဲ့ စာကြောင်းတွေ list အဖြစ် ပြုလုပ်ပါ။ ဒါက AI agent တစ်ခုကို data တွေ feed လုပ်မယ့် ပုံစံပါ။

**Hints:** API request လုပ်ပြီး `.json()` နဲ့ data ယူပါ၊ list comprehension နဲ့ string တွေ ဖန်တီးပါ။

**Expected behavior:** ဒီလို list တစ်ခု ရပါမယ် — `['User: Leanne Graham', 'User: Ervin Howell', ...]`

ပြီးသွားရင် `solution.md` ထဲက အဖြေတွေနဲ့ နှိုင်းယှဉ်ကြည့်ပါ!
