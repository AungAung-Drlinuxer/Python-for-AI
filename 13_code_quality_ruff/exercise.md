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

**Hints:** PEP 8 အရ operator နှစ်ဖက်မှာ space တစ်ခုစီ ထည့်ရပြီး `def add(a,b)` မှာ parameter အကြား `,` နောက်တွင် space ထည့်ရမည်၊ `c=a+b` နှင့် function ကိုယ်ထည် indentation ကို PEP 8 စည်းမျဉ်း (space ၄ ခု) အတိုင်း စစ်ကြည့်ပါ။

**Expected behavior:** သင်သည် `def add(a,b):` တွင် `,` နောက် space မထည့်ခြင်း၊ `c=a+b` တွင် operator နှစ်ဖက် space မထည့်ခြင်းနှင့် function ကိုယ်ထည် indentation တွင် space ၄ ခုအစား space ၁ ခုသာ သုံးခြင်းဆိုသည့် PEP 8 style ချိုးဖောက်မှု ၃ ခုကို မှန်ကန်စွာ ဖော်ပြနိုင်ရမည်။

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

**Hints:** save လုပ်တိုင်း format လုပ်စေချင်ရင် settings.json ထဲမှာ "editor.formatOnSave" ဆိုတဲ့ option ကို true ထားပါ၊ ဒါမှ Ruff က အလိုအလျောက် ပြင်ပေးမှာ ဖြစ်ပါတယ်။

**Expected behavior:** Save လုပ်လိုက်တာနဲ့ Ruff က code ကို အလိုအလျောက် format လုပ်ပြီး `message = "Hi " + name` လို့ operator ပတ်ပတ် space ထည့်ပေးပြီး၊ `def greet(name):` ရဲ့ အတွင်း part တွေကို indent လုပ်ပေးပြီး `return x * 2` မှာလည်း space ထည့်ပေးကာ function နှစ်ခုကြားမှာ blank line နှစ်ကြောင်း ထည့်ပေးထားတဲ့ ပုံစံအတိုင်း တွေ့ရမှာ ဖြစ်ပါတယ်။

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

**Hints:** function ခေါ်ရန် `def` ရဲ့ နောက်မှာ colon ထည့်ပြီး၊ body အတွင်းရှိ if/else တွေကို space ၄ ချက်နှင့် တိတိကျကျ indent လုပ်ပါ။

**Expected behavior:** သင်ရေးသားသည့် code ကို `ruff format` ဖြင့် run လိုက်သောအခါ မည်သည့် ပြောင်းလဲမှုမှ မဖြစ်ပေါ်ဘဲ၊ `def check_score(score):` အောက်ရှိ `if`/`else` block များနှင့် `return` statement များအားလုံး space ၄ ချက်အတိအကျ indent ဖြစ်နေသည့် version တစ်ခုကို ရရှိရမည်။

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

**Hints:** Ruff က import များကို alphabet စဉ်အတိုင်း အလိုအလျောက် ပြန်စီပေးတဲ့ `isort` rule (I001) ကို အသုံးပြုပါသည် — import order ကို မှားနေမှုကို စစ်ပေးသည်။

**Expected behavior:** Save file ချိန်တွင် Ruff က import များကိ် `import math`, `import os`, `import sys` ဆိုတဲ့ alphabet စဉ်အတိုင်း အလိုအလျောက် ပြန်စီပေးပြီး မှားနေမှုအားလုံး ပြင်သွားသည်ကို မြင်ရမည်။

## ၅ — Line Length စစ်ဆေးပါ

အောက်ပါ code တွင် line တစ်ကြောင်းသည် စာလုံး ၈၈ ထက်ရှည်နေသလား စစ်ပြီး Ruff ပြင်ပေးသည့်ပုံကို လေ့လာပါ။

```python
def build_prompt(system_message, user_message, temperature, max_tokens):
 prompt = "System: " + system_message + " User: " + user_message + " Temp: " + str(temperature) + " Tokens: " + str(max_tokens)
 return prompt
```

**Hint** — Ruff က ရှည်လွန်းသော line ကို ချွင်းပြီး ပြန်ရေးပေးပါလိမ့်မည်။

**မျှော်လင့်ရမည့် အပြုအမူ** — save လုပ်ပြီးလျှင် ရှည်လွန်းသော line များ အလိုအလျောက် ခွဲသွားသည်ကို မြင်ရမည်။

**Hints:** Ruff ကို run လုပ်ရန် `ruff check` ထက် `--fix` option နှင့်အတူ format command ကို အသုံးပြုပါ။

**Expected behavior:** `ruff format` ကို `--fix` နှင့်အတူ run လုပ်ပြီးလျှင် ၈၈ လုံးထက်ရှည်သော `prompt = ...` line သည် ဖတ်ရလွယ်စေရန် ချဲ့ကားချက်များဖြင့် စာလုံး ၈၈ အတွင်း ကျစ်လစ်စွာ ခွဲပေးထားသည်ကို မြင်ရမည်။

## ၆ — AI Agent Prompt Builder ကို Ruff Style ဖြင့် ရေးပါ

တစ်ခါတည်းသော AI agent prompt တည်ဆောက်ပေးသည့် function တစ်ခုရေးပါ။ ပြင်ဆင်ပြီးမှ Ruff extension ဖြင့် အလိုအလျောက် format လုပ်စေပြီး အရင် version နှင့် နှိုင်းယှဉ်ပါ။

**Hint** — prompt တည်ဆောက်ရန် string concatenation (သို့) f-string သုံးပါ။ မသေချာသောနေရာများကို ကြိုတင်မဖြေရှင်းပါ၊ Ruff format လုပ်ပြီးမှ ကြည့်ပါ။

**မျှော်လင့်ရမည့် အပြုအမူ** — function တစ်ခု အလုပ်လုပ်ရမည် (prompt တစ်ခု return ပေးရမည်)၊ ထို့နောက် Ruff က code ကို သန့်ရှင်းအဆင်ပြေသွားစေရမည်။

**Hints:** f-string ဖြင့် prompt ကိုတည်ဆောက်ပြီး VS Code ရှိ Ruff extension ကို `Shift+Alt+F` ဖြင့် format လုပ်ကြည့်ပါ၊ format မလုပ်ခင် မိမိရေးထားသော code ကို မပြင်ပါနှင့်။

**Expected behavior:** f-string ဖြင့်ရေးထားသော prompt တည်ဆောက်သည့ function တစ်ခု run လိုက်သည့်အခါ AI agent အတွက် အသုံးဝင်သော prompt စာသားတစ်ခု return ပြန်ရမည်ဖြစ်ပြီး၊ `Shift+Alt+F` ဖြင့် Ruff format လုပ်ပြီးသောအခါ code သည် စနစ်တကျ စီစဉ်သည့်ပုံစံသို့ ပြောင်းလဲသွားပြီး အမှားရှာခြင်း (lint) ပြဿနာများ မရှိတော့သည်ကို ဖန်တီးသူ မြင်ရမည်။

