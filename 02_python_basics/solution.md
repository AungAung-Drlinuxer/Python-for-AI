# အဖြေများ — Python Basics

## ၁။ Variable သိမ်းဆည်းခြင်း

```python
# Store personal data in variables
name = "Aung Aung"
age = 22
city = "Yangon"

# Print each value
print(name)
print(age)
print(city)
# Output:
# Aung Aung
# 22
# Yangon
```

အဓိကအကြောင်းချက် — Variable ဆိုတာ နာမည်တစ်ခုနဲ့ value တစ်ခုကို ချိတ်ဆက်ပေးတာ ဖြစ်ပါတယ်။

အဓိကအယူအဆ — Variable ဆိုတာ နာမည်တစ်ခုနဲ့ value တစ်ခုကို ချိတ်ဆက်ပေးထားပြီး print() နဲ့ ပြန်ဖော်ပြနိုင်တဲ့ အလွယ်ကျက်သာဆုံး သိမ်းဆည်းမှုနည်း ဖြစ်ပါတယ်။

## ၂။ သချာညီမျှ Operator သုံးခြင်း

```python
# Set the starting score
score = 75

# Perform calculations
doubled = score * 2        # 150
divided_by_10 = score / 10  # 7.5
remainder_by_5 = score % 5  # 0

# Print all results
print(doubled)
print(divided_by_10)
print(remainder_by_5)
# Output:
# 150
# 7.5
# 0
```

အဓိကအကြောင်းချက် — `/` က အမြဲ float ပြန်ပြီး `%` က စားပြီးကျန်တာ ပြပါတယ်။

အဓိကအယူအဆ — သချာညီမျှ Operator တွေဖြစ်တဲ့ `*`, `/`, `%` တို့နဲ့ score တန်ဖိုးကို တွက်ချက်ရာမှာ `/` က အမြဲ float ပြန်ပြီး `%` က စားပြီးကျန်တာ ပြပါတယ်။

## ၃။ နှိုင်းယှဉ်မှုနဲ့ Logical Operator

```python
# Set the temperature
temperature = 30

# Comparison checks
is_hot = temperature > 25
is_not_extreme = temperature < 40
print(is_hot)          # Output: True
print(is_not_extreme)  # Output: True

# Combine both checks with 'and'
is_comfortable = is_hot and is_not_extreme
print(is_comfortable)  # Output: True
```

အဓိကအကြောင်းချက် — နှိုင်းယှဉ်ရလဒ်က `True`/`False` ဖြစ်ပြီး `and` က နှစ်ခုလုံးမှ

အဓိကအယူအဆ — နှိုင်းယှဉ်မှု (`>` , `<`) တွေက `True`/`False` တန်ဖိုးတွေပြန်ပေးပြီး `and` operator က နှစ်ခုလုံး `True` ဖြစ်မှသာ `True` ပြန်သဖြင့် စည်းကမ်းများကို ပေါင်းစပ်စစ်ဆေးနိုင်သည်။

## ၄။ User Input သန့်စင်ခြင်း (AI အသုံးချ)
```python
# Store the raw user sentence in a variable
sentence = " PLEASE help me  "

# Chain methods: strip spaces, lowercase, then replace "please" with "kindly"
cleaned = sentence.strip().lower().replace("please", "kindly")

# Print the cleaned result
print(cleaned)
# Expected output: kindly help me
```

**အဓိကအယူအဆ** — Method သုံးခုကို `.` နဲ့ ဆက်တွဲသုံးခြင်းဖြင့် တစ်ကြောင်းတည်းနဲ့ space ဖယ်ရှား၊ အက္ခရာအသေးပြောင်း၊ စာလုံးအစားထိုးမှုကို အစီအစဉ်အတိုင်း လုပ်ဆောင်ပါတယ်။

## ၅။ Loop နဲ့ Data စစ်ဆေးခြင်း
```python
scores = [45, 78, 92, 60]

# Loop through each score in the list
for score in scores:
    # Check if the score is greater than or equal to 70
    if score >= 70:
        print(f"{score} - pass")
    else:
        print(f"{score} - fail")

# Expected output:
# 45 - fail
# 78 - pass
# 92 - pass
# 60 - fail
```

**အဓိကအယူအဆ** — list ထဲက score တစ်ခုချင်းစီကို for loop နဲ့ ယူပြီး if/else နဲ့ ၇၀ နှင့်အထက်ဖြစ်မဖြစ် စစ်ကာ f-string သုံး၍ score နှင့် pass/fail ကို တွဲပြရမည်။

## ၆။ Simple Model Response Filter (AI/Agent အသုံးချ)
```python
responses = ["Hello!", "", "How are you?", ""]

# Create an empty list to hold the allowed responses
allowed_responses = []

# Loop through each response from the agent
for response in responses:
    # Check if the response is not empty
    if len(response) > 0:
        # Add the valid response to the allowed list
        allowed_responses.append(response)

# Print the number of allowed responses
print(len(allowed_responses))
# Expected output: 2
```

**အဓိကအယူအဆ** — Loop ထဲမှာ `len(response) > 0` နဲ့ ဗလာ response တွေကို စစ်ပြီး မှန်တဲ့ response တွေကို `.append()` နဲ့ နာမည်ပေးထားတဲ့ list ထဲ ထည့်ကာ အရေအတွက်ကို `print()` နဲ့ ထုတ်ပြရန်ဖြစ်သည်။

