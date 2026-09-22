# External Tools — Packages & APIs

ဒီ module မှာ Python ကို package တွေနဲ့ API တွေသုံးပြီး တိုးချဲ့တတ်အောင် သင်မယ်။

## ဒီ module မှာ ဘာသင်မလဲ

- Built-in module နဲ့ external package ရဲ့ ကွာခြားချက်ကို နားလည်မယ်
- venv ထဲမှာ external package တွေကို install လုပ်တတ်မယ်
- Python ecosystem ထဲက အသုံးဝင်တဲ့ package တွေကို မိတ်ဆက်ခံရမယ်
- API ကနေ data တွေ pull လုပ်ပြီး သုံးတတ်အောင် လေ့ကျင့်မယ်
- API data တွေကို analyze လုပ်တတ်အောင် သင်မယ်

## သင်ခန်းစာ စာရင်း

### ၁။ Importing Modules
- Built-in module တွေ import လုပ်နည်း
- External package တွေကို venv ထဲမှာ install လုပ်ပြီးသုံးနည်း
- `pip` command သုံးပုံ

### ၂။ Working with APIs
- API ဆိုတာ ဘာလဲ၊ ဘာကြောင့် အရေးကြီးလဲ
- `requests` package နဲ့ web service ကနေ data pull လုပ်နည်း
- JSON data ကို Python object အဖြစ်ပြောင်းနည်း

### ၃။ Working with Data
- API ကနေရထားတဲ့ data တွေကို `pandas` နဲ့ analyze လုပ်နည်း
- Data ကို ရိုးရိုးရှင်းရှင်း ကြည့်နည်းနဲ့ စစ်နည်း

## Key Packages (ဒီ module မှာ သုံးမယ့် package တွေ)

| Package | အသုံးဝင်ပုံ |
|---------|-------------|
| `requests` | Web service တွေဆီက data ယူရန် |
| `pandas` | Data တွေကို analyze လုပ်ရန် |
| `beautifulsoup4` | Web scraping အတွက် |
| `openai` | OpenAI API ကို ချိတ်ဆက်ရန် |
| `python-dotenv` | API key တွေကို လုံခြုံစွာ သိမ်းရန် |

## Prerequisites (ဒီ module အရင် သင်ထားသင့်တာတွေ)

- Python variables, functions, lists, dictionaries အ基础 တွေ
- `pip` သုံးပြီး package install လုပ်နိုင်တဲ့ environment (venv)

## ဘယ်အချိန်မှာ အသုံးဝင်လဲ

- Web site တစ်ခုက data တွေ အလိုအလျောက် ယူချင်တဲ့အခါ
- AI model တစ်ခုရဲ့ API ကို ချိတ်ဆက်ချင်တဲ့အခါ
- အွန်လိုင်းမှာရှိတဲ့ data တွေကို analyze လုပ်ချင်တဲ့အခါ
- လက်ဖြင့်လုပ်ရတဲ့ အလုပ်တွေကို Python နဲ့ automate လုပ်ချင်တဲ့အခါ

## Reference Links

- Importing Modules — https://python.datalumina.com/libraries-apis/importing-modules
- Working with APIs — https://python.datalumina.com/libraries-apis/working-with-apis
- Working with Data — https://python.datalumina.com/libraries-apis/working-with-data
