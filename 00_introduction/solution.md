# Module ၁ — စာတမ်းများ အဖြေများ (Solutions)

## ၁။ သင်တန်းဆရာ profile

**အဓိက အယူအဆ —** `print()` ဖြင့် အချက်အလက်တွေကို စာကြောင်းအဖြစ် ထုတ်ပြနိုင်သည်။

```python
# Print instructor profile details
print("Name:", "Dave Ebbelaar")
print("Years of Python experience: 12")
print("Students taught: 30000")

# Expected output:
# Name: Dave Ebbelaar
# Years of Python experience: 12
# Students taught: 30000
```

အဓိကအယူအဆ — `print()` ဖြင့် စာသားနှင့် တန်ဖိုးများကိ comma ခွဲ၍ တစ်ကြောင်းချင်း ထုတ်ပြနိုင်သည်။

## ၂။ Python learning အပိုင်း ၂ ပိုင်း

**အဓိက အယူအဆ —** list ထဲမှာ အရာတွေကို သိမ်းပြီး `for` loop ဖြင့် တစ်ခုချင်း ထုတ်နိုင်သည်။

```python
# Store the two parts of learning Python
parts = ["syntax", "workflow"]

# Loop through the list and print each part
for part in parts:
 print("Part:", part)

# Expected output:
# Part: syntax
# Part: workflow
```

အဓိကအယူအဆ — Python သင်ယူမှုကို အပိုင်း ၂ ပိုင်း (syntax နှင့် workflow) အဖြစ် list ထဲမှာ သိမ်းဆည်းပြီး `for` loop ဖြင့် တစ်ပိုင်းချင်း ထုတ်ပြနိုင်သည်။

## ၃။ ကိုယ်ပိုင် profile

**အဓိက အယူအဆ —** f-string ဖြင့် variable တွေကို sentence တစ်ခုတည်းထဲ ပေါင်းစပ်နိုင်သည်။

```python
# Store your own details in variables
name = "Mg Aung"
goal = "build my own AI assistant"

# Combine variables into one sentence using an f-string
print(f"My name is {name} and I want to {goal}.")

# Expected output:
# My name is Mg Aung and I want to build my own AI assistant.
```

အဓိကအယူအဆ — f-string ဖြင့် name နှင့် goal စသည့် variable တွေကို sentence တစ်ခုတည်းအဖြစ် ပေါင်းစပ်ကာ ကိုယ်ပိုင် profile ကို ပရင့်ထုတ်နိုင်သည်။

## ၄။ AI project အိုင်ဒီယာစာရင်း

**အဓိက အယူအဆ —** `enumerate()` ဖြင့် list item တွေကို နံပါတ်နဲ့ တွဲယူနိုင်သည်။

```python
# Store AI project ideas
ideas = [
    "chatbot for customer support",
    "document summarizer",
    "resume reviewer agent",
]

# Print each idea with a number, starting from 1
for number, idea in enumerate(ideas, start=1):
 print(f"{number}. {idea}")

# Expected output:
# 1. chatbot for customer support
# 2. document summarizer
# 3. resume reviewer agent
```

အဓိကအယူအဆ — AI project idea များကို `enumerate()` ဖြင့် နံပါတ်စဉ်နှင့် တွဲဖော်ပြနိုင်သည်။

## ၅။ AI assistant အတွက် prompt များ

**အဓိက အယူအဆ —** prompt တွေကို code ဖြင့် ပုံသေ format လုပ်ထားရင် ပြန်သုံးလို့ လွယ်သည်။

```python
# Topics you want explained
topics = ["variables", "lists", "for loops"]

# Build a clear prompt for each topic
for topic in topics:
 prompt = f"Explain {topic} in Python with a simple example for a total beginner."
 print(prompt)

# Expected output:
# Explain variables in Python with a simple example for a total beginner.
# Explain lists in Python with a simple example for a total beginner.
# Explain for loops in Python with a simple example for a total beginner.
```

အဓိကအယူအဆ — prompt များကို code ဖြင့် ပုံသေ format ဖြင့် အလိုအလျောက် ထုတ်ပေးခြင်းဖြင့် ပြန်လည်သုံးစွဲလို့ရပြီး prompt များကို တညီတည်း ရေးသားရန် မလိုတော့ပါ။

## ၆။ Progress tracker

**အဓိက အယူအဆ —** `len()` ဖြင့် အရေအတွက်ယူပြီး ရာခိုင်နှုန်းတွက်ရန် ၁၀၀ နဲ့ မြှောက်နိုင်သည်။

```python
# Total modules in the course
total_modules = list(range(1, 11))  # modules 1 to 10

# Modules already completed
completed = [1, 2, 3]

# Calculate progress percentage
progress = (len(completed) / len(total_modules)) * 100

print(f"Progress: {progress:.0f}%")

# Expected output:
# Progress: 30%
```

စာတမ်းအားလုံး ကြိုးစားလုပ်ကြည့်ပြီးမှ အဖြေနဲ့ ယှဉ်ကြည့်ပါ။ ကိုယ်တိုင် လက်တွေ့လုပ်ဖို့က AI ခေတ်မှာ အရေးကြီးဆုံး အပိုင်းဖြစ်ပါသည်။

အဓိကအယူအဆ — တာဝန်ဝတ်ရားပြီးသောအရေအတွက်ကို `len()` ဖြင့်ယူပြီး စုစုပေါင်းအရေအတွက်နှင့် စားကာ ၁၀၀ နှင့် မြှောက်ခြင်းအားဖြင့် တိုးတက်မှုရာခိုင်နှုန်းကို တွက်ယူနိုင်သည်။

