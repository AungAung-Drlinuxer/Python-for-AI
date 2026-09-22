# Formatting with Ruff — Lint & Format

ဒီ module မှာ Python code တွေကို အလိုအလျောက် ရှင်းလင်းစွာရေးသွင်းနိုင်ရန် Ruff tool ကို သင်使用မည်။ (Python code ကို အလိုအလျောက် ရှင်းလင်းအဆင်ပြေစေရန် Ruff tool ကို အသုံးပြုသင်မည်။)

## ဒီ module မှာ ဘာသင်မလဲ

- Ruff ဆိုတာ ဘာလဲဆိုတာကို နားလည်မည်
- VS Code ထဲမှာ Ruff extension ထည့်သွင်းနည်း
- Save လုပ်တိုင်း format လုပ်ပေးသည့် setting ဖွင့်နည်း
- Linting ဆိုတာ ဘာလဲနှင့် အမှားများကို ရှာတွေ့နည်း
- PEP 8 style rules များကို Ruff က ဘယ်လို စီမံပေးလဲ

## သင်ခန်းစာများ

1. **Ruff ဆိုတာ ဘာလဲ** — modern all-in-one tool အကြောင်း။ Linting (ပြဿနာရှာခြင်း)၊ formatting (style အလိုအလျောက်ပြင်ခြင်း)နှင့် import sorting (import များ အစီအစဉ်တကျ စီခြင်း) ကို တစ်ခုတည်းနှင့် လုပ်ပေးနိုင်သည်။ Pylint, Black, isort တို့နေရာကို အစားထိုးနိုင်သည်။
2. **VS Code Setup** — Astral ရေးသားသည့် Ruff extension ကို install ခြင်း၊ Format On Save ဖွင့်ခြင်း၊ Python formatting provider ကို Ruff ဟု သတ်မှတ်ခြင်း။
3. **Linting** — code ထဲက ပြဿနာများကို ရှာတွေ့နည်း။
4. **PEP 8 Formatting Rules** — 4 spaces indent၊ operator များပတ်ဝန်းကျင် space၊ function များကြား blank line နှစ်ကြောင်း၊ line အရှည် 88 အထိ စသည့် rules များကို Ruff က အလိုအလျောက် စီမံပေးသည်။

## ဘာတွေ ကြိုတင်လိုအပ်လဲ

- Python အခြေခံရေးသွင်းနည်း နားလည်ထားရမည်
- VS Code ထဲမှာ Python development environment ပြင်ဆင်ထားရမည်

## ဘယ်အချိန်မှာ အသုံးဝင်လဲ

AI project ကြီးတစ်ခုရေးသည့်အခါ code ရှည်လျားလာပြီး style မကိုက်ညီမှုများဖြစ်လာသည်။ Ruff ကို အသုံးပြုပါက save လုပ်တိုင်း code သန့်ရှင်းသွားပြီး အဖွဲ့လိုက်ရေးသည့် project များတွင် စံတစ်ခုတည်းသာ ရှိသွားမည်။ ထို့ကြောင့် agent သို့မဟုတ် model တစ်ခု ရေးသည့်အခါတွင်လည်း code အရည်အသွေးကို ထိန်းသိမ်းနိုင်မည်။

## ကိုးကားလင့်ခ်များ

- Ruff Setup: https://python.datalumina.com/tools/code-quality
- Format On Save: https://python.datalumina.com/tools/code-quality
- Linting: https://python.datalumina.com/tools/code-quality
