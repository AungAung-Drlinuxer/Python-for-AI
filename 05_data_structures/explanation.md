# Data Structures — Lists, Dictionaries, Tuples, Sets

ဒီ module မှာ Python ရဲ့ container ၄ မျိုး — list, dictionary, tuple, set — ကို အဆင့်ဆင့် လေ့လာပါမယ်။

## ၁။ Lists

### ဘာကို ဆိုလိုတာလဲ

List ဆိုတာ value အများကြီးကို အစီအစဉ်တကျ သိမ်းထားနိုင်တဲ့ container ပါ။ Square bracket `[ ]` နဲ့ ရေးပါတယ်။ ဥပမာ — ဝယ်စာရင်းတစ်ခုလိုပါ။

### ဘာကြောင့် လဲ

Python မှာ data အများကြီးကို variable တစ်ခုတည်းနဲ့ သိမ်းချင်ရင် list လိုပါတယ်။ Variable တစ်ခုချင်းစီမှာ value တစ်ခုပဲ သိမ်းလို့ရတာက သိမ်းရခက်ပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

List ထဲက item တွေကို position (index) နဲ့ ရယူနိုင်ပါတယ်။ ပထမဆုံး item က index **0** ပါ။ Item ထည့်ခြင်း၊ ပြောင်းခြင်း၊ ဖျက်ခြင်း လုပ်နိုင်ပါတယ်။

### ဥပမာ

```python
# Create a shopping list
shopping = ["rice", "oil", "eggs", "milk"]

# Access items by index (first item is 0)
print(shopping[0])   # Output: rice
print(shopping[2])   # Output: eggs

# Change an item
shopping[1] = "sunflower oil"

# Add a new item
shopping.append("salt")

# Count items
print(len(shopping))  # Output: 5
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI မှာ dataset တွေ၊ prediction result တွေ၊ prompt list တွေကို list နဲ့ သိမ်းလေ့ရှိပါတယ်။ List မရှိရင် data အများကြီးကို စီမံခန့်ခွဲရခက်ပါတယ်။

## ၂။ Dictionaries

### ဘာကို ဆိုလိုတာလဲ

Dictionary ဆိုတာ **key** နဲ့ **value** တွဲထားတဲ့ container ပါ။ Curly brace `{ }` နဲ့ ရေးပါတယ်။ ဥပမာ — နာမည်က key၊ ဖုန်းနံပါတ်က value ဖြစ်တဲ့ ဖုန်းစာရင်းလိုပါ။

### ဘာကြောင့် လဲ

Position အရ မဟုတ်ဘဲ **နာမည် (key)** နဲ့ တန်းရှာနိုင်လို့ပါ။ အရေအတွက်မသိဘဲ key တစ်ခုချင်းစီကနေ value မြန်မြန်ရနိုင်ပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Key ပေးရင် value ပြန်ရပါတယ်။ Value ထည့်ခြင်း၊ ပြောင်းခြင်း၊ key ရှိမရှိ စစ်ခြင်း လုပ်နိုင်ပါတယ်။

### ဥပမာ

```python
# A phone book dictionary
phonebook = {"Alice": "091234567", "Bob": "097654321"}

# Look up a value by key
print(phonebook["Alice"])   # Output: 091234567

# Add a new entry
phonebook["Carol"] = "098765432"

# Check if a key exists
if "Bob" in phonebook:
 print("Bob is in the phone book")  # Output: Bob is in the phone book
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI agent တွေမှာ user settings၊ model parameters၊ API responses တွေကို dictionary နဲ့ ကိုင်တွယ်လေ့ရှိပါတယ်။ JSON data က dictionary နဲ့ ပုံသဏ္ဌာန်တူတာကြောင့် အရမ်းအသုံးဝင်ပါတယ်။

## ၃။ Tuples

### ဘာကို ဆိုလိုတာလဲ

