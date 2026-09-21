# Modern Python — uv Package Manager

## Topic 1: uv ဆိုတာ ဘာလဲ

### ဘာကို ဆိုလိုတာလဲ

`uv` ဆိုတာ Python package manager အသစ်တစ်ခုဖြစ်သည်။ pip နေရာမှာ အသုံးပြုနိုင်သော modern tool တစ်ခုဖြစ်သည်။

### ဘာကြောင့် လဲ

pip က အသုံးပြုခဲ့သည်က ကြာသည်။ ဒါပေမယ့် ပြဿနာတွေ ရှိသည်-

- install လုပ်တာ နှေးသည်
- venv command တွေက ရှုပ်ထွေးသည်
- pip, venv, pip-tools, pyenv စသည့် tool များစွာကို သီးခြားသီးခြား သင်ရသည်
- environment ကို မှားစွာသုံးမိရင် ပျက်စီးလွယ်သည်

`uv` က ဒီပြဿနာတွေကို ဖြေရှင်းပေးသည်။ ၁၀ ဆကနေ ၁၀၀ ဆအထိ မြန်သည်။ Rust ဘာသာနဲ့ ရေးထားသောကြောင့် ဤကဲ့သို့ မြန်သည်။

### ဘယ်လို အလုပ်လုပ်လဲ

`uv` က pip, venv, pip-tools, pyenv တို့ရဲ့ လုပ်ဆောင်ချက်တွေကို tool တစ်ခုတည်းနဲ့ ပေးသည်။ ဆိုလိုတာက tool များစွာ မလိုအပ်တော့ဘဲ `uv` တစ်ခုတည်းနဲ့ လုံလောက်သည်။

### ဥပမာ

pip ခေတ်က လုပ်ရသော command နှင့် `uv` ခေတ်က command ကို နှိုင်းယှဉ်ကြည့်ပါ။

pip ခေတ် (tool များစွာ လိုအပ်သည်):

```bash
# Old way: multiple tools needed
python -m venv .venv          # venv tool for virtual environment
source .venv/bin/activate     # activate manually
pip install requests          # pip for installing packages
```

`uv` ခေတ် (tool တစ်ခုတည်း လုံလောက်သည်):

```bash
# New way: only uv needed
uv init my_project    # create project with everything set up
uv add requests       # install package automatically
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI project တွေမှာ `numpy`, `pandas`, `torch` စသည့် library ကြီးတွေ သုံးရသည်။ pip နဲ့ install လုပ်ရင် မိနစ်ပိုင်းကြာတတ်သည်။ `uv` နဲ့ လုပ်ရင် စက္ကန့်ပိုင်းပဲ ကြာသည်။ အချိန်ကုန် သက်သာပြီး project စတင်တာ ပိုမြန်သည်။

## Topic 2: uv နဲ့ Virtual Environment

### ဘာကို ဆိုလိုတာလဲ

Virtual environment ဆိုတာ project တစ်ခုအတွက် သီးခြားခွဲထားသော Python package စုစည်းရန် နေရာဖြစ်သည်။ Project တစ်ခုနဲ့ တစ်ခု package တွေ မရောပါစေရန် ခွဲထားပေးသည်။

### ဘာကြောင့် လဲ

Package တွေကို system အတွင်းမှာ တိုက်ရိုက် install လုပ်ရင် project တွေ အားလုံး ဆိုင်ရင် ပြဿနာ ဖြစ်သည်။ Project A မှာ `numpy` version ၁ သုံးပြီး Project B မှာ version ၂ သုံးချင်ရင် conflict ဖြစ်သည်။ Virtual environment က ဒီပြဿနာကို ဖြေရှင်းပေးသည်။

pip ခေတ်မှာ venv command တွေက ရှုပ်ထွေးသည်။ Windows, Mac, Linux မှာ command တွေ မတူဘဲ လူသစ်တွေ မှားလွယ်သည်။ `uv` က ဒါကို ရိုးရိုးသွေးသွေး ဖြစ်စေသည်။

### ဘယ်လို အလုပ်လုပ်လဲ

`uv` မှာ project ဖန်တီးတဲ့အခါ virtual environment ကို အလိုအလျောက် ဖန်တီးပေးသည်။ လူသူ သက်သက် `activate` လုပ်စရာ မလိုဘူး။ `uv run` command နဲ့ ချက်ချင်း run လို့ရသည်။

### ဥပမာ

```bash
# uv creates a project with a virtual environment automatically
uv init my_ai_project
cd my_ai_project

