# Error Handling — try/except

ဒီ module မှာ Python program များမှာ အမှားများ (errors) ကို ဘယ်လိုကိုင်တွယ်ရမလဲဆိုတာကို သင်ကြားပါမယ်။ Program တစ်ခုက crash မခံဘဲ ဆက်လုပ်ဆောင်နိုင်အောင် `try/except` နည်းနဲ့ ကာကွယ်တဲ့ပုံစံကို လက်တွေ့ဥပမာတွေနဲ့ သင်ကြားပေးပါလိမ့်မယ်။

## ဒီ module မှာ ဘာသင်မလဲ

- Python error အမျိုးမျိုးရဲ့ သဘောသဘာဝကို နားလည်တာ
- Syntax error နဲ့ runtime error ကွာခြားချက်ကို ခွဲခြားသိနိုင်တာ
- `try/except` သုံးပြီး program ကို crash မှ ကယ်တင်တဲ့နည်း
- နေ့စဉ်တွေ့ရတဲ့ error တွေ (ZeroDivisionError, NameError, TypeError, FileNotFoundError) တွေကို ဖြေရှင်းတာ

## သင်ခန်းစာများ

1. **Error ဆိုတာ ဘာလဲ** — Error ဖြစ်တဲ့ အခြေအနေတွေ (file မရှိ၊ API ပျက်နေ၊ user က number အစား 'abc' ရိုက်တာ) ကို လေ့လာပါမယ်။
2. **SyntaxError** — code ရေးသားပုံမှားရင် ဘာဖြစ်လဲဆိုတာ (ဥပမာ — colon မထည့်တာ) ကို သင်ပါမယ်။
3. **Runtime errors** — Program လည်နေတုန်းက ဖြစ်တဲ့ error သုံးမျိုး (ZeroDivisionError, NameError, TypeError) ကို ဥပမာနဲ့ ကြည့်ပါမယ်။
4. **try/except နဲ့ ကိုင်တွဲတာ** — Crash ခံရတဲ့ version နဲ့ ကိုင်တွယ်ထားတဲ့ version ကို နှိုင်းယှဉ်ပြပါမယ်။ FileNotFoundError ကို `try/except` နဲ့ ဖမ်းပြီး program က 'Done!' ဆိုတဲ့ အဆင့်ထိ ရောက်အောင် လုပ်ပြပါမယ်။

## လိုအပ်ချက်များ (Prerequisites)

- Python basics — variables, `print()`, basic data types (strings, numbers)
- Function အခြေခံ အနည်းငယ်
- Module တွေရဲ့ အခြေခံကောင်းရင် ပိုကောင်းပါတယ်

## ဘယ်အချိန်မှာ အသုံးဝင်လဲ

AI project တွေမှာ user input၊ file ဖတ်တာ၊ API ခေါ်တာဆိုတာတွေက error ဖြစ်လွယ်တဲ့ နေရာတွေပါ။ ဥပမာ — user က number မှာ 'abc' ရိုက်လိုက်ရင်၊ ဒါမှမဟုတ် AI model က ဖတ်ရမဲ့ data file မရှိရင် program က crash သွားနိုင်ပါတယ်။ `try/except` သုံးတတ်ရင် program က ခံစားနိုင်တဲ့ error တွေကို သည့်တော့သည့်အတိုင်း ကိုင်တွယ်ပြီး ဆက်လည်နိုင်ပါတယ်။ Error handling က production-ready software ရေးတဲ့အခါ မဖြစ်မနေ လိုအပ်တဲ့ ကျွမ်းကျင်မှုတစ်ခုပါ။

## References

- try/except: https://python.datalumina.com/learn/python-basics/try-except
- Common errors: https://python.datalumina.com/learn/python-basics/common-errors
