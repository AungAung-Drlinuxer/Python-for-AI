# လက်တွေ့လေ့ကျင့်ခန်းများ

အလွယ်ကနေ ခက်ခဲအတိုင်း စီထားပါတယ်။ တစ်ခုချင်းစီ ကိုယ်တိုင်ကြိုးစားပြီးမှ solution ကြည့်ပါ။

## ၁။ ဝယ်စာရင်း List တည်ဆောက်ခြင်း

`shopping` အမည်ရှိ list တစ်ခု တည်ဆောက်ပါ။ အထဲမှာ ပစ္စည်း ၃ ခု ထည့်ပါ။ ထည့်ပြီးတဲ့နောက် ပစ္စည်း အများကြီး ဖြစ်လာအောင် အသစ်တစ်ခု ထပ်ထည့်ပြီး အားလုံးကို print လုပ်ပါ။

**Hints:** `append()` method ကို သုံးပါ။ List အားလုံးကို `print()` နဲ့ တန်းပြနိုင်ပါတယ်။

**Expected:** List ထဲမှာ item ၄ ခုပါပြီး အစီအစဉ်အတိုင်း ပေါ်ပါမယ်။

## ၂။ Dictionary နဲ့ ဖုန်းစာရင်း

`phonebook` dictionary တစ်ခု တည်ဆောက်ပါ။ နာမည် ၂ ခုနဲ့ ဖုန်းနံပါတ် ၂ ခု ထည့်ပါ။ အသစ်တစ်ယောက် ထပ်ထည့်ပြီး တစ်ယောက်ရဲ့ နံပါတ်ကို key နဲ့ ရှာပြပါ။

**Hints:** `phonebook["name"]` ပုံစံနဲ့ ရှာပါ။ အသစ်ထည့်ရန်လည်း ဒီပုံစံပဲ သုံးပါ။

**Expected:** ရှာတဲ့ နာမည်ရဲ့ ဖုန်းနံပါတ် တန်းပေါ်ပါမယ်။

## ၃။ Coordinate Tuple

`(latitude, longitude)` ပုံစံနဲ့ မြို့တစ်မြို့ရဲ့ location ကို tuple အဖြစ် သိမ်းပါ။ တစ်ခုချင်းစီကို index နဲ့ ရယူပြီး print လုပ်ပါ။ ပြီးရင် တစ်ခုပြောင်းလိုက်ရင် error ဖြစ်တာကို လေ့လာဖို့ အဲဒီကုဒ်ကို comment လုပ်ထားပါ။

**Hints:** Index 0 က latitude၊ index 1 က longitude ပါ။

**Expected:** တစ်ခုချင်းစီ အရေအတွက်အတိအကျ ပေါ်ပါမယ်။ Comment လုပ်ထားတဲ့ ကုဒ် run ရင် TypeError ဖြစ်မှာပါ။

## ၄။ Set နဲ့ Unique စကားလုံးများ

`"apple banana apple cherry apple"` ဆိုတဲ့ sentence တစ်ခုကနေ စကားလုံးတွေကို ခွဲပြီး set ထဲထည့်ပါ။ ဘယ်မျှမျိုးစုံမှန်း print လုပ်ပါ။

**Hints:** `sentence.split()` က string ကနေ word list ခွဲပေးပါတယ်။ `set()` က list ကနေ set ဆောက်ပေးပါတယ်။ `len()` နဲ့ အရေအတွက်ရပါတယ်။

**Expected:** Duplicate "apple" တွေ တစ်ခုပဲ ကျန်ပြီး ၃ မျိုး ရှိတာကို မြင်ရမယ်။

## ၅။ List မှာ Index နဲ့ Item ရှာခြင်း

`models = ["gpt", "claude", "gemini", "llama"]` list မှာ — (a) ပထမဆုံး item ကို index နဲ့ ရယူပါ၊ (b) နောက်ဆုံး item ကို ရယူပါ၊ (c) "claude" ရှိမရှိ `in` keyword နဲ့ စစ်ပါ။

**Hints:** နောက်ဆုံး item အတွက် index `len(models) - 1` သုံးနိုင်ပါတယ်။

**Expected:** ပထမဆုံးနဲ့ နောက်ဆုံး item ပေါ်ပြီး "claude" အတွက် `True` ပေါ်ပါမယ်။

## ၆။ AI Agent Profile (အားလုံးပေါင်း)

AI agent တစ်ခုရဲ့ profile ကို သိမ်းပါ — (a) အလုပ်တွေ list အဖြစ်၊ (b) config တွေ dictionary အဖြစ်၊ (c) version ကို tuple အဖြစ်၊ (d) လက်ခံနိုင်တဲ့ command တွေကို set အဖြစ် သိမ်းပါ။ Config ထဲက value တစ်ခုရှာပြပြီး command တစ်ခု လက်ခံမလဲ စစ်ပြပါ။

**Hints:** ဥပမာ — tasks = `["answer questions", "summarize text"]`, config = `{"name": "Helper", "speed": 10}`၊ version = `(1, 0)`၊ commands = `{"ask", "summarize", "translate"}`။

**Expected:** Config က value တစ်ခုနဲ့ command စစ်တဲ့ ရလဒ် `True` သို့မဟုတ် `False` ပေါ်ပါမယ်။
