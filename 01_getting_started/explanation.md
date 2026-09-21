# Getting Started — Environment Setup (ရှင်းလင်းချက်)

## ၁။ Python ဆိုတာ ဘာလဲ

**ဘာကို ဆိုလိုတာလဲ** — Python ဆိုသည်မှာ programming language တစ်မျိုးဖြစ်ပြီး လူသားဖတ်နိုင်တဲ့ ရိုးရှင်တဲ့ ဝါကျဖြင့် ရေးနိုင်သော ဘာသာစကားဖြစ်သည်။

**ဘာကြောင့် လဲ** — AI နယ်ပယ်မှာ Python က အသုံးအများဆုံး ဘာသာစကားဖြစ်သည်။ Code ရေးရလွယ်ကူပြီး data နဲ့ အလုပ်လုပ်ရန် အသင့်ဖြစ်သောကြောင့် ဖြစ်သည်။

**ဘယ်လို အလုပ်လုပ်လဲ** — Python interpreter က ရေးထားတဲ့ code ကို တစ်ကြောင်းချင်း ဖတ်ပြီး ကွန်ပျူတာကို လုပ်ဆောင်ခိုင်းသည်။ ဒါကြောင့် code ရေးပြီးလျှင် ချက်ချင်း run ကြည့်နိုင်သည်။

**ဥပမာ**

```python
# This is our first look at Python code
print("Hello, AI world!")
print("Python is easy to learn")
```

```
Hello, AI world!
Python is easy to learn
```

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — AI library ကြီးတွေဖြစ်တဲ့ NumPy, pandas, scikit-learn တို့အားလုံးက Python အပေါ် အခြေခံကြသည်။ Python နားလည်မှ အဲဒီ library တွေကို အသုံးချနိုင်မည်။

## ၂။ Python Install လုပ်ခြင်း

**ဘာကို ဆိုလိုတာလဲ** — ကွန်ပျူတာထဲမှာ Python interpreter ကို ထည့်သွင်းခြင်းကို install လုပ်ခြင်းဟု ခေါ်သည်။

**ဘာကြောင့် လဲ** — Python code ကို run ရန် interpreter လိုအပ်သည်။ Install မလုပ်ဘဲ Python file တွေကို run လို့ မရပါ။

**ဘယ်လို အလုပ်လုပ်လဲ** —

- **Windows**: python.org ကနေ installer download လုပ်ပြီး "Add Python to PATH" ကို စိတ်ချယ်၍ install လုပ်ရသည်။
- **macOS**: Installer download လုပ်၍ install လုပ်နိုင်သည်။
- **Linux**: များသောအားဖြင့် Python ပါဝင်ပြီးသားဖြစ်သည်။ မပါလျှင် package manager ဖြင့် ထည့်နိုင်သည်။

Install ပြီးလျှင် version ကို စစ်ကြည့်နိုင်သည်:

```bash
python --version
```

```
Python 3.12.4
```

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — Python မှန်ကန်စွာ install ဖြစ်နေမှ နောက်ဆုံး AI tools တွေကို ဆက်လက်အသုံးပြုနိုင်မည်။

## ၃။ VS Code Setup လုပ်ခြင်း

**ဘာကို ဆိုလိုတာလဲ** — VS Code ဆိုသည်မှာ code ရေးရန် အသုံးပြုသော editor (အသေးစား program) တစ်ခုဖြစ်သည်။

**ဘာကြောင့် လဲ** — Notepad နဲ့လည်း code ရေးလို့ ရသော်လည်း VS Code က အမှားရှာပေးခြင်း၊ အရောင်ပြခြင်း၊ Python extension တို့ကြောင့် အလုပ်လွယ်သည်။

**ဘယ်လို အလုပ်လုပ်လဲ** — code.visualstudio.com ကနေ download လုပ်ပြီး install လုပ်သည်။ ထို့နောက် Extensions panel ထဲမှာ "Python" extension ကို ရှာ၍ install လုပ်သည်။ ဒါက VS Code ကို Python editor အဖြစ် ပြောင်းပေးသည်။

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — သင်ခန်းစာအားလုံးကို VS Code အသုံးပြု၍ လေ့လာသွားမည်ဖြစ်သဖြင့် ကြိုတင် setup လုပ်ထားခြင်းက အရေးကြီးသည်။

## ၄။ VS Code Workspace ဖန်တီးခြင်း

**ဘာကို ဆိုလိုတာလဲ** — Workspace ဆိုသည်မှာ project တစ်ခုအတွက် သီးသန့် folder တစ်ခုဖြစ်သည်။

**ဘာကြောင့် လဲ** — File တွေကို စနစ်တကျ သီးသန့်ထားလျှင် နောက်ပိုင်း project ကြီးလာသည့်အခါ ရှုပ်ထွေးမှု မရှိပါ။

**ဘယ်လို အလုပ်လုပ်လဲ** — ဥပမာ `python-for-ai` ဟု အမည်ပေးထားသော folder တစ်ခု ဖန်တီးပြီး VS Code ထဲမှာ File > Open Folder ဖြင့် ဖွင့်လိုက်လျှင် ဒီ folder က သင့် workspace ဖြစ်သွားသည်။ Project အသစ်တိုင်းအတွက် folder အသစ် ဖန်တီးသင့်သည်။

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — AI project တစ်ခုစီမှာ data file၊ script၊ model တွေ များလာသဖြင့် အစပျိုးစဉ်ကတည်းက စနစ်တကျ ခွဲခြားထားခြင်းက အချိန်ကယ်ပေးသည်။

