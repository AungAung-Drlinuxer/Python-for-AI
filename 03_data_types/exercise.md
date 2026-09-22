# လက်တွေ့ လေ့ကျင့်ခန်းများ — Data Types

## လေ့ကျင့်ခန်း ၁ — Accuracy နှင့် Loss ကိန်းများ

**Task:** `accuracy` ဆိုတဲ့ variable မှာ `0.85` ကို သိမ်းပါ။ `epochs` ဆိုတဲ့ variable မှာ `5` ကို သိမ်းပါ။ ဒီနှစ်ခုလုံးကို `print()` နဲ့ ထုတ်ပြပါ။

**Hints:** Float ကိန်းနဲ့ int ကိန်း သိမ်းပုံက တူတူပါပဲ။ Variable နာမည် မှာ ရှေ့ဆင့်နောက်ဆင့် ရေးပါ။

**Expected behavior:** Program က `0.85` နှင့် `5` ကို ထွက်ပြပါမယ်။

## လေ့ကျင့်ခန်း ၂ — Model Name String

**Task:** `model_name` variable မှာ string တစ်ခု သိမ်းပြီး ၎င်းနဲ့ `" is ready"` ဆိုတဲ့ string ကို ပေါင်းပြပါ။

**Hints:** String ပေါင်းရန် `+` သင်္ကေတ သုံးပါ။ String ကို quote နဲ့ ဖွင့်ပိတ်ပါ။

**Expected behavior:** ပေါင်းလိုက်တဲ့ sentence အပြည့်အစုံ ထွက်ပါမယ်။

## လေ့ကျင့်ခန်း ၃ — Confidence Check (Boolean)

**Task:** `confidence` variable မှာ `0.92` သိမ်းပါ။ ၎င်းက `0.90` ထက် ကြီးလား ဆိုတာကို နှိုင်းယှဉ်ပြီး `is_confident` variable မှာ သိမ်းပြီး ထုတ်ပြပါ။

**Hints:** `>` သင်္ကေတနဲ့ နှိုင်းယှဉ်ရင် `True` ဒါမှမဟုတ် `False` ရပါတယ်။

**Expected behavior:** ရလဒ်က `True` ဖြစ်ပါမယ်၊ ဘာကြောင့်လဲဆိုတာကိုလည်း စဉ်းစားကြည့်ပါ။

## လေ့ကျင့်ခန်း ၄ — type() နဲ့ Type စစ်တာ

**Task:** `type()` သုံးပြီး `42`, `3.14`, `'Hello'`, `True` တို့ရဲ့ type တွေကို အစဉ်လိုက် ထုတ်ပြပါ။

**Hints:** `print(type(value))` ဆိုပြီး ရေးလို့ ရပါတယ်။

**Expected behavior:** `int`, `float`, `str`, `bool` တို့ကို အစဉ်လိုက် မြင်ရပါမယ်။

## လေ့ကျင့်ခန်း ၅ — String ကိန်းကို ပြောင်းပြီး တွက်တာ

**Task:** User ဆီက ဝင်လာတဲ့ `"25"` ဆိုတဲ့ string score ကို int အဖြစ် ပြောင်းပြီး `5` နဲ့ ပေါင်းပြပါ။

**Hints:** `int()` function သုံးပါ။ တိုက်ရိုက် `"25" + 5` လုပ်ရင် error တက်မယ် ဆိုတာ သတိထားပါ။

**Expected behavior:** ရလဒ်က `30` ဖြစ်ပါမယ်။

## လေ့ကျင့်ခန်း ၆ — AI Agent Message Builder

**Task:** AI agent တစ်ခုမှာ confidence score ရှိပါတယ်။ `confidence` variable မှာ `0.88` သိမ်းပါ။ `type()` နဲ့ confidence ရဲ့ type စစ်ပြပါ။ ပြီးရင် `"Confidence: "` ဆိုတဲ့ string နဲ့ confidence ကို ပေါင်းပြီး တစ်ခုတည်းသော message ထုတ်ပါ။

**Hints:** Float ကို string နဲ့ ပေါင်းချင်ရင် `str()` နဲ့ အရင် ပြောင်းပါ။

**Expected behavior:** `Confidence: 0.88` ဆိုတဲ့ message ထွက်ပါမယ်။

