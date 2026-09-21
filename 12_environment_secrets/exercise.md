# လေ့ကျင့်ခန်းများ — Environment & Secrets

ဒီလေ့ကျင့်ခန်းတွေက API key လုံခြုံစွာ သိမ်းဆည်းနည်းကို လက်တွေ့လေ့ကျင့်စေဖို့ ရည်ရွယ်ပါတယ်။ အခက်ခဲအလွယ် အဆင့်တက်စွာ ဖြေဆိုပါ။

## ၁ — Environment Variable ဖတ်ခြင်း

Terminal မှာ `MY_NAME` ဆိုတဲ့ environment variable တစ်ခု သတ်မှတ်ပါ။ Python code နဲ့ ဒီ variable ကို ဖတ်ပြီး print လုပ်ပါ။

**Hint:** macOS/Linux မှာ `export MY_NAME="..."` ဟု ရိုက်ပါ။ Python မှာ `os.environ.get()` ကို သုံးပါ။

**မျှော်မှန်းရလဒ် —** Program run ရင် သင်သတ်မှတ်ထားတဲ့ နာမည်ကို print လုပ်ပါမယ်။

## ၂ — Key ရှိ/မရှိ စစ်ခြင်း

`API_KEY` ဆိုတဲ့ environment variable ကို ဖတ်ပြီး ရှိလည်း မရှိလည်း စစ်ပါ။ ရှိရင် `"Key found"` လို့ print လုပ်ပြီး မရှိရင် `"Key missing"` လို့ print လုပ်ပါ။ Variable ကို သတ်မှတ်ထားတဲ့ အခါမျိုး၊ မထားတဲ့ အခါမျိုး နှစ်ခုလုံး စမ်းကြည့်ပါ။

**Hint:** `os.environ.get()` က variable မရှိရင် `None` ပြန်ပါတယ်။ `if` နဲ့ စစ်ပါ။

**မျှော်မှန်းရလဒ် —** Variable ရှိတုန်းး `"Key found"`၊ မရှိရင် `"Key missing"` ထွက်ပါမယ်။

## ၃ — `.env` File ဖန်တီးပြီး ဖတ်ခြင်း

`pip install python-dotenv` နဲ့ package install လုပ်ပါ။ Project folder ထဲမှာ `.env` file တစ်ခု ဖန်တီးပြီး `OPENAI_API_KEY=test-key-123` ဆိုပြီး ရေးထားပါ။ Python code နဲ့ ဒီ value ကို ဖတ်ပြီး print လုပ်ပါ။

**Hint:** `load_dotenv()` ကို ရေးပြီးမှ `os.environ.get()` နဲ့ ဖတ်ပါ။

**မျှော်မှန်းရလဒ် —** Program run ရင် `test-key-123` ထွက်ပါမယ်။

## ၄ — `.gitignore` နည်း ခံထားတဲ့ Structure ဆောက်ခြင်း

`my_ai_project` folder တစ်ခု ဆောက်ပါ။ အထဲမှာ `.env`၊ `.gitignore`၊ `main.py`ဆိုပြီး file သုံးခု ထည့်ပါ။ `.gitignore` ထဲမှာ `.env` ကို အပါးသင့်ဖြစ်စေပြီး `.env` ထဲမှာ `DATABASE_URL` တစ်ခု ရေးပါ။ `main.py` ကနေ ဒီ value ကို ဖတ်ပြီး print လုပ်ပါ။

**Hint:** `load_dotenv()` က `.env` file ကို project folder ထဲက သဘာ၀အတိုင်း ရှာပါတယ်။

**မျှော်မှန်းရလဒ် —** `main.py` run ရင် database URL ထွက်ပြီး `.env` file က Git ဆီတင်မိမည် မဟုတ်ပါ။

## ၅ — AI Agent Setting File ဖန်တီးခြင်း

OpenAI API key နဲ့ model နာမည် နှစ်ခုလုံးကို `.env` file ထဲမှာ သိမ်းပါ — `OPENAI_API_KEY` နဲ့ `MODEL_NAME` ဆိုတဲ့ variable နှစ်ခု။ Python code နဲ့ ဒီ နှစ်ခုလုံး ဖတ်ပြီး agent က ဘယ် key နဲ့ ဘယ် model ကို သုံးမလဲဆိုတာ ပြောပြမယ့် program တစ်ခု ရေးပါ။

**Hint:** `.env` file တစ်ခုထဲမှာ variable အများကြီး တစ်ကြောင်းချင်း `KEY=value` ပုံစံနဲ့ ရေးနိုင်ပါတယ်။

**မျှော်မှန်းရလဒ် —** Program run ရင် model နာမည်နဲ့ key ရှိ/မရှိကို ပြောပြပါမယ် (key အပြည့်အစုံကို print မလုပ်ပါနဲ့)။

## ၆ — Safety Check Function

`check_secrets()` ဆိုတဲ့ function တစ်ခု ရေးပါ။ ဒီ function က `OPENAI_API_KEY` ရှိ/မရှိကို စစ်ပြီး မရှိရင် ရပ်စေတဲ့ error message နဲ့ ဆုံးပါမယ်။ နောက် `main` အစအဆုံးမှာ ဒီ function ကို ခေါ်ပြီး key ရှိမှ ဆက်လုပ်တဲ့ ပုံစံနဲ့ ရေးပါ။

**Hint:** `raise SystemExit("message")` ဟူ၍ ရေးပြီး မရှိတဲ့အခါ program ကို ရပ်စေနိုင်ပါတယ်။

**မျှော်မှန်းရလဒ် —** Key မရှိတဲ့အခါ program က error message နဲ့ ရပ်သွားပြီး ရှိတဲ့အခါ ဆက်လုပ်ပါမယ်။