# uv add installs packages into the project's environment
uv add numpy

# uv run executes the script inside the environment
uv run main.py
```

Project folder အတွင်းမှာ မြင်ရမည့် file တွေ:

```
my_ai_project/
├── .python-version    # Python version for this project
├── main.py            # Main script
├── pyproject.toml     # Project settings and dependencies
└── .venv/             # Virtual environment (created automatically)
```

pip နဲ့ နှိုင်းယှဉ်ရင် environment ထဲ activate ဝင်ဖို့၊ ပြီးရင် install လုပ်ဖို့ အဆင့်တွေ များသည်။ `uv` မှာတော့ အဆင့်တွေ လျှော့သွားသည်။

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI project တွေမှာ library version တွေ အရေးကြီးသည်။ Environment တစ်ခု ပျက်ရင် model training တစ်ခုလုံး ရပ်တန့်နိုင်သည်။ `uv` ရဲ့ ရိုးရှင်းတဲ့ environment စနစ်က ဒီအန္တရာယ်ကို လျှော့ချပေးသည်။

## Topic 3: Complete Setup Workflow

### ဘာကို ဆိုလိုတာလဲ

Complete workflow ဆိုတာ project တစ်ခုကို အစကနေ အဆုံးအထိ တည်ဆောက်ပုံ အဆင့်ဆင့် နည်းလမ်းဖြစ်သည်။

### ဘာကြောင့် လဲ

လူသစ်တွေက project စတင်တဲ့အခါ ဘယ် command ကို ရှေ့သုံးမလဲ၊ ဘယ် file တွေ ဖန်တီးမလဲ မသိတတ်ကြ။ စဉ်းစားရမည့်အရာ များလွန်းသည်။ Standard workflow တစ်ခု ရှိရင် တွေးစရာ လျှော့ပြီး project ကို မြန်မြန် စတင်နိုင်သည်။

### ဘယ်လို အလုပ်လုပ်လဲ

Workflow က အောက်ပါအတိုင်း ဖြစ်သည်-

1. `uv init` နဲ့ project အသစ် ဖန်တီးသည်
2. `uv add` နဲ့ လိုအပ်တဲ့ package တွေ ထည့်သည်
3. code ရေးသည်
4. `uv run` နဲ့ လုပ်ငန်းကို လုပ်ဆောင်သည်

### ဥပမာ

ပထမဆုံး project တစ်ခု ဖန်တီးကြည့်ပါ။

```bash
# Step 1: create a new project
uv init hello_ai
cd hello_ai

# Step 2: add a package we need
uv add rich

# Step 3: write code in main.py
# Step 4: run it
uv run main.py
```

`main.py` အတွင်း ရေးရမည့် code ဥပမာ:

```python
# main.py
# This script prints a formatted welcome message using the rich library
from rich import print

# Print a colorful message
print("[bold green]Hello from my first uv project![/bold green]")
# Expected output: a bold green greeting message in the terminal
```

Run လုပ်ပြီးရင် terminal မှာ အစိမ်းရောင် စာသား မြင်ရမည်။ အချက်အပြုးက `rich` package ကို `uv add` နဲ့ ထည့်ပြီးမှ သုံးလို့ရသည် ဆိုတာပင်။

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI field မှာ project အသစ်တွေ မကြာခဏ စတင်ရသည်။ Idea တစ်ခု စမ်းကြည့်ချင်တဲ့အခါ လူမှန် အချိန်မှန် စတင်နိုင်ရင် အရေးကြီးသည်။ `uv` workflow က project setup ကို စက္ကန့်ပိုင်းအတွင်း ပြီးစေသည်။ ဒါက AI developer တစ်ယောက်အတွက် ကျွမ်းကျင်မှု တစ်ခုပင်။

## အနှစ်ချုပ်

- `uv` က pip ထက် ၁၀ ဆကနေ ၁၀၀ ဆ မြန်သော modern package manager ဖြစ်သည်
- Rust နဲ့ ရေးထားပြီး pip, venv, pip-tools, pyenv တို့ကို အစားထိုးသည်
- Virtual environment ကို အလိုအလျောက် စီမံပေးသည်
- `uv init` -> `uv add` -> `uv run` workflow က project စတင်ရာကို ရိုးရိုးသွေးသွေး ဖြစ်စေသည်
