# Solutions — Functions

## လေ့ကျင့်ခန်း ၁ — Solution

```python
# Define a function with no parameters
def greet():
    print("Welcome to Python for AI!")

# Call the function three times
greet()
greet()
greet()
# Expected output:
# Welcome to Python for AI!
# Welcome to Python for AI!
# Welcome to Python for AI!
```

Key idea: `def` နဲ့ function ကို define လုပ်ပြီး အမည်နဲ့ `()` ခေါ်ရုံပဲ။

## လေ့ကျင့်ခန်း ၂ — Solution

```python
# Define a function that takes one parameter
def greet_name(name):
    print("Hello, " + name + "!")

# Call it with two different names
greet_name("Aung")
greet_name("Su")
# Expected output:
# Hello, Aung!
# Hello, Su!
```

Key idea: Parameter `name` ထဲမှာ ခေါ်စဉ် ထည့်လိုက်တဲ့ argument အစားဝင်သွားတယ်။

## လေ့ကျင့်ခန်း ၃ — Solution

```python
# Define a function that returns the sum
def add_numbers(a, b):
    return a + b

# Store the returned value, then print it
result = add_numbers(5, 3)
print("Result:", result)
# Expected output:
# Result: 8
```

Key idea: `print()` က ပြတာပဲ၊ `return` က တန်ဖိုးကို program ထဲ ပြန်ပေးတာဖြစ်တယ်။

## လေ့ကျင့်ခန်း ၄ — Solution

```python
# Define a function that calculates tax
def calculate_tax(price, rate):
    tax = price * rate
    return tax

# Use the returned value to compute the total
tax_amount = calculate_tax(20000, 0.05)
total = 20000 + tax_amount
print("Tax:", tax_amount)
print("Total:", total)
# Expected output:
# Tax: 1000.0
# Total: 21000.0
```

Key idea: Return ပြန်တဲ့ ရလဒ်ကို variable မှာ သိမ်းပြီး တွက်ချက်မှုအသစ်မှာ ဆက်သုံးလို့ရတယ်။

## လေ့ကျင့်ခန်း ၅ — Solution

```python
# Define a function that checks message length
def is_long_message(text):
    if len(text) > 20:
        return True
    else:
        return False

# Test with a short and a long message
print(is_long_message("Hi"))
print(is_long_message("This is a very long message"))
# Expected output:
# False
# True
```

Key idea: `len()` နဲ့ `if/else` ကို တွဲသုံးပြီး boolean တန်ဖိုး (`True`/`False`) return ပြန်တယ်။

## လေ့ကျင့်ခန်း ၆ — Solution

```python
# Define a function with a default parameter value
def build_prompt(role="assistant", task=""):
    prompt = "You are a " + role + ". Your task: " + task
    return prompt

# Call with an explicit role
prompt1 = build_prompt(role="assistant", task="summarize the text")
print(prompt1)

# Call without giving a role, so the default is used
prompt2 = build_prompt(task="translate to Burmese")
print(prompt2)
# Expected output:
# You are a assistant. Your task: summarize the text
# You are a assistant. Your task: translate to Burmese
```

Key idea: Default parameter နဲ့ function တစ်ခုကို ပိုမို စုံလင်အောင် လုပ်နိုင်ပြီး AI agent ရဲ့ prompt တွေကို ထပ်ခါထပ်ခါ တည်ဆောက်လို့ရတယ်။
