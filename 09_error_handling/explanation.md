# Error Handling — try/except (ရှင်းလင်းချက်)

ဒီနေရာမှာ Error handling ရဲ့ အဓိကကောင်းတွေကို အဆင့်ဆင့် ရှင်းပြပါမယ်။ အဓိက သင်ခန်းစာလေးခုကို တစ်ခုချင်းစီ လေ့လာကြရအောင်။

## ၁။ Error ဆိုတာ ဘာလဲ

**ဘာကို ဆိုလိုတာလဲ** — Error ဆိုတာ Python က instruction တစ်ခုကို လုပ်ဆောင်လို့မရတဲ့အခါ ထုတ်ပြတဲ့ သတင်းစကားပါ။ Error ဖြစ်လာရင် program က ရပ်တန့် (crash) သွားနိုင်ပါတယ်။

**ဘာကြောင့် လဲ** — တကယ့်ကမ္ဘာမှာ အမြဲတမ်း တစ်ခုချင်း အဆင်ပြေခြင်း မရှိပါ။ File တွေ ပျောက်နိုင်သလို၊ API service တွေ ပျက်နိုင်ပါတယ်။ User တွေကလည်း number မှတ်ရမယ့်နေရာမှာ 'abc' လိုမျိုး ရိုက်ခဲ့တတ်ကြပါတယ်။ ဒီအခြေအနေတွေက error တွေကို မလွှဲသာ ဖြစ်လာစေပါတယ်။

**ဘယ်လို အလုပ်လုပ်လဲ** — Python က error တစ်ခု တွေ့တဲ့အခါ "exception" တစ်ခုကို မြှင့်တင် (raise) လိုက်ပါတယ်။ ဘယ်သူမှ မဖမ်းဘူးဆိုရင် program က crash သွားပြီး error message ပြပါတယ်။ ဒါပေမယ့် `try/except` သုံးရင် error ကို ဖမ်းပြီး program ကို ဆက်လည်စေနိုင်ပါတယ်။

**ဥပမာ** —

```python
# A user types something that is not a number
user_input = "abc"
number = int(user_input)  # This raises a ValueError
print(number)
```

```
ValueError: invalid literal for int() with base 10: 'abc'
```

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — AI app တွေမှာ user input ကို လက်ခံရတဲ့နေရာ များပါတယ်။ Error ကို ကြိုတင်ကိုင်တွယ်နိုင်ရင် user ကို error နဲ့ မကြုံစေဘဲ ချောမွေ့တဲ့ experience တစ်ခု ပေးနိုင်ပါတယ်။

## ၂။ SyntaxError — code ရေးသားပုံအမှား

**ဘာကို ဆိုလိုတာလဲ** — SyntaxError က program လည်တဲ့အခါမှာ မဟုတ်ဘဲ၊ Python က code ကို ဖတ်တဲ့အခါကတည်းက တွေ့တဲ့ error ပါ။ ဥပမာ — colon (:) မထည့်ရင် SyntaxError ရပါတယ်။

**ဘာကြောင့် လဲ** — Python က တိကျတဲ့ ရေးသားပုံ (syntax) စည်းမျဉ်းတွေနဲ့ ရေးရပါတယ်။ စည်းမျဉ်းပျက်ရင် Python interpreter က code ကို စတင်လည်တာ မလုပ်နိုင်ပါဘူး။

**ဘယ်လို အလုပ်လုပ်လဲ** — Python က code တစ်ကြောင်းချင်း ဖတ်ပြီး စည်းမျဉ်းနဲ့ မကိုက်ရင် အဲဒီနေရာမှာပဲ SyntaxError ပြပါတယ်။

**ဥပမာ** —

```python
# INTENTIONAL: this snippet does NOT compile - it is the SyntaxError demo for this lesson
# Missing colon after 'if' causes a SyntaxError
x = 10
if x > 5
 print("big")
# Correct version:
# if x > 5:
# print("big")
```

```
SyntaxError: expected ':'
```

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — SyntaxError က program လည်တာပင် မစပါဘူး။ ဒါကြောင့် code ရေးတုန်းက ဂရုစိုက်ပြီး error message ကို ဖတ်တတ်ရင် မြန်မြန် ပြင်နိုင်ပါတယ်။

## ၃။ Runtime errors — program လည်နေတုန်းက ဖြစ်တဲ့ error တွေ

**ဘာကို ဆိုလိုတာလဲ** — Runtime error က syntax က မှန်ပေမယ့် program လည်နေတဲ့အခါမှာ ဖြစ်တဲ့ error တွေပါ။ သုံးခု လေ့လာပါမယ် — ZeroDivisionError, NameError, TypeError။

