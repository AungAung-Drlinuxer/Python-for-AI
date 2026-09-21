# အဖြေများ

## ၁။ ဝယ်စာရင်း List

သော့ချက် — `append()` နဲ့ list အဆုံးမှာ item အသစ်ထည့်နိုင်ပါတယ်။

```python
# Create a shopping list with 3 items
shopping = ["rice", "oil", "eggs"]

# Add a fourth item at the end
shopping.append("salt")

# Print the whole list
print(shopping)  # Output: ['rice', 'oil', 'eggs', 'salt']
```

## ၂။ Dictionary နဲ့ ဖုန်းစာရင်း

သော့ချက် — key ပေးရင် value တန်းရပါတယ်။ အသစ်ထည့်တာလည်း ဒီပုံစံပါ။

```python
# Create a phone book dictionary
phonebook = {"Alice": "091234567", "Bob": "097654321"}

# Add a new person
phonebook["Carol"] = "098765432"

# Look up Bob's number by key
print(phonebook["Bob"])  # Output: 097654321
```

## ၃။ Coordinate Tuple

သော့ချက် — Tuple က index နဲ့ ရယူလို့ရပေမယ့် ပြောင်းလို့မရပါ။

```python
# Store a city location as a tuple (latitude, longitude)
location = (16.8, 96.1)

# Access each value by index
print(location[0])  # Output: 16.8
print(location[1])  # Output: 96.1

# This would raise a TypeError, so we keep it commented
# location[0] = 20.0
```

## ၄။ Set နဲ့ Unique စကားလုံးများ

သော့ချက် — `split()` က word list ပြန်ပြီး `set()` က duplicate အလိုအလျောက် ဖယ်ပေးပါတယ်။

```python
# A sentence with repeated words
sentence = "apple banana apple cherry apple"

# Split into a list of words, then convert to a set
unique_words = set(sentence.split())

# Print the set and count unique words
print(unique_words)      # Output: {'apple', 'banana', 'cherry'}
print(len(unique_words))  # Output: 3
```

## ၅။ List မှာ Index နဲ့ Item ရှာခြင်း

သော့ချက် — ပထမဆုံး index က 0 ဖြစ်ပြီး နောက်ဆုံးက `len() - 1` ပါ။

```python
# A list of model names
models = ["gpt", "claude", "gemini", "llama"]

# (a) Get the first item using index 0
print(models[0])  # Output: gpt

# (b) Get the last item using length minus one
print(models[len(models) - 1])  # Output: llama

# (c) Check membership with the in keyword
print("claude" in models)  # Output: True
```

## ၆။ AI Agent Profile

သော့ချက် — container ၄ မျိုးစလုံးကို တစ်နေရာတည်း တွဲသုံးနိုင်တာက data ကို စနစ်တကျ စီစဉ်ပေးပါတယ်။

```python
# Agent tasks as a list (ordered, changeable)
tasks = ["answer questions", "summarize text"]

# Agent config as a dictionary (key-value lookup)
config = {"name": "Helper", "speed": 10}

# Agent version as a tuple (immutable)
version = (1, 0)

# Accepted commands as a set (unique values)
commands = {"ask", "summarize", "translate"}

# Look up a config value by key
print(config["name"])  # Output: Helper

# Check if a command is accepted
print("summarize" in commands)  # Output: True

# Print all parts of the profile
print(tasks, config, version, commands)
# Output: ['answer questions', 'summarize text'] {'name': 'Helper', 'speed': 10} (1, 0) {'ask', 'summarize', 'translate'}
```

### နိဂုံး

Container ၄ မျိုးကို အခြေအနေအလိုက် ရွေးသုံးတတ်ရင် data ကို ရှင်းရှင်းလင်းလင်း စီမံနိုင်ပါတယ်။ ပြောင်းလဲရင် **list**၊ key နဲ့ ရှာရင် **dictionary**၊ မပြောင်းရင် **tuple**၊ unique ဖို့ရင် **set** ပါ။
