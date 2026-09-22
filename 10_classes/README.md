# Classes — Object-Oriented Python

ဒီ module မှာ Python ၏ Object-Oriented Programming (OOP) အခြေခံများကို သင်ကြားပါမယ်။ ဆိုလိုသည်မှာ data နှင့် function များကို object တစ်ခုအဖြစ် စုစည်း သုံးစွဲနည်း ဖြစ်ပါသည်။

## ဒီ module မှာ ဘာသင်မလဲ

- Class နှင့် object ဆိုတာ ဘာလဲဆိုတာကို နားလည်မယ်
- Attribute (data) နှင့် method (behavior) တွေကို ရေးသားနိုင်မယ်
- `__init__` constructor ကို အသုံးပြုတတ်လာမယ်
- Inheritance (class ဆက်ခံခြင်း) အခြေခံကို လေ့လာမယ်
- ဘယ်အချိန်မှာ class သုံးသင့် ဘယ်အချိန်မှာ function လောက် လုံလောက်တယ်ဆိုတာ ခွဲခြားနိုင်မယ်

## သင်ခန်းစာ စာရင်း

1. **Class ဆိုတာ ဘာလဲ (first-class)** — Class ဆိုသည်မှာ blueprint (အကြံစည်) ဖြစ်ပုံ၊ object ဆိုသည်မှာ အဲဒီ blueprint မှ ပြုလုပ်ထားသော အရာတစ်ခုဖြစ်ပုံကို ရှင်းပြပါမယ်။ Toolbox ဥပမာနှင့် တူသည်။
2. **Methods နှင့် Attributes** — Object ထဲမှာ data (attributes) နှင့် လုပ်ဆောင်ချက်များ (methods) ကို ဘယ်လို သတ်မှတ်ရမလဲ။ `self` ဆိုတာ ဘာလဲ။ `__init__` က ဘယ်လို အလုပ်လုပ်လဲ။
3. **Inheritance** — ရှိပြီးသား class ကနေ နောက်ထပ် class အသစ်ကို ဆက်ခံပြီး ရေးနည်း။ Code ထပ်မရေးရတော့ပါ။
4. **ဘယ်အချိန်မှာ သုံးသင့်လဲ (when-to-use)** — Program တွေ ရှည်လာပြီး ရှုပ်ထွေးလာတဲ့အခါမှာ OOP က ဘာကြောင့် အသုံးဝင်လဲ။ Single-file script မှ functions၊ ပြီးရင် multiple files၊ နောက်ဆုံးမှာ classes အထိ တိုးတက်ပုံ။

## မသင်မနေရ လိုအပ်ချက်များ (Prerequisites)

- Python basics — variables, data types, lists, dicts
- Functions ရေးနည်း (def, return, parameters)
- Python file တစ်ခု run နည်း

## ဘယ်အချိန်မှာ အသုံးဝင်လဲ

AI project တွေမှာ OpenAI လို API client တွေနှင့် အလုပ်လုပ်ရတဲ့အခါ class တွေနဲ့ ရေးထားတဲ့ clean interface တွေကို တွေ့ရပါတယ်။ ဥပမာ — `OpenAIClient` class ထဲမှာ `__init__` နဲ့ `api_key` သိမ်းပြီး `generate(prompt)` method နဲ့ ခေါ်သုံးပါတယ်။ Data pipeline တွေနဲ့ တခြား program တွေမှာလည်း အကြိမ်ကြိမ် ပြန်သုံးနိုင်တဲ့ component တွေ၊ state သိမ်းထားရတဲ့ operation တွေအတွက် class တွေက အထိထိလိမ်မိဆုံး ဖြစ်ပါတယ်။

## Reference Links

- Classes overview: https://python.datalumina.com/ တွင် classes module ကို ကြည့်ပါ
- First-class / blueprint အခြေခံ: https://python.datalumina.com/advanced/classes/first-class
- Methods & Attributes: https://python.datalumina.com/advanced/classes/methods-attributes
- Inheritance: https://python.datalumina.com/advanced/classes/inheritance
- When to use OOP: https://python.datalumina.com/advanced/classes/when-to-use