**ဘာကြောင့် လဲ** — Python က code ကို run တဲ့အခါမှ တွေ့နိုင်တဲ့ အခြေအနေတွေ ရှိပါတယ်။ ဥပမာ — ဘယ်ကိန်းနဲ့မဆို 0 နဲ့ စားလို့မရပါ။ မကြောင်းရှိတဲ့ variable ကို ခေါ်လို့လည်း မရပါ။ String နဲ့ number ကို ပေါင်းလို့လည်း မရပါ။

**ဘယ်လို အလုပ်လုပ်လဲ** — Program လည်နေတုန်း ဒီကိစ္စတွေနဲ့ တွေ့တဲ့အခါ Python က error အမျိုးအစားအလိုက် exception မြှင့်လိုက်ပါတယ်။

**ဥပမာ** —

```python
# Three common runtime errors

# 1. ZeroDivisionError: dividing by zero
# result = 10 / 0  # ZeroDivisionError: division by zero

# 2. NameError: using a variable that was never defined
# print(score)  # NameError: name 'score' is not defined

# 3. TypeError: adding a string and a number
# print("hello" + 5)  # TypeError: can only concatenate str (not "int") to str

# Fixed TypeError example:
print("hello" + str(5))  # Convert the number to a string first
```

```
hello5
```

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — Data ကို တွက်ချက်တဲ့ AI project တွေမှာ 0 နဲ့စားမိတာ၊ မသိရှိရတဲ့ variable တို့ ဖြစ်တတ်ပါတယ်။ Error အမျိုးအစားကို သိရင် ဘာမှားလဲဆိုတာ မြန်မြန် ခန့်မှန်းနိုင်ပါတယ်။

## ၄။ try/except — crash မခံတဲ့ program ရေးနည်း

**ဘာကို ဆိုလိုတာလဲ** — `try/except` က error ဖြစ်နိုင်တဲ့ code ကို `try` block ထဲမှာ ထားပြီး၊ error ဖြစ်ရင် `except` block က ဖမ်းပြီး ကိုင်တွယ်ပေးတဲ့ နည်းပါ။

**ဘာကြောင့် လဲ** — Error တွေက မဖြစ်မနေ ဖြစ်လာမယ်။ ဒါကြောင့် program တစ်ခုက crash သွားတာထက် error ကို ဖမ်းပြီး ဆက်လည်တာက ပိုကောင်းပါတယ်။

**ဘယ်လို အလုပ်လုပ်လဲ** — `try` block ထဲက code က error တစ်ခု မြှင့်လိုက်ရင် Python က `try` block ရဲ့ ကျန်တဲ့ပိုင်းကို ချန်ထားပြီး သင်ထားတဲ့ `except` block ထဲကို ခုန်ပါတယ်။ Program က crash မသွားပါဘူး။

**ဥပမာ** — Crash ခံရတဲ့ version နဲ့ ကိုင်တွယ်ထားတဲ့ version ကို နှိုင်းယှဉ်ကြည့်ပါမယ်။ File တစ်ခုကို ဖတ်မယ်ဆိုပါစို့။

```python
# Crash version: no error handling
# If 'data.txt' does not exist, the program stops here
# file = open("data.txt")
# print(file.read())  # FileNotFoundError: [Errno 2] No such file or directory
# print("Done!")  # This line never runs
```

```python
# Handled version: with try/except
try:
    # Try to open and read the file
 file = open("data.txt")
 print(file.read())
 file.close()
except FileNotFoundError:
    # This runs only if the file is missing
 print("File not found. Skipping...")

# The program keeps running and reaches here
print("Done!")
```

```
File not found. Skipping...
Done!
```

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — AI application တစ်ခုက အမြဲတမ်း ဆက်လည်နေဖို့ အရေးကြီးပါတယ်။ Data file တစ်ခု မရှိလို့ crash သွားတာထက် error ကို ဖမ်းပြီး user ကို သင့်တင့်တဲ့ message ပြပြီး ဆက်သွားတာက ပိုကောင်းပါတယ်။ `try/except` က production မှာ အသုံးအများဆုံး error handling နည်းပါ။

## အနှစ်ချုပ်

- Error တွေက မဖြေမနေ ဖြစ်လာနိုင်ပါတယ်
- SyntaxError က code ရေးသားပုံအမှား၊ runtime error က program လည်နေတုန်းက ဖြစ်တာပါ
- `try/except` သုံးရင် error ကို ဖမ်းပြီး program က crash မခံဘဲ ဆက်လည်နိုင်ပါတယ်
