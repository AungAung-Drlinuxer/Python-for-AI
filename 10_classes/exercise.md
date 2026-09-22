# လက်တွေ့ လေ့ကျင့်ခန်းများ — Classes

အောက်ပါ လေ့ကျင့်ခန်းများကို အဆင့်အတိုင်း ဖြေဆိုပါ။ တစ်ခုစီကို ကိုယ်တိုင် ကြိုးစားပြီးမှ solution ကို ကြည့်ပါ။

---

## ၁ — ရိုးရိုး Class တစ်ခု ရေးပါ

`Book` ဆိုတဲ့ class တစ်ခု ရေးပါ။ `title` နှင့် `author` ဆိုတဲ့ attributes နှစ်ခု သတ်မှတ်ပါ။ ပြီးရင် object နှစ်ခု ဖန်တီးပြီး attributes တွေကို print ပါ။

**Hints:** `__init__` method နှင့် `self` ကို အသုံးပြုပါ။ Object ဖန်တီးရန် `Book("...", "...")` လို့ ရေးပါ။

**မျှော်မှန်းအမူအယ:** Object တစ်ခုစီမှာ `title` နှင့် `author` ကို ခေါ်ကြည့်လို့ ရပါတယ်။

---

**Expected behavior:** Object တစ်ခုစီမှာ `title` နှင့် `author` ကို ခေါ်ကြည့်လို့ ရပါတယ်။

## ၂ — Method ထည့်ပါ

`Book` class ထဲမှာ `describe()` ဆိုတဲ့ method တစ်ခု ထည့်ပါ။ ဒီ method က `"{title} by {author}"` ဆိုတဲ့ string ကို ပြန်ပေးပါ။ Object တစ်ခု ဖန်တီးပြီး `describe()` ကို ခေါ်ကြည့်ပါ။

**Hints:** Method ရဲ့ ပထမ parameter က `self` ဖြစ်ရမယ်။ String format လုပ်ရန် f-string သုံးပါ။

**မျှော်မှန်းအမူအယ:** `book.describe()` က `Python Basics by John` လိုမျိုး ပြန်ပါတယ်။

---

**Expected behavior:** `book.describe()` က `Python Basics by John` လိုမျိုး ပြန်ပါတယ်။

## ၃ — Attribute ပြောင်းလဲနိုင်စေပါ

`RequestCounter` ဆိုတဲ့ class ရေးပါ။ `count` ကို 0 ကနေ စပြီး `add()` method ခေါ်တိုင်း တစ်တက် တိုးစေပါ။

**Hints:** `__init__` ထဲမှာ `self.count = 0` သတ်မှတ်ပါ။ `add()` မှာ `self.count += 1` လုပ်ပြီး တန်ဖိုး ပြန်ပါ။

**မျှော်မှန်းအမူအယ:** `add()` ကို သုံးခေါ်ရင် 1၊ 2၊ 3 ဆိုပြီး တိုးသွားပါတယ်။

---

**Expected behavior:** `add()` ကို သုံးခေါ်ရင် 1၊ 2၊ 3 ဆိုပြီး တိုးသွားပါတယ်။

## ၄ — AI Client Class ရေးပါ

`OpenAIClient` ဆိုတဲ့ class ရေးပါ။ `__init__` မှာ `api_key` ကို လက်ခံပြီး သိမ်းပါ။ `generate(prompt)` method မှာ fake response string တစ်ခု ပြန်ပါ — ဥပမာ `"Response to: {prompt}"`။ Object နှစ်ခု အသုံးပြုပြီး key တွေက သီးသန့်ဖြစ်ကြောင်း ပြပါ။

**Hints:** Fake response မှာ real API မခေါ်ပါနှင့် — string တစ်ခု ပြန်ရုံပေးပါ။ Object နှစ်ခုရဲ့ `api_key` က မတူကြောင်း print ဖြင့် ပြပါ။

**မျှော်မှန်းအမူအယ:** Object တစ်ခုစီက ကိုယ်ပိုင် `api_key` နှင့် ကိုယ်ပိုင် response ရပါတယ်။

---

**Expected behavior:** Object တစ်ခုစီက ကိုယ်ပိုင် `api_key` နှင့် ကိုယ်ပိုင် response ရပါတယ်။

## ၅ — Inheritance သုံးပါ

`AIModel` ဆိုတဲ့ parent class ရေးပါ — `name` attribute နှင့် `describe()` method ပါဝင်ပါ။ ပြီးရင် `ChatModel` ဆိုတဲ့ child class ရေးပြီး `chat(message)` method တစ်ခုပဲ ထပ်ထည့်ပါ။ `ChatModel` object တစ်ခုကနေ parent ရဲ့ method နှင့် child ရဲ့ method နှစ်လုံးလုံး ခေါ်ကြည့်ပါ။

**Hints:** Child class ကို `class ChatModel(AIModel):` လို့ ရေးပါ။ Child class မှာ `__init__` ပြန်ရေးစရာ မလိုပါ (ဆက်ခံရရှ်ပါတယ်)။

**မျှော်မှန်းအမူအယ:** `describe()` နှင့် `chat()` နှစ်ခုလုံး အလုပ်လုပ်ပါတယ်။

---

**Expected behavior:** `describe()` နှင့် `chat()` နှစ်ခုလုံး အလုပ်လုပ်ပါတယ်။

## ၆ — Data Pipeline တစ်ခု Class နဲ့ ရေးပါ

`DataPipeline` ဆိုတဲ့ class ရေးပါ။ Class ထဲမှာ text list တစ်ခု သိမ်းပါ။ `add(text)` method နှင့် `process()` method ရေးပါ — `process()` က text တွေရဲ့ စာလုံးအရေအတွက်ကို list အဖြစ် ပြန်ပါ။ ဥပမာ `"hello ai"` က 7 ပြန်ပါမယ်။

**Hints:** `__init__` မှာ `self.texts = []` နဲ့ စပါ။ `len()` function နဲ့ စာလုံးအရေအတွက် ရှာပါ။ List comprehension သုံးလို့ရပါတယ်။

**မျှော်မှန်းအမူအယ:** Text နှစ်ခု add ပြီး `process()` ခေါ်ရင် အရှည်တွေပါတဲ့ list တစ်ခု ရပါတယ်။

**Expected behavior:** Text နှစ်ခု add ပြီး `process()` ခေါ်ရင် အရှည်တွေပါတဲ့ list တစ်ခု ရပါတယ်။

