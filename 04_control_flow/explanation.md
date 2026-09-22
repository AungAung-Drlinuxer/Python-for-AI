# Control Flow — If Statements အသေးစိတ်ရှင်းလင်းချက်

## Topic 1 — if Statement အခြေခံ

### ဘာကို ဆိုလိုတာလဲ

`if` statement ဆိုတာက ပရိုဂရမ်ရဲ့ "ဆုံးဖြတ်ချက် ချမှတ်စနစ်" ပါ။ ဒါက "IF ဒါမှန်ရင် THEN ဒီလိုလုပ်" လို့ ဆိုလိုတာပါ။

### ဘာကြောင့်လဲ

ပရိုဂရမ်တွေက အမြဲတစ်နက် တစ်လမ်းတည်း မဟုတ်ဘဲ အခြေအနေပေါ် မူတည်ပြီး ကွဲပြားတဲ့ လုပ်ဆောင်ချက်တွေ လုပ်ဖို့ လိုပါတယ်။ ATM စက်ကို စဉ်းစားပါ— password မှားရင် အဝင်မပေးသင့်ဘူး။ ဒီလို ခွဲခြားရွေးချယ်မှုအတွက် `if` က လိုအပ်ပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

`if` ရဲ့ နောက်မှာ condition တစ်ခု ရှိပါတယ်။ Condition ဆိုတာက `True` ဒါမှမဟုတ် `False` ဖြစ်နေတဲ့ နားလည်ချက်တစ်ခုပါ။ Condition က `True` ဖြစ်ရင် `if` block ထဲက code တွေ အလုပ်လုပ်ပါတယ်။ `False` ဖြစ်ရင် ကျော်သွားပါတယ်။ သတိထားဖို့က— `if` line အဆုံးမှာ colon (`:`) ထည့်ရပြီး block ထဲက code တွေကို space ၄ ခုနဲ့ စတင်ရပါတယ်။ ဒီ space ခြားခြင်းကို **indentation** လို့ ခေါ်ပါတယ်။

### ဥပမာ

```python
temperature = -5

# Check if the temperature is below zero
if temperature < 0:
 print("Snow icon")

# This line runs no matter what
print("Done checking weather")
```

```
Snow icon
Done checking weather
```

`temperature < 0` က `True` ဖြစ်လို့ "Snow icon" ပါ ပေါ်လာပါတယ်။

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Weather app တွေ၊ game တွေ၊ ATM တွေ အားလုံးက condition စစ်ပြီး လုပ်ဆောင်ချက်ကို ပြောင်းလဲကြတယ်။ AI app တွေမှာလည်း data input တစ်ခုက သတ်မှတ်စည်းမျဉ်းနဲ့ ကိုက်ညီမူ ကွဲပြားတဲ့ output ထုတ်ဖို့ `if` က အခြေခံကျပါတယ်။

## Topic 2 — else Statement

### ဘာကို ဆိုလိုတာလဲ

`else` က `if` ရဲ့ condition မှားသွားရင် အလုပ်လုပ်မယ့် အပိုင်းပါ။ "မဟုတ်ရင် ဒီလိုလုပ်" လို့ ဆိုလိုတာပါ။

### ဘာကြောင့်လဲ

Condition မှားတဲ့အခါ ဘာမှ မလုပ်ဘဲ ထားချင်မှ ထားမယ်။ ဒါပေမယ့် မှားရင်လည်း တစ်ခုခု လုပ်စေချင်တဲ့ အခါတွေ များပါတယ်။ ဥပမာ— login မှားရင် "Password မှားပါတယ်" လို့ ပြောပြဖို့ လိုပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

`if` block အောက်မှာ `else:` ကို ထည့်ပါတယ်။ Python က `if` condition ကို စစ်ပြီး `False` ဖြစ်ရင် `else` block ထဲက code ကို သွားအလုပ်လုပ်ပါတယ်။ နှစ်ခုထဲက တစ်ခုတည်းပဲ အလုပ်လုပ်ပါတယ်— နှစ်ခုလုံး မဟုတ်ပါဘူး။

### ဥပမာ

```python
password = "1234"

# Check if the password matches
if password == "admin123":
 print("Access granted")
else:
 print("Access denied")

print("Login attempt finished")
```

```
Access denied
Login attempt finished
```

`password == "admin123"` က `False` ဖြစ်လို့ `else` block ကို သွားအလုပ်လုပ်ပါတယ်။

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

ATM စက်တို့၊ login system တို့မှာ မှားတဲ့အခါ အသုံးပြုသူကို အသိပေးဖို့ လိုအပ်ပါတယ်။ `else` က ဒီလို "မှားတဲ့ လမ်းကြောင်း" အတွက် အဖြေရှိနေစေပါတယ်။

## Topic 3 — elif Statement

### ဘာကို ဆိုလိုတာလဲ

`elif` ဆိုတာ "else if" ရဲ့ တိုချုံးထားတာပါ။ Condition အများအတွက် အဆင့်ဆင့် စစ်ချင်တဲ့အခါ သုံးပါတယ်။

### ဘာကြောင့်လဲ

