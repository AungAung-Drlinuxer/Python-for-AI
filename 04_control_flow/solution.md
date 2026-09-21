# ဖြေရှင်းချက်များ — If Statements

## ၁ — အပူချိန် စစ်ဆေးခြင်း

အဓိကအချက်— `if` နဲ့ comparison operator `>` ကိုသုံးပြီး condition တစ်ခုကို စစ်ပါတယ်။

```python
# Create a temperature variable
temperature = 30

# Check if the temperature is above 25
if temperature > 25:
    print("Hot day")
```

```
Hot day
```

## ၂ — Password စစ်ဆေးခြင်း

အဓိကအချက်— `==` နဲ့ တူမတူ စစ်ပြီး မတူတဲ့အခါ `else` block ကိုသုံးပါတယ်။

```python
# Create a password variable
password = "letmein"

# Check if the password matches
if password == "letmein":
    print("Access granted")
else:
    print("Access denied")
```

```
Access granted
```

## ၃ — Health အလိုက် Game Status

အဓိကအချက်— `if`၊ `elif`၊ `else` သုံးခုနဲ့ အခြေအနေ သုံးမျိုးကို အဆင့်ဆင့် စစ်ပါတယ်။

```python
# Create a health variable
health = 0

# Decide the game status based on health
if health == 0:
    print("Game over")
elif health < 30:
    print("Warning: low health")
else:
    print("Healthy")
```

```
Game over
```

## ၄ — မှတ်ချက် စစ်ဆေးခြင်း (AI chatbot)

အဓိကအချက်— `in` keyword က string ထဲမှာ စကားလုံး ပါမပါကို `True` / `False` ပြန်ပေးပါတယ်။

```python
# Create a comment variable
comment = "You are great"

# Check if the comment contains the positive keyword
if "great" in comment:
    print("Positive comment detected")
else:
    print("No positive keyword found")
```

```
Positive comment detected
```

## ၅ — နံပါတ် ခန့်မှန်းချက် စစ်ဆေးခြင်း

အဓိကအချက်— ခန့်မှန်းချက်ကို ကြီး/နည်း/ညီ ဆိုတဲ့ သုံးလမ်းကြောင်းနဲ့ `elif` တွဲပြီး စစ်ပါတယ်။

```python
# Create a guess variable
guess = 7

# Compare the guess against the target 10
if guess > 10:
    print("Too high")
elif guess < 10:
    print("Too low")
else:
    print("Correct")
```

```
Too low
```

## ၆ — Age Group ခွဲခြားခြင်း

အဓိကအချက်— အသက်အပိုင်းအခြားကို `elif` နဲ့ အဆင့်ဆင့် စစ်ပြီး ပထမဆုံး ကိုက်ညီတဲ့ အုပ်စုကိုသာ ပြပါတယ်။

```python
# Create an age variable
age = 15

# Decide the age group
if age < 13:
    print("Child")
elif age <= 19:
    print("Teenager")
else:
    print("Adult")
```

```
Teenager
```

`age = 10` ထည့်ရင် "Child" ပေါ်ပြီး၊ `age = 25` ထည့်ရင် "Adult" ပေါ်ပါတယ်။ ဒီမှာ `elif age <= 19` ကိုပဲ ရေးရုံမျှနိုင်တာက— ပထမ `if age < 13` မှားပြီးသွားရင် `age` က `13` ဒါမှမဟုတ် အဲဒါထက်ကြီးနေတာ သေချာနေလို့ပါ။