Tuple ဆိုတာ list လိုပဲ အစီအစဉ်ရှိပေမယ့် **မပြောင်းလဲနိုင်တဲ့ (immutable)** container ပါ။ Round bracket `( )` နဲ့ ရေးပါတယ်။ ဥပမာ — map ပေါ်က (x, y) coordinate လိုပါ။

### ဘာကြောင့် လဲ

Data မပြောင်းလဲသင့်တဲ့အခါ tuple သုံးရင် မှတ်မိနေတဲ့ data မထိခိုက်ဘဲ လုံခြုံပါတယ်။ Coordinate, config value တွေအတွက် သင့်တော်ပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

List လိုပဲ index နဲ့ ရယူနိုင်ပေမယ့် ပြောင်းခြင်း၊ ထည့်ခြင်း၊ ဖျက်ခြင်း မလုပ်နိုင်ပါ။ လုပ်ရင် error ဖြစ်ပါတယ်။

### ဥပမာ

```python
# A coordinate as a tuple
point = (10.5, 20.3)

# Access by index
print(point[0])   # Output: 10.5
print(point[1])   # Output: 20.3

# Trying to change it raises an error
# point[0] = 99  -> TypeError
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Model input shape၊ location coordinate တွေလို တည်ငြိုးတဲ့ data တွေကို tuple နဲ့ သိမ်းရင် မလိုအပ်ဘဲ ပြောင်းမိတာကို ကာကွယ်ပေးပါတယ်။

## ၄။ Sets

### ဘာကို ဆိုလိုတာလဲ

Set ဆိုတာ duplicate မရှိတဲ့ **unique value** များသာ သိမ်းနိုင်တဲ့ container ပါ။ Curly brace `{ }` နဲ့ ရေးပါတယ်။ ဥပမာ — ထူးခြားတဲ့ပစ္စည်းတွေပဲပါတဲ့ အိတ်လိုပါ။

### ဘာကြောင့် လဲ

Duplicate တွေအလိုမရှိတဲ့အခါ — ဥပမာ စကားလုံးထူးထူးတွေ စစ်တဲ့အခါ — set က အလိုအလျောက် duplicate ဖယ်ပေးလို့ပါ။

### ဘယ်လို အလုပ်လုပ်လဲ

Item ထည့်ရင် ရှိပြီးသားဆို duplicate မဖြစ်ပါ။ Order မရှိတာကြောင့် index နဲ့ ရယူလို့ မရပါ။ ရှိမရှိ (`in`)၊ ထည့်ခြင်း၊ ဖျက်ခြင်း လုပ်နိုင်ပါတယ်။

### ဥပမာ

```python
# A set of unique words
words = {"apple", "banana", "apple", "cherry"}

# Duplicates are removed automatically
print(words)  # Output: {'apple', 'banana', 'cherry'}

# Check membership quickly
print("banana" in words)   # Output: True

# Add a new item
words.add("mango")
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Text data မှာ unique စကားလုံးတွေရှာတာ၊ tag တွေ duplicate ဖယ်တာ စတဲ့ AI အလုပ်တွေမှာ set က အလွန်အသုံးဝင်ပါတယ်။

## ၅။ Zero-Based Indexing

List, tuple တို့မှာ ပထမဆုံး item က index **0** ပါ။ ဒုတိယက **1**၊ ဆက်တက် သွားပါတယ်။ ဒါက ကိုယ့်ရေတဲ့ code တွေမှာ off-by-one error မဖြစ်ဖို့ သတိထားရပါမယ်။

## အနှစ်ချုပ်

- **List** — ပြောင်းလဲနိုင်၊ အစီအစဉ်ရှိ။ ဝယ်စာရင်း။
- **Dictionary** — key နဲ့ value ရှာနိုင်။ ဖုန်းစာရင်း။
- **Tuple** — မပြောင်းလဲနိုင်။ Coordinate။
- **Set** — unique value သာ။ ထူးခြားပစ္စည်းအိတ်။
- ပထမဆုံး item ရဲ့ index က **0**။
