# Environment & Secrets — အသေးစိတ်ရှင်းပြချက်

ဒီ သင်ခန်းစာမှာ secret data တွေကို လုံခြုံစွာ သိမ်းဆည်းဖို့ environment variable နည်းနဲ့ `.env` file နည်းကို အဆင့်ဆင့် ရှင်းပြပေးပါမယ်။

## ၁။ Secret ကို code ထဲ ဘာကြောင့် မရေးသင့်လဲ

### ဘာကို ဆိုလိုတာလဲ

Secret ဆိုတာက API key၊ password၊ database connection string လိုမျိုး သူများသိခွင့် မရှိသင့်တဲ့ data တွေကို ဆိုလိုပါတယ်။

### ဘာကြောင့်လဲ

Code ထဲ တိုက်ရိုက်ရေးထားရင် အောက်ပါ ပြဿနာတွေ ရှိပါတယ် —

- Code ကို GitHub ဆီတင်ရင် API key ပါတဲ့အတွက် လူအားလုံး မြင်ရပါမယ်။
- Key တစ်ခုပြောင်းချင်ရင် code ထဲ ရောက်သွားပြီး အချိန်ကုန်ပါတယ်။
- Key တစ်ခု leak ဖြစ်သွားရင် account တစ်ခုလုံး အန္တရာယ်ရှိပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Key ကို code ထဲမရေးပဲ **code အပြင်ဘက်**မှာ သိမ်းထားပြီး code က သာမန်နာမည်နဲ့ ဖတ်ယူပါတယ်။ ဒီနည်းကို environment variable လို့ခေါ်ပါတယ်။

### ဥပမာ

မကောင်းတဲ့ နည်း (ဒီလို မလုပ်ပါနဲ့) —

```python
# BAD: never do this
api_key = "sk-abc123-secret-key"
print(api_key)
```

မကောင်းတဲ့ နည်းက key ကို code ထဲ တိုက်ရိုက်ရေးထားတာပါ။ ဒီ file ကို Git ဆီတင်လိုက်တာနဲ့ key က အများသိသွားပါတယ်။

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI project တွေမှာ OpenAI API key တို့လို key တွေက ကုန်ကျစရိတ်နဲ့တွဲထားတာမို့ leak ဖြစ်သွားရင် အခြားသူတွေက သင့် account နဲ့ အသုံးပြုနိုင်ပါတယ်။ ဒါကြောင့် ပထမဆုံး သင်ယုံကြေးရတဲ့ စနစ်ကို အစကတည်းက အသုံးပြုသင့်ပါတယ်။

## ၂။ System Environment Variable

### ဘာကို ဆိုလိုတာလဲ

Environment variable ဆိုတာက operating system (Windows၊ macOS၊ Linux) ရဲ့ အပြင်ဘက်မှာ သိမ်းထားတဲ့ value တစ်ခုပါ။ Program တိုင်းက ဒီ value တွေကို နာမည်နဲ့ ဖတ်ယူနိုင်ပါတယ်။

### ဘာကြောင့်လဲ

Code ထဲ key တိုက်ရိုက်မရေးပဲ OS ထဲ သိမ်းထားရင် code က key ကို မမြင်ရဘဲ value ကိုပဲ သုံးနိုင်လို့ လုံခြုံပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Terminal မှာ variable တစ်ခုသတ်မှတ်ပြီး Python `os.environ` နဲ့ ဖတ်ယူပါတယ်။ Terminal မှာ သတ်မှတ်တဲ့ အခါ —

```bash
export MY_API_KEY="sk-abc123-secret-key"
```

Python ကနေ ဖတ်ယူတဲ့ အခါ —

```python
import os

# Read the environment variable by name
api_key = os.environ.get("MY_API_KEY")
print(api_key)
# Expected output: sk-abc123-secret-key
```

### ဥပမာ

Key ရှိမရှိ စစ်ပြီး သုံးတဲ့ နမူနာ —

