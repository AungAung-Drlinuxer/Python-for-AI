# အဖြေများ — try/except

## လေ့ကျင့်ခန်း ၁ — Error ရှာဖွေခြင်း

အဓိကသဘော — 0 နဲ့ စားတာက `ZeroDivisionError` ကို ဖြစ်စေပါတယ်။

```python
# Dividing by zero is impossible in math and in Python
print(10 / 0)
```

```
ZeroDivisionError: division by zero
```

## လေ့ကျင့်ခန်း ၂ — NameError ဖြေရှင်းခြင်း

အဓိကသဘော — Variable ကို အရင်သတ်မှတ်ပြီးမှ သုံးရပါတယ်။

```python
# Define the variable before using it
score = 95
print(score)
```

```
95
```

## လေ့ကျင့်ခန်း ၃ — TypeError ပြင်ခြင်း

အဓိကသဘော — String နဲ့ number ကို တိုက်ရိုက်ပေါင်းလို့မရပါ။ `str()` နဲ့ ပြောင်းပါ။

```python
# Convert the number to a string before concatenating
print("hello" + str(5))
```

```
hello5
```

## လေ့ကျင့်ခန်း ၄ — ZeroDivisionError ကို try/except နဲ့ ဖမ်းခြင်း

အဓိကသဘော — Error ဖြစ်နိုင်တဲ့ code ကို `try` ထဲထည့်ပြီး `except` နဲ့ ဖမ်းပါ။

```python
# Get a number from the user
user_input = input("Enter a number: ")

try:
    # Try to divide 100 by the user's number
    number = int(user_input)
    result = 100 / number
    print("Result:", result)
except ZeroDivisionError:
    # This runs only if the user entered zero
    print("Cannot divide by zero!")
```

```
Enter a number: 0
Cannot divide by zero!
```

## လေ့ကျင့်ခန်း ၅ — FileNotFoundError ဖမ်းခြင်း

အဓိကသဘော — File ဖတ်တဲ့ code ကို `try/except` နဲ့ ကာကွယ်ရင် program က crash မခံဘဲ 'Done!' ထိ ရောက်ပါတယ်။

```python
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

## လေ့ကျင့်ခန်း ၆ — AI agent input validation

အဓိကသဘော — User input ကို ယုံကြည်လို့မရပါ။ `try/except` နဲ့ မှားတဲ့ input ကို ကိုင်တွယ်ပြီး AI agent က crash မခံရအောင် လုပ်ပါ။

```python
# An AI agent asks the user for a number
user_input = input("Enter a number: ")

try:
    # Try to convert the input to an integer
    number = int(user_input)
    print("You entered:", number)
except ValueError:
    # This runs if the input is not a valid number, e.g. 'abc'
    print("Invalid number. Please try again.")

# The agent keeps running no matter what
print("Agent still running!")
```

```
Enter a number: abc
Invalid number. Please try again.
Agent still running!
