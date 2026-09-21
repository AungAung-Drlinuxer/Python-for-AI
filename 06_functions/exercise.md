# Exercises — Functions

အောက်မှာ လက်တွေ့ လေ့ကျင့်ခန်း ၆ ခု ပါတယ်။ အလွယ်ကနေ ခက်ခဲအထိ စီထားတယ်။

## လေ့ကျင့်ခန်း ၁ — Greeting Function ရေးပါ

Function တစ်ခု define လုပ်ပါ — အမည်က `greet()`။ ခေါ်လိုက်ရင် `"Welcome to Python for AI!"` ဆိုတာ ပရင့်ထုတ်ပါ။ ၃ ခေါက် ခေါ်ပြပါ။

**Hints:** `def greet():` နဲ့ စပါ။ Function ကိုယ်ထည်ကို indent (၄ ကွက်) လုပ်ပါ။

**Expected behavior:** `"Welcome to Python for AI!"` စာသား ၃ ကြိမ် ပေါ်ရမယ်။

## လေ့ကျင့်ခန်း ၂ — နာမည်နဲ့ နှုတ်ခွန်ဆော်ပါ

`greet_name(name)` ဆိုတဲ့ function ရေးပါ။ Parameter `name` ထည့်ပြီး `"Hello, <name>!"` ပုံစံနဲ့ ပရင့်ထုတ်ပါ။ နာမည် ၂ ခု နဲ့ စမ်းပါ။

**Hints:** String နှစ်ခုကို `+` နဲ့ ဆက်လို့ရတယ်၊ ဒါမှမဟုတ် f-string သုံးလို့ရတယ်။

**Expected behavior:** `greet_name("Aung")` ခေါ်ရင် `Hello, Aung!` ပေါ်ရမယ်။

## လေ့ကျင့်ခန်း ၃ — နံပါတ်နှစ်ခု ပေါင်းပါ

`add_numbers(a, b)` ဆိုတဲ့ function ရေးပါ။ Parameter နှစ်ခုလက်ခံပြီး ပေါင်းခြင်းရလဒ်ကို **return** ပြန်ပါ။ ရလဒ်ကို variable မှာ သိမ်းပြီး ပရင့်ထုတ်ပါ။

**Hints:** `return a + b` လို့ ရေးလို့ရတယ်။ ရလဒ်ကို `result = add_numbers(5, 3)` လို သိမ်းပါ။

**Expected behavior:** `add_numbers(5, 3)` က `8` ပြန်ရမယ်။

## လေ့ကျင့်ခန်း ၄ — Tax တွက်ပါ

`calculate_tax(price, rate)` ဆိုတဲ့ function ရေးပါ။ `price` က ကုန်ပစ္စည်း တန်ဖိုး၊ `rate` က tax အချိုး (ဥပမာ — `0.05`)။ Tax ပမာဏကို return ပြန်ပါ။ တန်ဖိုး `20000`၊ rate `0.05` နဲ့ စမ်းပြပါ။

**Hints:** Tax = `price * rate` ဖြစ်တယ်။ ပြီးရင် total တွက်ဖို့ ရလဒ်ကို ဆက်သုံးလို့ရတယ်။

**Expected behavior:** `calculate_tax(20000, 0.05)` က `1000.0` ပြန်ရမယ်။

## လေ့ကျင့်ခန်း ၅ — စာသားရှည်ကို စစ်ပါ

`is_long_message(text)` ဆိုတဲ့ function ရေးပါ။ Text ရဲ့ အရှည်က `20` ထက်ကြီးရင် `True`၊ မဟုတ်ရင် `False` return ပြန်ပါ။ စာသားတိုတစ်ခု၊ ရှည်တစ်ခု နှစ်ခုလုံးနဲ့ စမ်းပါ။

**Hints:** `len()` function က စာသားရဲ့ အရှည်ကိုပေးတယ်။ `if/else` နဲ့ `return` ကို တွဲသုံးပါ။

**Expected behavior:** `is_long_message("Hi")` က `False`၊ `is_long_message("This is a very long message")` က `True` ပြန်ရမယ်။

## လေ့ကျင့်ခန်း ၆ — AI Agent Message Labeler

`build_prompt(role, task)` ဆိုတဲ့ function ရေးပါ။ `role` (ဥပမာ — `"assistant"`) နဲ့ `task` (စာသား) လက်ခံပြီး `"You are a <role>. Your task: <task>"` ပုံစံနဲ့ prompt တစ်ခု return ပြန်ပါ။ `role` မပေးထားရင် default အနေနဲ့ `"assistant"` သုံးပါ။ ၂ မျိုး စမ်းပြပါ — role ပေးထားတာ တစ်ခု၊ မပေးထားတာ တစ်ခု။

**Hints:** Parameter default value ကို `def build_prompt(role="assistant", task=""):` လို ရေးလို့ရတယ်။

**Expected behavior:** `build_prompt(task="summarize the text")` ခေါ်ရင် role က `assistant` ဖြစ်နေရမယ်၊ role ပေးရင် ပေးတဲ့ role ပေါ်ရမယ်။