```python
import os

# Get the key, return None if it does not exist
api_key = os.environ.get("MY_API_KEY")

if api_key:
    print("API key ready.")
else:
    print("API key not found. Set MY_API_KEY first.")
# Expected output (if set): API key ready.
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

Server ပေါ်မှာ AI service တွေ run တဲ့အခါ ဒီနည်းက အသုံးအများဆုံးပါ။ Server ရဲ့ setting ထဲ သိမ်းလိုက်ရင် code ထဲ key လုံးဝ မပါတော့ပါ။ သို့ပေါင်း terminal ပိတ်သွားရင် ပြန်သတ်မှတ်ရတဲ့ ပြဿနာ ရှိပါတယ်။

## ၃။ `.env` File နဲ့ စီမံခန့်ခွဲနည်း

### ဘာကို ဆိုလိုတာလဲ

`.env` ဆိုတာက `KEY=value` ပုံစံနဲ့ ရေးထားတဲ့ text file တစ်ခုပါ။ Project folder ထဲမှာ သိမ်းပြီး code က ဒီ file ကနေ value တွေ ဖတ်ယူပါတယ်။

### ဘာကြောင့်လဲ

Python project အများစုက `.env` file ကို အသုံးပြုပါတယ် —

- Local development မှာ အလွယ်ကူဆုံး နည်းဖြစ်လို့။
- Project တစ်ခုချင်းစီမှာ key သီးသန့် သိမ်းနိုင်လို့။
- Terminal ပိတ်လို့ variable ပျောက်တာ မရှိလို့။

### ဘယ်လို အလုပ်လုပ်လဲ

ပထမဆုံး `python-dotenv` package ကို install ပါ —

```bash
pip install python-dotenv
```

Project folder ထဲမှာ `.env` file တစ်ခု ဖန်တီးပြီး အောက်ပါအတိုင်း ရေးပါ —

```
OPENAI_API_KEY=sk-abc123-secret-key
DATABASE_URL=postgres://localhost/mydb
```

Python code ထဲမှာ `load_dotenv()` နဲ့ ဖတ်ယူပြီး `os.environ.get()` နဲ့ သုံးပါတယ်။

### ဥပမာ

```python
import os
from dotenv import load_dotenv

# Load all variables from the .env file
load_dotenv()

# Read values like normal environment variables
api_key = os.environ.get("OPENAI_API_KEY")
db_url = os.environ.get("DATABASE_URL")

print("API key:", api_key)
print("Database URL:", db_url)
# Expected output:
# API key: sk-abc123-secret-key
# Database URL: postgres://localhost/mydb
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

LLM နဲ့ AI agent တွေဆောက်တဲ့ project တွေမှာ API key တစ်ခုထက် ပိုသုံးတတ်ပါတယ်။ `.env` file ထဲ စုပြီး သိမ်းထားရင် project တစ်ခုလုံးရဲ့ setting ကို နေရာတစ်ခုတည်းမှာ စီမံနိုင်ပါတယ်။

## ၄။ `.gitignore` နဲ့ ကာကွယ်နည်း

### ဘာကို ဆိုလိုတာလဲ

`.gitignore` ဆိုတာက Git ဆီ မတင်သင့်တဲ့ file တွေရဲ့ စာရင်း သိမ်းတဲ့ file ပါ။

### ဘာကြောင့်လဲ

`.env` file မှာ secret တွေ ပါထားလို့ Git ဆီ တက်သွားရင် အများသိသွားပါမယ်။ ဒါကြောင့် Git က ဒီ file ကို လုံးဝ မမြင်စေရန် ပြင်ဆင်ရပါမယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Project folder ထဲမှာ `.gitignore` file တစ်ခု ဖန်တီးပြီး အောက်ပါ စာကြောင်း ထည့်ပါ —

```
.env
```

ဒါဆို `.env` file ကို Git က လျစ်လျူရှုပြီး GitHub ဆီ တင်မိတော့ပါ။

### ဥပမာ

Project structure တစ်ခုရဲ့ ပုံစံ —

```text
my_ai_project/
    .env
    .gitignore
    main.py
    requirements.txt
```

Team မှာ တွဲလုပ်တဲ့အခါ `.env` အစား `.env.example` ဆိုတဲ့ sample file တစ်ခု တင်ပြီး key တွေရဲ့ ပုံစံကိုပဲ မျှဝေပါတယ် —

```
OPENAI_API_KEY=your-key-here
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

GitHub ပေါ်မှာ API key တင်မိလို့ နာမည်ကြီးဖြစ်ခဲ့တဲ့ ဇာတ်လမ်းတွေ များပါတယ်။ `.gitignore` ကို project စတင်တဲ့ အခါမှာပဲ ပြင်ဆင်ထားရင် ဒီလို အမှားမျိုး ကာကွယ်နိုင်ပါတယ်။

## အနှစ်ချုပ်

- Secret တွေကို code ထဲ မရေးပါနဲ့။
- Environment variable က key ကို code အပြင်ဘက်မှာ သိမ်းခြင်းနည်းပါ။
- Local development အတွက် `.env` file နည်းက အလွယ်ကူဆုံးပါ။
- `.env` ကို `.gitignore` နဲ့ အမြဲ ကာကွယ်ပါ။
