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

# uv ဖြင့် Python စတင်အသုံးပြုခြင်း — စတာမှ-အဆုံး လမ်းညွှန်

## uv ဆိုတာ ဘာလဲ၊ ဘာကြောင့် မြန်လဲ

uv ဆိုတာ Astral အဖွဲ့က ရေးထားတဲ့ Python package နှင့် environment စီမံခန့်ခွဲမှု tool တစ်ခုဖြစ်ပါတယ်။ Rust ဘာသာနဲ့ ရေးထားပြီး traditional pip နဲ့ ယှဉ်ရင် ဆယ်စုံကျော် မြန်စွာ အလုပ်လုပ်ပါတယ်။ မြန်ရတဲ့ အကြောင်းရင်းတွေကတော့ —

၁။ **Rust နဲ့ ရေးထားခြင်း** — compiled language ဖြစ်လို့ CPU resource တွေကို အပြည့်အဝ အသုံးချနိုင်ပြီး pip (Python နဲ့ ရေးထားတာ) ထက် သိသိသာသာ မြန်ပါတယ်။

၂။ **Global cache စနစ်** — package တစ်ခါ download လုပ်ပြီးရင် သက်ဆိုင်ရာ environment တိုင်းမှာ cache ထဲကနေ link လုပ်တာလို့ ဒစ်စက်နေရာလည်း သက်သာပြီး နောက်တစ်ခါ install တွေ အရမ်းမြန်ပါတယ်။

၃။ **Parallel download** — package တွေကို တစ်ချက်တည်း မဟုတ်ပဲ တပြိုင်တည်း စုပေါင်း download လုပ်လို့ နှစ်ဆ သုံးဆ အထိ မြန်ပါတယ်။

၄။ **Resolution algorithm မြန်ခြင်း** — dependency version တွေ ရွေးတဲ့ PubGrub algorithm က dependency conflict တွေကို လျင်မြန်စွာ ဖြေရှင်းပေးပါတယ်။

## အခြေခံ command တွေ

### `uv venv` — virtual environment ဖန်တီးခြင်း

```bash
uv venv
```

project folder ထဲမှာ `.venv` ဆိုတဲ့ virtual environment ဖန်တီးပေးပါတယ်။ Python version သီးသန့် ချင်ရင် —

```bash
uv venv --python 3.12
```

uv က Python interpreter ကိုပါ မသိုလာရင် အလိုအလျောက် download လုပ်ပေးတာကြောင့် Python ကို ကြိုတင် install လုပ်နေစရာ မလိုပါဘူး။

### `uv init` — project အသစ် စတင်ခြင်း

```bash
uv init my-project
cd my-project
```

ဒီ command က `pyproject.toml` နဲ့ `main.py` (သို့) `hello.py` ဖန်တီးပေးပြီး project အခြေခံ ဖိုင်တွေ အလိုအလျောက် ပြင်ဆင်ပေးပါတယ်။ `uv init --package my-project` လို့ ရေးရင် package အနေနဲ့ ဖြန့်ဖြီးနိုင်တဲ့ ဖွဲ့စည်းပုံ (`src/` layout) နဲ့ ဖန်တီးပေးပါတယ်။

### `uv add` — package ထည့်သွင်းခြင်း

```bash
uv add requests
```

package ကို install လုပ်ပြီးသာမက `pyproject.toml` ထဲကိုပါ dependency အနေနဲ့ ရေးသွင်းပေးပြီး `uv.lock` ဖိုင်ကိုလည်း update လုပ်ပေးပါတယ်။ Development အတွက်သာ လိုအပ်တဲ့ package ဆိုရင် —

```bash
uv add --dev pytest
```

### `uv sync` — lock file နဲ့ တူညီအောင် စင်ခြင်း

```bash
uv sync
```

`uv.lock` ဖိုင်ထဲ record လုပ်ထားတဲ့ version တွေအတိုင်း environment ကို အတိအကျ ပြန်တည်ဆောက်ပေးပါတယ်။ Team တစ်ခုလုံးက တူညီတဲ့ version တွေ သုံးနိုင်အောင် အာမခံပေးတဲ့ command ဖြစ်ပါတယ်။

### `uv run` — environment အတွင်းမှာ လည်ပတ်ခြင်း

```bash
uv run main.py
```

virtual environment ကို ကြိုတင် activate လုပ်နေစရာ မလိုပဲ script ကို တိုက်ရိုက် run ပေးပါတယ်။ Environment မရှိသေးရင် အလိုအလျောက် sync လုပ်ပေးပါတယ်။

## `pyproject.toml` ဖိုင် ဖွဲ့စည်းပုံ

`uv init` လုပ်ပြီးရင် ဒီလို `pyproject.toml` ရပါလိမ့်မယ် —

```toml
[project]
name = "my-project"
version = "0.1.0"
description = "A simple demo project"
requires-python = ">=3.12"
dependencies = [
    "requests>=2.32.0",
]

[dependency-groups]
dev = [
    "pytest>=8.0.0",
]
```

အပိုင်းတွေရဲ့ အဓိပ္ပာယ်က —

- `name`, `version`, `description` — project အချက်အလက်များ
- `requires-python` — လိုအပ်တဲ့ Python version အနိမ့်ဆုံး
- `dependencies` — production မှာ လိုအပ်တဲ့ package များ
- `[dependency-groups]` — development အတွက်သာ သုံးတဲ့ package များ (pytest 처럼)

## စတာမှ-အဆုံး Project Workflow

