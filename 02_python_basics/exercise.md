# လက်တွေ့ စာမေးပွဲများ — Python Basics

## ၁။ Variable သိမ်းဆည်းခြင်း

**Task** — ကိုယ့်အကြောင်း data သုံးခု variable ထဲ သိမ်းပြီး print ထုတ်ပါ။ `name`, `age`, `city` ဆိုတဲ့ variable သုံးခု ဆောက်ပါ။

**Hint** — Variable နာမည်တွေကို ရိုးရှင်းပြီး နားလည်လွယ်အောင် ပေးပါ။ Value တွေကို `"..."` ထဲ ထည့်ပါ။

**Expected behavior** — ကုဒ် run ရင် နာမည်၊ အသက်၊ မြို့ သုံးခု ထွက်ပါမယ်။

**Hints:** Variable ဆောက်ဖို့ `name = "..."` ဆိုတဲ့ pattern ကို သုံးပါ၊ age မှာ quotes မထည့်ပါနဲ့၊ ထုတ်ပြရန် `print()` function ကို ခေါ်ပါ။

## ၂။ သချာညီမျှ Operator သုံးခြင်း

**Task** — `score` variable တစ်ခု ဆောက်ပြီး (ဥပမာ 75) အောက်ပါတွေ တွက်ပါ — `score` ကို ၂ ဆ၊ `score` ကို ၁၀ နဲ့ စား၊ `score` ကို ၅ နဲ့ စားပြီး ကျန်တာ (modulo)။ ရလဒ်တွေ အကုန် print ထုတ်ပါ။

**Hint** — `*`, `/`, `%` operator တွေကို သုံးပါ။ Modulo က စားပြီး ကျန်တာ ပြပေးပါတယ်။

**Expected behavior** — တွက်ချက်မှု သုံးခုရဲ့ ရလဒ် သုံးကြောင်း ထွက်ပါမယ်။

**Hints:** `score` variable တစ်ခုတည်းကို variable အသစ်များမှာ သိမ်းဆည်းပြီး `*`, `/`, `%` operator တွေသုံးပြီး `print()` နဲ့ တစ်ကြောင်းချင်း ထုတ်ပြပါ။

## ၃။ နှိုင်းယှဉ်မှုနဲ့ Logical Operator

**Task** — `temperature = 30` ဆိုတဲ့ variable ဆောက်ပါ။ အပူချိန်က ၂၅ ထက် ကြီးလား၊ ၄၀ ထက် ငယ်လား ဆိုတာ နှိုင်းယှဉ်ပြီး print ထုတ်ပါ။ ပြီးရင် `and` သုံးပြီး နှစ်ခုလုံး မှန်လား စစ်ပါ။

**Hint** — နှိုင်းယှဉ်တဲ့အခါ `>` နဲ့ `<` သုံးပါ။ ရလဒ်က `True` ဒါမှမဟုတ် `False` ပြပါမယ်။

**Expected behavior** — `True`/`False` သုံးကြောင်း ထွက်ပါမယ်။

**Hints:** `and` operator က နှစ်ခုလုံး `True` ဖြစ်မှသာ `True` ပြမယ်၊ ဒါကို `if` မသုံးပါဘဲ comparison နှစ်ခုကိုတိုက်ရိုက် print လုပ်လို့ရတာ သတိထားပါ။

## ၄။ User Input သန့်စင်ခြင်း (AI အသုံးချ)

**Task** — User ရေးသွင်းတဲ့ sentence တစ်ခုကို ပြနိုင်အောင် လုပ်ပါ။ Sentence တစ်ခုကို variable ထဲ သိမ်းပြီး — space အစွန်းနှစ်ဖက် ဖယ်ရှား၊ အက္ခရာအသေးပြောင်း၊ "please" ကို "kindly" အစားထိုးပါ။ ရလဒ်ကို print ထုတ်ပါ။

**Hint** — `.strip()`, `.lower()`, `.replace()` method သုံးပါ။ Method တွေကို `.` နဲ့ တွဲသုံးနိုင်ပါတယ်။

**Expected behavior** — Input `" PLEASE help me  "` ဆိုရင် output က `kindly help me` ဖြစ်ပါမယ်။ ဒါက AI app တွေမှာ user input သန့်စင်တဲ့ ပုံစံ ဖြစ်ပါတယ်။

**Hints:** `input()` နဲ့ ယူထားတဲ့ sentence ကို `.strip()`, `.lower()`, `.replace()` method တွေကို `.` နဲ့ တစ်ဆက်တည်း တွဲသုံးပြီး သန့်စင်ပါ။

## ၅။ Loop နဲ့ Data စစ်ဆေးခြင်း

**Task** — `scores = [45, 78, 92, 60]` list ကို loop လုပ်ပြီး — ၇၀ နဲ့ ညီမျှ ဒါမှမဟုတ် ထက်ကြီးရင် "pass"၊ ငယ်ရင် "fail" လို့ print ထုတ်ပါ။ ရလဒ်နဲ့အတူ score တွေကိုပါ ပြပါ။

**Hint** — `for score in scores:` နဲ့ စပါ။ အတွင်းမှာ `if`/`else` သုံးပါ။ f-string သုံးပြီး score နဲ့ အတူ ပြပါ။

**Expected behavior** — လေးကြောင်း ထွက်ပြီး score တစ်ခုချင်းစီအတွက် pass/fail ပြပါမယ်။

**Hints:** `for` loop အတွင်းမှာ `if score >= 70:` နဲ့ `else` သုံးပြီး f-string မှာ score တန်ဖိုး ထည့်ဖို့ မမေ့ပါနဲ့။

## ၆။ Simple Model Response Filter (AI/Agent အသုံးချ)

**Task** — Agent ရဲ့ response တွေထဲက မှားနေတဲ့ (empty string) တွေကို စစ်ပါ။ `responses = ["Hello!", "", "How are you?", ""]` list ကို loop လုပ်ပြီး — response က ဗလာ (len က ၀) မဟုတ်ရင် ထွက်ပါမယ့် response အဖြစ် သတ်မှတ်ပြီး နာမည်ပေးထားတဲ့ list ထဲ ထည့်ပါ။ နောက်ဆုံးမှာ ခွင့်ပြုထားတဲ့ response အရေအတွက်ကိုပါ print ထုတ်ပါ။

**Hint** — ဗလာ list တစ်ခု အရင်ဆောက်ပါ။ Loop ထဲမှာ `len(response) > 0` နဲ့ စစ်ပြီး `.append()` နဲ့ ထည့်ပါ။

**Expected behavior** — `Hello!` နဲ့ `How are you?` ဆိုတဲ့ response ၂ ခုပဲ ခွင့်ပြု list ထဲ ဝင်ပြီး ၂ လို့ print ထွက်ပါမယ်။

**Hints:** ဗလာ list တစ်ခု အရင်ဆောက်ပြီး loop ထဲမှာ `len()` နဲ့ ဗလာမဟုတ်ကြောင်း စစ်၊ `.append()` နဲ့ ထည့်ပါ။

