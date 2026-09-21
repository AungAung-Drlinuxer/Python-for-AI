# လက်တွေ့ လေ့ကျင့်ခန်းများ — Environment Setup

## ၁။ Python Version စစ်ဆေးခြင်း

**Task** — Terminal (Windows: Command Prompt, macOS/Linux: Terminal) ဖွင့်ပြီး Python version ကို စစ်ဆေးပါ။

**Hint** — `python --version` သို့မဟုတ် `python3 --version` ကို ရိုက်ကြည့်ပါ။

**Expected behavior** — `Python 3.x.x` ပုံစံ အရေအတွက် တစ်ခု ပေါ်လာပါမည်။ မပေါ်လျှင် Python ကို install လုပ်ရန် လိုအပ်သည်။

## ၂။ ပထမဆုံး Python File ရေးခြင်း

**Task** — VS Code ထဲမှာ `hello.py` file တစ်ခု ဖန်တီးပြီး ကိုယ့်နာမည်ကို နှုတ်ခေါ်သည့် code ရေးပါ။ ထို့နောက် terminal ကနေ run ပါ။

**Hint** — `print()` function ကို အသုံးပြုပါ။ Run ရန် `python hello.py` ရိုက်ပါ။

**Expected behavior** — Terminal ထဲမှာ ကိုယ့်နာမည်နှင့်အတူ နှုတ်ခေါ်စာ တစ်ကြောင်း ပေါ်လာပါမည်။

## ၃။ ကိုယ်ပိုင် AI Workspace ဖန်တီးခြင်း

**Task** — `my-ai-workspace` ဟု အမည်ပေးထားသော folder တစ်ခု ဖန်တီးပြီး VS Code ဖြင့် ဖွင့်ပါ။ ထို့နောက် အထဲတွင် `intro.py` file ရေးပြီး ကိုယ်တော့် AI လေ့လာရန် ရည်မှန်းချက် ၃ ကြောင်း `print()` ဖြင့် ရေးပါ။

**Hint** — VS Code မှာ File > Open Folder ကို အသုံးပြုပါ။ `print()` ကို ၃ ကြိမ် ရိုက်ပါ။

**Expected behavior** — `python intro.py` run လိုက်လျှင် ရည်မှန်းချက် ၃ ကြောင်း ထွက်လာပါမည်။

## ၄။ Virtual Environment ဖန်တီးပြင့် Activate လုပ်ခြင်း

**Task** — Workspace ထဲမှာ `.venv` ဟု အမည်ပေးထားသော virtual environment တစ်ခု ဖန်တီးပြီး activate လုပ်ပါ။

**Hint** — `python -m venv .venv` ဖြင့် ဖန်တီးပါ။ Windows မှာ `.venv\Scripts\activate` ၊ macOS/Linux မှာ `source .venv/bin/activate` ဖြင့် activate လုပ်ပါ။

**Expected behavior** — Terminal ရှေ့မှာ `(.venv)` ဟု ပေါ်လာပြီး သင့် environment အသုံးပြုရန် အသင့်ဖြစ်ပါမည်။

## ၅။ Package Install လုပ်ပြီး အသုံးပြုခြင်း

**Task** — Activate ပြီး environment ထဲမှာ `numpy` package ကို install လုပ်ပါ။ ထို့နောက် `sum.py` file ဖန်တီးပြီး numpy ဖြင့် ကိန်းညွှန်း list တစ်ခု၏ ပမာဏ တွက်ပါ။

**Hint** — `pip install numpy` ဖြင့် install လုပ်ပါ။ `import numpy as np` ဖြင့် သွင်းပြီး `np.array()` နှင့် `.sum()` ကို အသုံးပြုပါ။

**Expected behavior** — `python sum.py` run လိုက်လျှင် ကိန်းများ၏ ပမာဏ တစ်ခု ထွက်လာပါမည်။

## ၆။ AI Agent အတွက် ကြိုတင်စစ်ဆေးမှု Script

**Task** — AI agent တစ်ခု တည်ဆောက်ရန် အစီအစဉ်ရှိသူတစ်ဦးအဖြစ် ဖြင့် `check_setup.py` file တစ်ခု ရေးပါ။ ဒီ script က Python ကို အသုံးပြု၍ ပြုလုပ်ရမည့် အဆင့်များကို တစ်ဆင့်ချင်း ရှင်းပြပါမည် (ဥပမာ — environment ရွေးချယ်ခြင်း၊ tool တွေ စစ်ဆေးခြင်း၊ data ပြင်ခြင်း၊ model လေ့ကျင့်ခြင်း)။

**Hint** — `print()` ကို အဆင့်ဆင့် အသုံးပြုပြီး အဆင့်တိုင်းရဲ့ နံပါတ်ကို ထည့်ပါ။

**Expected behavior** — Run လိုက်လျှင် AI agent တည်ဆောက်ရန် အဆင့်များကို စနစ်တကျ ရှင်းပြတဲ့ အထွက်တွေ ပေါ်လာပါမည်။