အောက်မှာ တကယ့် project တစ်ခုကို uv နဲ့ ဖန်တီးပြီး run အထိ အဆင့်ဆင့် ပြထားပါတယ်။

**အဆင့် ၁ — Project ဖန်တီးခြင်း**

```bash
uv init price-checker
cd price-checker
```

**အဆင့် ၂ — လိုအပ်တဲ့ package ထည့်ခြင်း**

```bash
uv add requests
uv add --dev pytest
```

**အဆင့် ၃ — Code ရေးခြင်း**

`main.py` ကို ဖွင့်ပြီး ဒီ code ရေးပါ —

```python
import requests

def fetch_price(symbol: str) -> float:
    # Fetch a fake stock price from a public API
    response = requests.get(f"https://httpbin.org/json")
    response.raise_for_status()
    data = response.json()
    return data.get("slideshow", {}).get("slidecount", 0)

if __name__ == "__main__":
    count = fetch_price("AAPL")
    print(f"Slide count received: {count}")
```

**အဆင့် ၄ — Run ခြင်း**

```bash
uv run main.py
```

**အဆင့် ၅ — Test ရေးပြီး run ခြင်း**

`test_main.py` ဆိုတဲ့ ဖိုင် ဖန်တီးပြီး —

```python
from main import fetch_price

def test_fetch_price_returns_number():
    result = fetch_price("AAPL")
    assert isinstance(result, int)
```

ပြီးရင် —

```bash
uv run pytest
```

**အဆင့် ၆ — Git မှာ မျှဝေခြင်း**

`uv.lock` ဖိုင်ကို commit လုပ်ပါ — ဒါဆို အဖွဲ့ဝင်တိုင်းက `uv sync` နဲ့ တူညီတဲ့ environment ရနိုင်ပါတယ်။

**အဆင့် ၇ — Git clone ပြီးတဲ့အခါ အခြားသူတွေ လုပ်ရမယ့်အရာ**

```bash
git clone <repo-url>
cd price-checker
uv sync
uv run main.py
```

## ထပ်ဆောင်း လက်တွေ့ ဥပမာများ

### ဥပမာ ၁ — pyproject.toml ဖိုင်ကို Python နဲ့ ဖတ်ကြည့်ခြင်း

ဥပမာဒီ code က `pyproject.toml` ထဲက project နာမည်နဲ့ dependency စာရင်းကို Python standard library သာ သုံးပြီး ထုတ်ပြနိုင်ကြောင်း ပြသထားပါတယ်။

```python
import tomllib

with open("pyproject.toml", "rb") as f:
    data = tomllib.load(f)

print(data["project"]["name"])
for dep in data["project"]["dependencies"]:
    print(f"- {dep}")
# Expected output:
# price-checker
# - requests>=2.32.0
```

### ဥပမာ ၂ — uv နဲ့ install လုပ်ထားတဲ့ package version စစ်ခြင်း

ဥပမာဒီ code က installed package တွေကို `importlib.metadata` နဲ့ စစ်ပြီး version တူမတူ တွေ့နိုင်ကြောင်း ပြသထားပါတယ်။

```python
from importlib.metadata import version

for pkg in ["requests", "pytest"]:
    try:
        print(f"{pkg}: {version(pkg)}")
    except Exception:
        print(f"{pkg}: not installed")
# Expected output:
# requests: 2.32.3
# pytest: 8.3.4
```

### ဥပမာ ၃ — subprocess နဲ့ uv sync လုပ်ပြီး lock file ရှိ/မရှိ စစ်ခြင်း

ဥပမာဒီ code က `uv.lock` ဖိုင် ရှိမရှိ စစ်ပြီး မရှိရင် `uv sync` command ကို Python ကနေ ခေါ် run နိုင်ကြောင်း ပြသထားပါတယ်။

```python
import subprocess
from pathlib import Path

if Path("uv.lock").exists():
    print("Lock file found, skipping sync")
    # Expected output: Lock file found, skipping sync
else:
    result = subprocess.run(["uv", "sync"], capture_output=True, text=True)
    print("Sync finished with return code:", result.returncode)
    # Expected output: Sync finished with return code: 0
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

uv က command တွေကို ရိုးရိုးလေး ဖန်တီးပေးပြီး မြန်စွာ အလုပ်လုပ်တာကြောင့် ကျောင်းသားတွေအတွက် setup အဆင့်တွေကို လျှော့ချပေးပြီး code ရေးတာနဲ့ ပိုမိုအာရုံစိုက်နိုင်စေပါတယ်။ `pyproject.toml` နဲ့ `uv.lock` ဖိုင်တွေက project ရဲ့ dependency တွေကို စာရွက်စာတမ်းအသွင် မှတ်တမ်းတင်ထားတာမလို့ team တစ်ခုလုံးရဲ့ environment တူညီမှုကို အာမခံပေးပါတယ်။ `uv sync` လို command တွေက CI/CD pipeline ထဲမှာပါ အလွယ်တကူ သုံးနိုင်တာကြောင့် production deploy အထိ တစ်ပြေးညီ ဖြစ်စေပါတယ်။ ဒီ workflow က pip, venv, pip-tools စတဲ့ tool အများအပြားရဲ့ လုပ်ဆောင်ချက်တွေကို tool တစ်ခုတည်းနဲ့ အစားထိုးနိုင်တာကြောင့် အစပြုသူတွေအတွက် ရှုပ်ထွေးမှု သိသိသာသာ လျှော့နိုင်ပါတယ်။
