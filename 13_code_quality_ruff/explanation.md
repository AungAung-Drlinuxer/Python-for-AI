# Formatting with Ruff — Lint & Format

## ၁။ Ruff ဆိုတာ ဘာလဲ

### ဘာကို ဆိုလိုတာလဲ

Ruff ဆိုသည်မှာ Python code အတွက် ခေတ်ပြောင်းသော all-in-one tool တစ်ခုဖြစ်သည်။ ၎င်းသည် linting၊ formatting နှင့် import sorting ဆိုသည့် လုပ်ငန်းသုံးမျိုးကို တစ်ခုတည်းနှင့် လုပ်ဆောင်ပေးသည်။ ယခင်က Pylint, Black, isort ဆိုသည့် tool သုံးခုကို သီးသန့်သုံးခဲ့ရသော်လည်း Ruff တစ်ခုတည်းက ၎င်းတို့၏နေရာကို အစားထိုးနိုင်သည်။

### ဘာကြောင့် လဲ

Python code ရေးရာတွင် တစ်ယောက်နှင့်တစ်ယောက် ရေးပုံရေးနည်းမတူနိုင်ပါ။ ဥပမာ — တစ်ယောက်က space တစ်ခုထည့်ရေး၊ တစ်ယောက်က မထည့်ရေးသည့်အခါ code ဖတ်ရခက်လာသည်။ Ruff က ၎င်းပြဿနာများကို အလိုအလျောက် ဖြေရှင်းပေးသည်။

### ဘယ်လို အလုပ်လုပ်လဲ

Ruff က code ဖိုင်တစ်ခုကို ဖတ်၍ PEP 8 style rules များအတိုင်း ရှိ၊မရှိ စစ်ဆေးသည်။ ပြဿနာရှိပါက linting ဖြင့် အကြောင်းပြပြီး formatting ဖြင့် အလိုအလျောက် ပြင်ပေးသည်။

### ဥပမာ

```python
# Before Ruff formatting (messy style)
def add(a,b):
    return a+b
```

```python
# After Ruff formatting (clean PEP 8 style)
def add(a, b):
    return a + b
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI project များတွင် code များမှာ ရှည်လျားလာသည်။ Ruff ကိုသုံးခြင်းအားဖြင့် style အတွက် အချိန်မဆုံးရှုံးပါဘဲ logic အပေါ်တွင်သာ အာရုံစူးစိုက်နိုင်သည်။

## ၂။ VS Code ထဲမှာ Ruff Setup လုပ်နည်း

### ဘာကို ဆိုလိုတာလဲ

VS Code editor ထဲတွင် Ruff ကို အသုံးပြုနိုင်ရန် ကြိုတင်ပြင်ဆင်ရသည့် အဆင့်များကို setup ဟုခေါ်သည်။

### ဘာကြောင့် လဲ

Ruff ကို editor နှင့် ချိတ်ဆက်မပေးပါက save လုပ်တိုင်း အလိုအလျောက် format လုပ်ပေးခြင်း မရှိနိုင်ပါ။ Setup ပြုလုပ်ခြင်းအားဖြင့် ရေးလိုက်တိုင်း အလိုအလျောက် သန့်ရှင်းသော code ရရှိမည်။

### ဘယ်လို အလုပ်လုပ်လဲ

အဆင့်သုံးဆင့်ဖြင့် ပြုလုပ်ရမည် —

1. VS Code Extension Marketplace တွင် Astral ရေးသည့် **Ruff** extension ကို install လုပ်ရမည်။
2. VS Code settings တွင် **Format On Save** ကို enable လုပ်ရမည်။
3. Python formatting provider အဖြစ် **Ruff** ကို ရွေးချယ်ရမည်။

### ဥပမာ

settings.json ဖိုင်တွင် ဤသို့ သတ်မှတ်နိုင်သည် —

```json
{
    "editor.formatOnSave": true,
    "[python]": {
        "editor.defaultFormatter": "charliermarsh.ruff"
    }
}
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Setup တစ်ကြိမ်ပြုလုပ်ပြီးပါက နောက်ပိုင်း project တိုင်းတွင် အလိုအလျောက် အကျိုးခံစားရမည်။ Save နှိပ်လိုက်တိုင်း code ညီညွတ်သွားမည်။

