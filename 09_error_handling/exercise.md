# လက်တွေ့ လေ့ကျင့်ခန်းများ — try/except

အောက်မှာ လေ့ကျင့်ခန်း ၆ ခု ပါဝင်ပါတယ်။ လွယ်ကူတဲ့ အဆင့်ကနေ ခက်ခဲတဲ့ အဆင့်ထိ စီစဉ်ထားပါတယ်။

## လေ့ကျင့်ခန်း ၁ — Error ရှာဖွေခြင်း

**Task** — အောက်က code မှာ ဘာ error ဖြစ်မလဲ အရင်ခန့်မှန်းပြီးမှ run ကြည့်ပါ။

```python
print(10 / 0)
```

**Hint** — 0 နဲ့ စားလို့ရလဲဆိုတာ စဉ်းစားပါ။
**Expected behavior** — Program က crash သွားပြီး error message တစ်ခု ပေါ်မယ်။ Error ရဲ့ အမျိုးအစား ဘာလဲဆိုတာ မှတ်ပါ။

**Hints:** 0 နဲ့ စားတဲ့အခါ `ZeroDivisionError` ဖြစ်ပါတယ်။ Error message မှာ `division by zero` လို့ ပေါ်လာမယ်။

## လေ့ကျင့်ခန်း ၂ — NameError ဖြေရှင်းခြင်း

**Task** — ဒီ code မှာ `NameError` ဖြစ်နေတဲ့အတွက် ပြင်ပါ။

```python
print(score)
```

**Hint** — `score` ဆိုတဲ့ variable ကို အရင်သတ်မှတ်ဖို့ လိုပါတယ်။
**Expected behavior** — Program က error မပြဘဲ `score` ရဲ့ တန်ဖိုးကို ထုတ်ပြနိုင်ရမယ်။

**Hints:** `score = 0` လိုမျိုး variable ကို အရင်သတ်မှတ်ပြီးမှ `print(score)` ရေးပါ။

## လေ့ကျင့်ခန်း ၃ — TypeError ပြင်ခြင်း

**Task** — `"hello" + 5` က TypeError ပြပါတယ်။ Error မဖြစ်အောင် ပြင်ပြီး `hello5` ဆိုတာ ထွက်အောင် ရေးပါ။

**Hint** — `str()` နဲ့ number ကို string ပြောင်းနိုင်ပါတယ်။
**Expected behavior** — Output က `hello5` ဖြစ်ရမယ်။

**Hints:** `print("hello" + str(5))` လိုမျိုး `str()` function နဲ့ 5 ကို string ပြောင်းပါ။

## လေ့ကျင့်ခန်း ၄ — try/except သုံးပြီး ZeroDivisionError ဖမ်းခြင်း

**Task** — User ရင့်ထည့်တဲ့ ကိန်းနဲ့ 100 ကို စားပြီး ရလဒ်ပြမယ့် program ရေးပါ။ 0 ရင့်ထည့်ရင် `ZeroDivisionError` ကို `try/except` နဲ့ ဖမ်းပြီး "Cannot divide by zero!" ဆိုတာ ပြပါ။

**Hint** — စားတဲ့ code ကို `try` ထဲထည့်ပါ။ `except ZeroDivisionError:` နဲ့ ဖမ်းပါ။
**Expected behavior** — 0 ရင့်သွင်းရင် program က crash မခံဘဲ မှန်တဲ့ message ပြပြီး ဆက်လည်ရမယ်။

**Hints:** `try:` block ထဲမှာ 100 ကို user ရင့်ထည့်တဲ့ ကိန်းနဲ့ စားတဲ့ code ထည့်ပြီး `except ZeroDivisionError:` နဲ့ error message ထုတ်ပါ။

## လေ့ကျင့်ခန်း ၅ — FileNotFoundError ဖမ်းခြင်း

**Task** — `data.txt` ဆိုတဲ့ file ကို ဖတ်မယ့် program ရေးပါ။ File မရှိရင် `try/except` နဲ့ ဖမ်းပြီး "File not found. Skipping..." ပြပါ။ Program ရဲ့ အဆုံးမှာ "Done!" ပြရမယ်။

**Hint** — `open()` ကို `try` block ထဲမှာ ထည့်ပါ။ `except FileNotFoundError:` နဲ့ ဖမ်းပါ။
**Expected behavior** — File မရှ်ေလည်း program က crash မခံဘဲ "Done!" ထိ ရောက်ရမယ်။

**Hints:** `try:` block ထဲမှာ `open("data.txt")` ထည့်ပြီး `except FileNotFoundError:` နဲ့ error message ထုတ်ပါ။ Program အဆုံးမှာ `print("Done!")` ထည့်ပါ။

## လေ့ကျင့်ခန်း ၆ — AI agent input validation

**Task** — AI agent တစ်ခုက user ဆီက ကိန်းတစ်ခု တောင်းခံတယ်ဆိုပါစို့။ User က number အစား 'abc' လိုမျိုး ရိုက်တတ်ပါတယ်။ `input()` နဲ့ ကိန်းယူပြီး `int()` ပြောင်းတဲ့ code ကို `try/except` နဲ့ ကာကွယ်ပါ။ Error ဖြစ်ရင် "Invalid number. Please try again." ဆိုတာ ပြပြီး program က crash မခံရအောင် ရေးပါ။

**Hint** — `int()` က number မဟုတ်တဲ့ string ကို ပြောင်းလို့မရရင် error တက်ပါတယ်။ ဒါက ValueError ပါ။ `except ValueError:` သုံးကြည့်ပါ။
**Expected behavior** — User က 'abc' ရိုက်ရင် program က crash မခံဘဲ မှန်တဲ့ message ပြရမယ်။

**Hints:** `try:` block ထဲမှာ `int(input())` ထည့်ပြီး `except ValueError:` နဲ့ error message ထုတ်ပါ။

