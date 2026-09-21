# လက်တွေ့ လေ့ကျင့်ခန်းများ — uv Package Manager

ဒီလေ့ကျင့်ခန်းတွေကို terminal ထဲမှာ တိုက်ရိုက် လုပ်ဆောင်ပါ။ အလွယ်ကနေ ခက်ခဲသို့ စီစဉ်ထားသည်။

## လေ့ကျင့်ခန်း ၁ — uv install status စစ်ဆေးခြင်း

Terminal ထဲမှာ `uv --version` command ကို ရိုက်ပါ။

**Task:** `uv` ထည့်သွင်းထားမထား စစ်ဆေးပြီး version number ကို မြင်ရစေပါ။

**Hints:** command တစ်ခုတည်း ရိုက်ရုံပါ။ version number တစ်ခု ပေါ်လာရင် အောင်မြင်သည်။

**Expected behavior:** Terminal မှာ `uv x.x.x` ပုံစံနဲ့ version ပေါ်လာမည်။

## လေ့ကျင့်ခန်း ၂ — Project အသစ် ဖန်တီးခြင်း

`uv init first_project` command နဲ့ project အသစ်တစ်ခု ဖန်တီးပါ။

**Task:** Project ဖန်တီးပြီးရင် folder ထဲဝင်ပြီး ဘယ် file တွေ ပေါ်လာလဲ ကြည့်ပါ။

**Hints:** `cd first_project` နဲ့ ဝင်ပါ။ ပြီးရင် `ls` (Windows မှာ `dir`) နဲ့ ကြည့်ပါ။

**Expected behavior:** `main.py` နဲ့ `pyproject.toml` file တွေ မြင်ရမည်။

## လေ့ကျင့်ခန်း ၃ — Package ထည့်ပြီး Run လုပ်ခြင်း

**Task:** `first_project` ထဲမှာ `rich` package ကို ထည့်ပါ။ ပြီးရင် `main.py` ကို ပြင်ပြီး အောက်ပါ code ထည့်ပါ၊ `uv run main.py` နဲ့ လည်ပတ်စေပါ။

**Hints:** `uv add rich` ကို အရင် ရိုက်ပါ။ ပြီးမှ `main.py` ကို ပြင်ပါ။

```python
# main.py
# Import the rich library for colorful output
from rich import print

# Print a styled message
print("[bold blue]My uv project works![/bold blue]")
```

**Expected behavior:** Terminal မှာ အပြာရောင် bold စာသား မြင်ရမည်။

## လေ့ကျင့်ခန်း ၄ — Project Structure မှတ်တမ်းတင်ခြင်း

**Task:** လေ့ကျင့်ခန်း ၃ အပြီးမှာ `pyproject.toml` file ကို ဖွင့်ကြည့်ပါ။ `rich` ရဲ့ အမည် ဘယ်နေရာမှာ ရောင်းနေလဲ မှတ်ပါ။

**Hints:** `pyproject.toml` ကို text editor နဲ့ ဖွင့်ပါ။ `dependencies` section ကို ရှာပါ။

**Expected behavior:** `dependencies` list ထဲမှာ `rich` ဆိုတဲ့ စာသား တွေ့ရမည်။

## လေ့ကျင့်ခန်း ၅ — AI Project Setup

**Task:** `ai_starter` ဆိုတဲ့ project အသစ် ဖန်တီးပါ။ `numpy` package ကို ထည့်ပါ။ ပြီးရင် `main.py` ကို အောက်ပါ code နဲ့ အစားထိုးပြီး run ပါ။

**Hints:** လေ့ကျင့်ခန်း ၃ လိုပဲ `uv add numpy` နဲ့ ထည့်ပါ။

**Expected behavior:** Terminal မှာ array ၏ ပျမ်းမျှတန်ဖိုး ပေါ်လာမည်။

## လေ့ကျင့်ခန်း ၆ — Full Workflow ကို ကိုယ့်ကိုယ်ကိုယ် စမ်းခြင်း

**Task:** အခြေအနေအလိုက် ကိုယ်ပိုင် project တစ်ခု ကိုယ့်ကိုယ်ကိုယ် ဖန်တီးပါ။ နာမည်ကို ကြိုက်တဲ့ နာမည်ပေးပါ၊ package တစ်ခု ရွေးပြီး ထည့်ပါ၊ ရိုးရှင်းတဲ့ code တစ်ခု ရေးပြီး run ပါ။

**Hints:** Workflow ကို မမေ့ပါနဲ့ — `uv init` -> `uv add` -> code ရေး -> `uv run`။

**Expected behavior:** Project တစ်ခု ဖန်တီးပြီး ကိုယ်ရေးတဲ့ code က terminal မှာ အလုပ်လုပ်ရမည်။