## ၃။ Linting — ပြဿနာများ ရှာတွေ့ခြင်း

### ဘာကို ဆိုလိုတာလဲ

Linting ဆိုသည်မှာ code ကို run မလုပ်မီ အမှားနှင့် style ပြဿနာများကို ရှာဖွေစစ်ဆေးခြင်းဖြစ်သည်။ Ruff သည် code ထဲတွင် မလိုအပ်သော variable၊ မသုံးတော့သော import စသည့် ပြဿနာများကို ညွှန်ပြပေးသည်။

### ဘာကြောင့် လဲ

Code run လုပ်မှသာ အမှားကို သိရပါက အချိန်ဆုံးရှုံးသည်။ Linting က save လုပ်စဉ်ပင် ပြဿနာကို အရင်ပြပေးသဖြင့် အချိန်ကုန်သက်သာသည်။

### ဘယ်လို အလုပ်လုပ်လဲ

Ruff က code တစ်ကြောင်းချင်းစီကို rules များနှင့် တိုက်ဆိုင်စစ်ဆေးသည်။ မကိုက်ညီသည်များကို editor ထဲတွင် အဝါရောင် မျဉ်းကြောင်းဖြင့် ပြပေးသည်။

### ဥပမာ

```python
import os   # unused import - Ruff will warn
import math

def area(radius):
    x = 5   # unused variable - Ruff will warn
    return math.pi * radius ** 2

# Expected: Ruff marks the unused import and variable
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI model သို့မဟုတ် agent code ရေးသည့်အခါ မလိုအပ်သော import များကို စက်ရှာပေးသဖြင့် code ပိုမာမလာသည်။

## ၄။ PEP 8 Formatting Rules

### ဘာကို ဆိုလိုတာလဲ

PEP 8 ဆိုသည်မှာ Python code ရေးသည့် စံနှုန်း style လမ်းညွှန်ဖြစ်သည်။ Ruff က ဤ rules များကို အလိုအလျောက် လိုက်နာစေသည် —

- Indent တစ်ခုကို **space ၄ ခု** သုံးရမည်
- Operator များနှစ်ဖက်တွင် space ထည့်ရမည် (ဥပမာ `a + b`)
- Function များကြားတွင် **blank line နှစ်ကြောင်း** ချရမည်
- Line တစ်ကြောင်းသည် စာလုံး **၈၈ အထိ**သာ ရှိရမည်

### ဘာကြောင့် လဲ

စံတစ်ခုတည်းရှိပါက လူတိုင်း code ဖတ်ရလွယ်ကူသည်။ အဖွဲ့လိုက် ရေးသည့်အခါ တစ်ဦးနှင့်တစ်ဦး code ကို လွယ်လင့်တကူ နားလည်နိုင်သည်။

### ဘယ်လို အလုပ်လုပ်လဲ

Save နှိပ်သည့်အခါ Ruff က code တစ်ခုလုံးကို ပြန်ဖတ်၍ PEP 8 rules များအတိုင်း ပြင်ဆင်ပေးသည်။

### ဥပမာ

```python
# Before: style problems
def get_message(name):
    full="Hello, "+name
    return full
def shout( text ):
    return text.upper()
```

```python
# After Ruff formatting: clean PEP 8 style
def get_message(name):
    full = "Hello, " + name
    return full


def shout(text):
    return text.upper()
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI project များတွင် file များစွာဖြင့် ရေးသည့်အခါ style ညီညွတ်မှုက bugs ရှာရာတွင် အထောက်အကူပြုသည်။ Ruff ကိုသုံးခြင်းဖြင့် style ကိစ္စများကို စိတ်မစိုးရဘဲ code logic တစ်ခုတည်းကိုသာ ဦးစားပေးရေးသားနိုင်မည်။