ရွေးချယ်စရာ သုံးခုထက် များနေရင် `if` တစ်ခုတည်းနဲ့ ရှုပ်ထွေးသွားပါတယ်။ ဥပမာ— အပူချိန်အလိုက် icon သုံးမျိုး ပြချင်ရင် `elif` က ရှင်းလင်းတဲ့ နည်းလမ်း ဖြစ်ပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Python က `if` condition ကို အရင်စစ်ပါတယ်။ မှားရင် ပထမ `elif` ကို စစ်ပါတယ်။ အဲဒါလည်း မှားရင် နောက်ထပ် `elif` ဆက်စစ်ပါတယ်။ ပထမဆုံး `True` ဖြစ်တဲ့ condition ရှိရင် အဲဒီ block ပဲ အလုပ်လုပ်ပြီး ကျန်တာတွေကို ကျော်ပါတယ်။ အားလုံးမှားရင် `else` block က အလုပ်လုပ်ပါတယ်။

### ဥပမာ

```python
temperature = 15

# Decide which icon to show based on temperature
if temperature < 0:
 print("Snow icon")
elif temperature < 20:
 print("Cold icon")
else:
 print("Sunny icon")
```

```
Cold icon
```

`temperature < 0` က `False` ပါ။ ဒါကြောင့် `temperature < 20` ကို စစ်ပါတယ်— `15 < 20` က `True` ပါ။ ဒါကြောင့် "Cold icon" ပဲ ပေါ်ပါတယ်။

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Game တွေမှာ health အလိုက် အခြေအနေ အများအတွက်— "Game Over"၊ "Warning"၊ "Healthy" စတာတွေ ပြရင် `elif` က သေချာရှင်းလင်းတဲ့ နည်းပေးပါတယ်။ AI မှာလည်း input တစ်ခုကို အုပ်စုများအလိုက် ခွဲချင်တဲ့အခါ ဒီပုံစံက အခြေခံ ဖြစ်ပါတယ်။

## အနှစ်ချုပ်

- `if` — condition မှန်ရင် လုပ်
- `else` — မှားရင် လုပ်
- `elif` — condition အများကို အဆင့်ဆင့် စစ်
- Indentation က Python အတွက် သတိထားစရာ အရေးကြီးဆုံးအချက် ဖြစ်ပါတယ်

## ထပ်ဆောင်း လက်တွေ့ ဥပမာများ

### ဥပမာ ၁ — အခြေအနေစစ်ပြီး စိတ်ဝင်စားမှု ပြောင်းခြင်း
if / elif / else သုံးပြီး အသုံးပြုသူ၏ query length အရ စိတ်ဝင်စားမှုနယ်ပယ် ခွဲခြားပုံကို ပြထားပါတယ်။

```python
query = "what is the weather in Yangon today"

if len(query) < 5:
    print("Too short to understand")
elif "weather" in query:
    print("User is asking about weather")
elif "news" in query:
    print("User is asking about news")
else:
    print("General question")
# Expected output: User is asking about weather
```

### ဥပမာ ၂ — အတက်အဆင့် တူညီမှု စစ်ဆေးခြင်း
နှိုင်းယှဉ် operator (==) နဲ့ logical operator (and) သုံးပြီး အောင်မြင်မှုအတက်အဆင့် တူညီမှုကို စစ်ပုံကို ပြထားပါတယ်။

```python
score = 75
streak = 3

if score == 75 and streak == 3:
    print("Exactly at threshold with a streak")
elif score >= 75 or streak >= 5:
    print("Qualified by either condition")
else:
    print("Not qualified yet")
# Expected output: Exactly at threshold with a streak
```

### ဥပမာ ၃ — nested if နဲ့ tool call ဆုံးဖြတ်ခြင်း
nested if သုံးပြီး API key ရှိမရှိ၊ token budget လုံ့လုံ့ရှိမရှိကို အဆင့်ဆင့် စစ်ပြီး tool ခေါ်မလား ဆုံးဖြတ်ပုံကို ပြထားပါတယ်။

```python
has_api_key = True
token_budget = 200
tool_requires = 150

if has_api_key:
    if token_budget >= tool_requires:
        print("Calling weather tool")
    else:
        print("Enough key but not enough budget")
else:
    print("Cannot call tool: missing API key")
# Expected output: Calling weather tool
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ
AI agent တစ်ခုဟာ tool တွေကို ဘယ်အချိန်မှာ ဘယ်လို အခြေအနေတွေ ပြည့်စုံမှ ခေါ်ရမလဲဆိုတာကို အတိအကျ သတ်မှတ်ပေးရပါတယ်၊ ဒါက if / elif / else နဲ့ comparison, logical operator တွေရဲ့ တိုက်ရိုက် အသုံးချမှုပါ။ ဥပမာ — API key ရှိပြီး token budget လုံလောက်မှသာ tool ခေါ်ရမယ်ဆိုတာက nested if နဲ့ ရေးရတဲ့ လော့ဂျစ်အတိအကျ ဖြစ်ပါတယ်။ ဒါမှမဟုတ်ရင် မဖြစ်သင့်တဲ့ အချိန်မှာ tool ခေါ်မိပြီး token နဲ့ ကုန်ကျစရိတ် အလွန်အကျွံ ဖြစ်စေမှာပါ။ ဒါကြောင့် ဒီ conditional အခြေခံတွေကို နားလည်နိုင်ရင် agent တစ်ခုရဲ့ ဆုံးဖြတ်ချက် လမ်းကြောင်းကို မှန်ကန်စွာ ဖန်တီးပေးနိုင်ပါတယ်။
