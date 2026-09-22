# အဖြေများ — try/except

## လေ့ကျင့်ခန်း ၁ — Error ရှာဖွေခြင်း

**အဓိကအယူအဆ** — 0 နဲ့ စားတာက `ZeroDivisionError` ကို ဖြစ်စေပါတယ်။

```python
# Dividing by zero is impossible in math and in Python
print(10 / 0)
```

```
ZeroDivisionError: division by zero
```

## လေ့ကျင့်ခန်း ၂ — NameError ဖြေရှင်းခြင်း

**အဓိကအယူအဆ** — Variable ကို အရင်သတ်မှတ်ပြီးမှ သုံးရပါတယ်။

```python
# Define the variable before using it
score = 95
print(score)
```

```
95
```

## လေ့ကျင့်ခန်း ၃ — TypeError ပြင်ခြင်း

**အဓိကအယူအဆ** — String နဲ့ number ကို တိုက်ရိုက်ပေါင်းလို့မရပါ။ `str()` နဲ့ ပြောင်းပါ။

```python
# Convert the number to a string before concatenating
print("hello" + str(5))
```

```
hello5
```

## လေ့ကျင့်ခန်း ၄ — ZeroDivisionError ကို try/except နဲ့ ဖမ်းခြင်း

**အဓိကအယူအဆ** — Error ဖြစ်နိုင်တဲ့ code ကို `try` ထဲထည့်ပြီး `except` နဲ့ ဖမ်းပါ။

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

**အဓိကအယူအဆ** — File ဖတ်တဲ့ code ကို `try/except` နဲ့ ကာကွယ်ရင် program က crash မခံဘဲ 'Done!' ထိ ရောက်ပါတယ်။

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

**အဓိကအယူအဆ** — User input ကို ယုံကြည်လို့မရပါ။ `try/except` နဲ့ မှားတဲ့ input ကို ကိုင်တွယ်ပြီး AI agent က crash မခံရအောင် လုပ်ပါ။

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
```

**ရှင်းလင်းချက်** — `int(user_input)` က `'abc'` ကဲ့သို့သော စာသားကို integer အဖြစ် ပြောင်းလို့မရသဖြင့် `ValueError` ကို ထုတ်ပေးပါသည်။ `try` block အတွင်းမှာ error ဖြစ်လို့က `except ValueError` block က လမ်းစာချက်ကို ဖမ်းယူပြီး မှားနေကြောင်း အသုံးပြုသူကို အသိပေးပါသည်။ Program က crash မဖြစ်ဘဲ `Agent still running!` ကို ဆက်လက် print လုပ်နိုင်ပါသည်။

**မေးခွန်း** — User input ကို အကြိမ်များစွာ မေးပြီး မှန်ကန်တဲ့ number ရသည်အထိ loop လုပ်ချင်ရင် `while` loop နဲ့ ဒီ pattern ကို ဘယ်လို ပေါင်းစပ်မလဲ?
