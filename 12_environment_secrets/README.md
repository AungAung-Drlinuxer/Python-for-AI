# Environment & Secrets — API Key လုံခြုံစွာ သုံးနည်း

API key နဲ့ password တို့လို လျှို့ဝှက် data တွေကို code ထဲမှာ တိုက်ရိုက်မရေးဘဲ environment variable နဲ့ `.env` file သုံးပြီး လုံခြုံစွာ သိမ်းဆည်းနည်းကို ဒီ module မှာ သင်ယူမှာ ဖြစ်ပါတယ်။

## ဒီ module မှာ ဘာသင်မလဲ

- Secret data ဆိုတာ ဘာလဲ၊ ဘာကြောင့် code ထဲ မရေးသင့်တာလဲ
- Environment variable ဆိုတာ ဘာလဲ၊ ဘယ်လို အလုပ်လုပ်လဲ
- System environment variable သတ်မှတ်ပြီး ဖတ်နည်း
- `.env` file သုံးပြီး API key သိမ်းနည်း
- `python-dotenv` package နဲ့ `.env` file ကနေ value ဖတ်နည်း
- `.env` file ကို Git ထဲ မတင်ရန် `.gitignore` နဲ့ ကာကွယ်နည်း

## သင်ခန်းစာများ

1. **Secret ကို code ထဲ ဘာကြောင့် မရေးသင့်လဲ** — API key ကို code ထဲတိုက်ရိုက်ရေးမှုက ဘာကြောင့် အန္တရာယ်ရှိတာလဲဆိုတာကို ရှင်းပြပါတယ်။
2. **Environment variable အခြေခံ** — Operating system ရဲ့ environment variable ဆိုတာ ဘာလဲ၊ Python ကနေ ဘယ်လို ဖတ်မလဲကို သင်ကြားပါတယ်။
3. **`.env` file နဲ့ စီမံခန့်ခွဲနည်း** — Local development အတွက် အသုံးအများဆုံးဖြစ်တဲ့ `.env` file နည်းကို လက်တွေ့ကျကျ လေ့ကျင့်ပါတယ်။
4. **`python-dotenv` နဲ့ ဖတ်နည်း** — `.env` file ထဲက value တွေကို Python code နဲ့ ဘယ်လို ယူသုံးမလဲကို သင်ကြားပါတယ်။
5. **`.gitignore` နဲ့ ကာကွယ်နည်း** — `.env` file ကို GitHub ဆီ မတင်မိရန် ဘယ်လို ပြင်ဆင်ရမလဲကို လေ့လာပါတယ်။

## မသင်မီ လိုအပ်ချက်များ (Prerequisites)

- Python variable အခြေခံ သိထားရပါမယ်
- `pip install` နဲ့ package install လုပ်နည်း သိထားရပါမယ်
- Terminal သို့မဟုတ် command line အခြေခံ အသုံးပြုနိုင်ရပါမယ်

## ဘယ်အချိန်မှာ အသုံးဝင်လဲ

OpenAI API တို့ LLM API တို့နဲ့ အလုပ်လုပ်တဲ့ AI project တိုင်းမှာ API key လိုအပ်ပါတယ်။ Database password၊ cloud service key တွေအတွက်လည်း ဒီနည်းက အသုံးဝင်ပါတယ်။ Project တစ်ခုစီမှာ secret တွေကို လုံခြုံစွာ သိမ်းဆည်းချင်တဲ့အခါ ဒီ module ရဲ့ အသိပညာက တိုက်ရိုက် အသုံးဝင်ပါတယ်။

## အသုံးဝင်မည့် ကိုးကားများ

- Python Variables — https://python.datalumina.com/
- Dotenv / Environment Variables — https://python.datalumina.com/