## ၅။ ပထမဆုံး Python File

**ဘာကို ဆိုလိုတာလဲ** — Python code တွေကို `.py` extension ပါတဲ့ file ထဲမှာ ရေးသောအခါ Python file ဟု ခေါ်သည်။

**ဘာကြောင့် လဲ** — REPL ထဲမှာ ရေးတဲ့ code က ပိတ်လိုက်လျှင် ပျက်သွားသည်။ File ထဲမှာ ရေးလျှင် အချိန်မရွေး ပြန်ဖွင့်၍ run နိုင်သည်။

**ဘယ်လို အလုပ်လုပ်လဲ** — Workspace ထဲမှာ `hello.py` file တစ်ခု ဖန်တီးပြီး code ရေးသည်။ ထို့နောက် terminal ထဲမှာ `python hello.py` ဟု ရိုက်၍ run သည်။

**ဥပမာ**

```python
# Save this as hello.py and run with: python hello.py
name = "AI learner"
print("Hello,", name)
print("Welcome to Python for AI!")
```

```
Hello, AI learner
Welcome to Python for AI!
```

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — AI model တွေကို လေ့ကျင့်သည့် script အားလုံးက Python file တွေဖြစ်သည်။ File ဖန်တီးပြီး run တတ်ရန် အခြေခံကျသည်။

## ၆။ Virtual Environment

**ဘာကို ဆိုလိုတာလဲ** — Virtual environment ဆိုသည်မှာ project တစ်ခုအတွက် သီးသန့်ခွဲထားသော Python environment ဖြစ်သည်။

**ဘာကြောင့် လဲ** — Project နှစ်ခုက package version မတူညီတဲ့ အခါ တစ်ခုနဲ့တစ်ခု ထိခိုက်တတ်သည်။ Virtual environment တစ်ခုစီက package တွေကို သီးသန့် သိမ်းထားပေးသဖြင့် ပြဿနာ မဖြစ်ပါ။

**ဘယ်လို အလုပ်လုပ်လဲ** — Terminal ထဲမှာ အောက်ပါ command တွေကို ရိုက်သည်:

```bash
# Create a virtual environment named .venv
python -m venv .venv

# Activate it (Windows)
.venv\Scripts\activate

# Activate it (macOS / Linux)
source .venv/bin/activate
```

Activate ဖြစ်နေလျှင် terminal ရှေ့မှာ `(.venv)` ဟု ပေါ်လာသည်။

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — AI project တစ်ခုစီက ကွဲပြားတဲ့ library version တွေ လိုအပ်တတ်သည်။ Environment ခွဲထားခြင်းက project တွေကို လုံခြုံစေသည်။

## ၇။ Packages နှင့် pip

**ဘာကို ဆိုလိုတာလဲ** — Package ဆိုသည်မှာ အခြားသူများ ရေးထားပြီးသား Python code ပုံစံများဖြစ်ပြီး `pip` က အဲဒီ package တွေကို install လုပ်ပေးသော ကိရိယာဖြစ်သည်။

**ဘာကြောင့် လဲ** — Data စစ်ဆေးခြင်း၊ AI model လေ့ကျင့်ခြင်းစသည့် အလုပ်တွေအတွက် အလွန်အသုံးများသော package တွေက ကြိုတင်ပြီး ရှိနေသည်။ ကိုယ်တိုင် အစကနေ ရေးစရာ မလိုပါ။

**ဘယ်လို အလုပ်လုပ်လဲ** — Virtual environment activate ပြီးနောက် `pip install` ဖြင့် package ထည့်သည်။

```bash
# Install a package
pip install numpy

# List installed packages
pip list
```

**ဥပမာ**

```python
# Use an installed package
import numpy as np

# Create a simple array of numbers
numbers = np.array([1, 2, 3, 4, 5])
print("Sum of numbers:", numbers.sum())
```

```
Sum of numbers: 15
```

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — AI လောကမှာ NumPy, pandas တို့က မရှိမဖြစ် package များဖြစ်သည်။ pip သုံးတတ်ရင် လိုအပ်တဲ့ ကိရိယာအားလုံးကို ယူနိုင်မည်။

## ၈။ Interactive Python (REPL)

**ဘာကို ဆိုလိုတာလဲ** — REPL (Read-Eval-Print Loop) ဆိုသည်မှာ Python command တွေကို တစ်ကြောင်းချင်း ရိုက်၍ ချက်ချင်း အဖြေကြည့်နိုင်သော interactive mode ဖြစ်သည်။

**ဘာကြောင့် လဲ** — File ဖန်တီးရန် မလိုဘဲ ချက်ချင်း စမ်းသပ်နိုင်သဖြင့် လေ့ကျင့်ရန် အကောင်းဆုံးနည်းလမ်းဖြစ်သည်။

**ဘယ်လို အလုပ်လုပ်လဲ** — Terminal ထဲမှာ `python` ဟုသာ ရိုက်လိုက်လျှင် `>>>` ဆိုသော prompt ပေါ်လာသည်။ အဲဒီမှာ code ရိုက်၍ ချက်ချင်း run နိုင်သည်။ ထွက်လိုလျှင် `exit()` ရိုက်သည်။

**ဥပမာ**

```python
>>> 2 + 3
5
>>> "AI" + " learner"
'AI learner'
```

**လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ** — Python feature အသစ်တွေကို အြမန်စမ်းသပ်နိုင်သဖြင့် AI project ရေးနေစဉ် library တွေကို ချက်ချင်း စစ်ကြည့်နိုင်သည်။
