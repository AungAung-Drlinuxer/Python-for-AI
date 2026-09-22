# Data Types — အသေးစိတ်ရှင်းလင်းချက်

## ၁။ Numbers — int နှင့် float

### ဘာကို ဆိုလိုတာလဲ

Number ဆိုတာ ကိန်းဂဏန်းတွေကို သိမ်းတဲ့ data type ပါ။ Python မှာ ကိန်းပြည့်အတွက် `int` နှင့် ဒသမကိန်းအတွက် `float` ဆိုပြီး နှစ်မျိုး ရှိပါတယ်။ `42` က `int` ပါ။ `3.14` က `float` ပါ။

### ဘာကြောင့် လဲ

AI မှာ ကိန်းဂဏန်းတွေက အရေးကြီးဆုံးပါ။ Model ရဲ့ accuracy, loss, score တို့ဟာ ကိန်းတွေ ဖြစ်လို့ပါ။ ဒါကြောင့် ကိန်း type နှစ်မျိုးကို ကောင်းကောင်း နားလည်ဖို့ လိုပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Number တွေကို ပုံမှန် သင်္ချာ လုပ်ဆောင်ချက်တွေနဲ့ တွက်လို့ ရပါတယ်။ ပေါင်း၊ နှုတ်၊ မြှောက်၊ စားတို့ အကုန် ရပါတယ်။

### ဥပမာ

```python
# Integer and float examples
accuracy = 0.95        # float value
epochs = 10           # int value

# Basic math operations
total = accuracy + 0.03
loss = 1 - accuracy
doubled = epochs * 2

print(total)    # 0.98
print(loss)     # 0.050000000000000044
print(doubled)  # 20
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Model training မှာ accuracy တိုးလာသလား၊ loss ကျလာသလား ဆိုတာကို ကိန်းတွေနဲ့ စစ်ကြည့်ရပါတယ်။ ကိန်း type မှန်ကန်ဖို့ဟာ တွက်ချက်မှု မှန်ကန်ဖို့ အခြေခံ ဖြစ်ပါတယ်။

## ၂။ Strings

### ဘာကို ဆိုလိုတာလဲ

String ဆိုတာ စာသား (text) တွေကို သိမ်းတဲ့ data type ပါ။ Single quote (`'Hello'`) ဒါမှမဟုတ် double quote (`"Hello"`) နဲ့ ရေးရပါတယ်။

### ဘာကြောင့် လဲ

AI application တွေဟာ စာသားတွေနဲ့ အများကြီး လုပ်စားပါတယ်။ User message၊ model response၊ document text အကုန်လုံးက string ပါ။

### ဘယ်လို အလုပ်လုပ်လဲ

String တွေကို `+` နဲ့ ပေါင်းလို့ ရပါတယ်။ ၎င်းကို concatenation လို့ ခေါ်ပါတယ်။ String ထဲမှာ ကိန်းရေးထားလို့လည်း ၎င်းဟာ ကိန်း မဟုတ်ဘဲ string သာ ဖြစ်ပါတယ်။

### ဥပမာ

```python
# String examples
model_name = "GPT"
greeting = "Hello"

# Joining strings together
message = greeting + ", " + model_name + "!"

print(message)  # Hello, GPT!

# A number inside quotes is still a string
score_text = "25"
print(type(score_text))  # <class 'str'>
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Chatbot တစ်ခုဆီ user က ပို့လာတဲ့ message ဟာ string ပါ။ Model က reply ပြန်တာလည်း string ပါ။ ဒါကြောင့် string ကိုင်တွယ်နိုင်ဖို့ဟာ AI development မှာ အခြေခံကျပါတယ်။

## ၃။ Booleans

### ဘာကို ဆိုလိုတာလဲ

Boolean ဆိုတာ `True` ဒါမှမဟုတ် `False` ဆိုတဲ့ တန်ဖိုး နှစ်ခုပဲ ရှိတဲ့ data type ပါ။

### ဘာကြောင့် လဲ

Program တွေဟာ decision လုပ်ရပါတယ်။ Confidence က 90% ထက် ကြီးလား? Answer မှန်လား? ဒီမျိုးမေးခွန်းတွေရဲ့ အဖြေက `True` ဒါမှမဟုတ် `False` ပါ။

