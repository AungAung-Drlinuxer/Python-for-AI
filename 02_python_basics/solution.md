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
