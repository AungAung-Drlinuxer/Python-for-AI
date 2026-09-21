# လေ့ကျင့်ခန်းများ — Formatting with Ruff

## ၁ — Style ပြဿနာများကို မျက်စိဖြင့် ရှာပါ

အောက်ပါ code တွင် PEP 8 style ချိုးဖောက်မှု ၃ ခုရှိသည်။ သင်ကိုယ်တိုင် ရှာဖွေပြီး မှတ်တမ်းတင်ပါ။

```python
def add(a,b):
    c=a+b
    return c
```

**Hint** — operator ပတ်ဝန်းကျင် space များနှင့် function parameter ကြား space ကို ကြည့်ပါ။

**မျှော်လင့်ရမည့် အပြုအမူ** — space ၂ ခု စသည့် ချိုးဖောက်မှု ၃ ခုကို ဖော်ပြနိုင်ရမည်။

## ၂ — Ruff ဖြင့် Format လုပ်ပြီး နှိုင်းယှဉ်ပါ

VS Code တွင် Ruff extension ထည့်ပြီး Format On Save ဖွင့်ပါ။ ထို့နောက် အောက်ပါ code ကို file ထဲ save လုပ်ကာ Ruff ပြင်ပေးသည့် ပုံကို လေ့လာပါ။

```python
def greet(name):
    message="Hi "+name
    return message
def double(x):
    return x*2
```

**Hint** — save လုပ်တိုင်း format လုပ်စေရန် settings မှာ "editor.formatOnSave": true ဟု သတ်မှတ်ပါ။

**မျှော်လင့်ရမည့် အပြုအမူ** — save လုပ်လိုက်သည်နှင့် operator ပတ်ပတ် space များထည့်ပြီး function နှစ်ခုကြား blank line နှစ်ကြောင်း ထွက်လာရမည်။

## ၃ — Indent ၄ ခုနှင့် Function ခွဲခြားခြင်း

အောက်ပါ code ကို PEP 8 indentation rule (space ၄ ခု) အတိုင်း ကိုယ်တိုင် ရေးပြင်ပါ။

```python
def check_score(score):
    if score >= 90:
        return "Excellent"
    else:
        return "Keep learning"
```

**Hint** — Ruff format လုပ်ပြီး သင်ရေးသည့် version နှင့် တူမတူ နှိုင်းယှဉ်ကြည့်ပါ။

**မျှော်လင့်ရမည့် အပြုအမူ** — သင့်ရေးသည့် code မှာ Ruff format လုပ်ထားသည့် code နှင့် တူညီရမည်။

## ၄ — Import Sorting စစ်ဆေးပါ

အောက်ပါ code ကို Ruff extension ထည့်ထားသည့် VS Code ထဲတွင် ဖွင့်ပြီး import များ အစီအစဉ်ပြောင်းသွားပုံကို လေ့လာပါ။

```python
import sys
import os
import math

result = math.sqrt(16)
print(result)
print(os.name)
print(sys.version)
```

**Hint** — import များကို alphabet အလိုက် စီပေးခြင်းကို Ruff က လုပ်ပေးသည်။

**မျှော်လင့်ရမည့် အပြုအမူ** — import များက os, sys စသည့် စံစဉ်အတိုင်း ပြန်စီသွားသည်ကို မြင်ရမည်။

## ၅ — Line Length စစ်ဆေးပါ

အောက်ပါ code တွင် line တစ်ကြောင်းသည် စာလုံး ၈၈ ထက်ရှည်နေသလား စစ်ပြီး Ruff ပြင်ပေးသည့်ပုံကို လေ့လာပါ။

```python
def build_prompt(system_message, user_message, temperature, max_tokens):
    prompt = "System: " + system_message + " User: " + user_message + " Temp: " + str(temperature) + " Tokens: " + str(max_tokens)
    return prompt
```

**Hint** — Ruff က ရှည်လွန်းသော line ကို ချွင်းပြီး ပြန်ရေးပေးပါလိမ့်မည်။

**မျှော်လင့်ရမည့် အပြုအမူ** — save လုပ်ပြီးလျှင် ရှည်လွန်းသော line များ အလိုအလျောက် ခွဲသွားသည်ကို မြင်ရမည်။

## ၆ — AI Agent Prompt Builder ကို Ruff Style ဖြင့် ရေးပါ

တစ်ခါတည်းသော AI agent prompt တည်ဆောက်ပေးသည့် function တစ်ခုရေးပါ။ ပြင်ဆင်ပြီးမှ Ruff extension ဖြင့် အလိုအလျောက် format လုပ်စေပြီး အရင် version နှင့် နှိုင်းယှဉ်ပါ။

**Hint** — prompt တည်ဆောက်ရန် string concatenation (သို့) f-string သုံးပါ။ မသေချာသောနေရာများကို ကြိုတင်မဖြေရှင်းပါ၊ Ruff format လုပ်ပြီးမှ ကြည့်ပါ။

**မျှော်လင့်ရမည့် အပြုအမူ** — function တစ်ခု အလုပ်လုပ်ရမည် (prompt တစ်ခု return ပေးရမည်)၊ ထို့နောက် Ruff က code ကို သန့်ရှင်းအဆင်ပြေသွားစေရမည်။