### ဘယ်လို အလုပ်လုပ်လဲ

Comparison လုပ်တဲ့အခါ Boolean ရပါတယ်။ ဥပမာ — ကိန်းနှစ်ခုကို `>` ဒါမှမဟုတ် `==` နဲ့ နှိုင်းယှဉ်ရင် `True` ဒါမှမဟုတ် `False` ပြန်ပါတယ်။

### ဥပမာ

```python
# Boolean examples
accuracy = 0.95

# Comparisons produce booleans
is_ready = accuracy > 0.90
is_equal = (accuracy == 1.0)

print(is_ready)  # True
print(is_equal)  # False
print(type(is_ready))  # <class 'bool'>
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI agent တစ်ခုက အဖြေတစ်ခုကို ယုံကြည်စိတ်ချရလား ဆိုတာကို confidence threshold နဲ့ စစ်ပါတယ်။ စစ်တဲ့ ရလဒ်က `True` ဖြစ်ရင် တစ်မျိုး၊ `False` ဖြစ်ရင် တစ်မျိုး လုပ်ရပါတယ်။

## ၄။ Type Conversion — Type မတူလျှင် မရောရ

### ဘာကို ဆိုလိုတာလဲ

Type မတူတဲ့ value တွေကို တိုက်ရိုက် ရောစပ်လို့ မရပါဘူး။ ရောစပ်ချင်ရင် အရင်ဆုံး type ပြောင်းပေးရပါမယ်။ `int('25') + 5` လုပ်ရင် `30` ရပါတယ်၊ ဘာကြောင့်ဆို string `'25'` ကို int အဖြစ် အရင် ပြောင်းထားလို့ပါ။

### ဘာကြောင့် လဲ

User input က string အဖြစ် ဝင်လာတတ်ပါတယ်။ ကိန်းနဲ့ တွက်ချင်ရင် အရင် ပြောင်းဖို့ လိုပါတယ်။ မပြောင်းဘဲ ပေါင်းရင် error တက်ပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

`int()`, `float()`, `str()` တို့နဲ့ type ပြောင်းလို့ ရပါတယ်။

### ဥပမာ

```python
# Wrong: adding a string to a number directly
# score = "25" + 5  # This would give an error

# Right: convert the string to an int first
score = int("25") + 5
print(score)  # 30

# Convert a number to a string for joining text
label = "Score: " + str(score)
print(label)  # Score: 30
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

User ဆီကလာတဲ့ input က string ပါ။ ဥပမာ — user က "25" လို့ ရိုက်ရင် ၎င်းက string ပါ။ တွက်ချက်ချင်ရင် `int('25')` လို့ ပြောင်းရပါမယ်။

## ၅။ type() Function — Data Type စစ်နည်း

### ဘာကို ဆိုလိုတာလဲ

`type()` function က value တစ်ခုရဲ့ data type ကို ပြပါတယ်။ `type(42)` က `int` ပြပါတယ်။ `type(3.14)` က `float` ပါ။ `type('Hello')` က `str` ပါ။ `type(True)` က `bool` ပါ။

### ဘာကြောင့် လဲ

Code မှာ data type ဘာလဲ ဆိုတာ မသိရင် bug ရှာရခက်ပါတယ်။ `type()` နဲ့ စစ်လိုက်ရင် ချက်ချင်း သိရပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Value တစ်ခုကို `type()` ထဲ ထည့်ပြီး `print()` နဲ့ ပြရင် ရပါတယ်။

### ဥပမာ

```python
# Checking types with type()
print(type(42))      # <class 'int'>
print(type(3.14))    # <class 'float'>
print(type('Hello')) # <class 'str'>
print(type(True))    # <class 'bool'>
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Program တစ်ခုမှာ data က ဘယ် type လဲ ဆိုတာ သိနေရင် error တွေကို ကြိုတင် ကာကွယ်လို့ ရပါတယ်။ ဒါဟာ debugging အတွက် အသုံးဝင်တဲ့ ပထမဆုံး အဆင့်ပါ။

