# လက်တွေ့လေ့ကျင့်ခန်းများ — If Statements

## ၁ — အပူချိန် စစ်ဆေးပါ

`temperature` ဆိုတဲ့ variable တစ်ခု ဖန်တီးပြီး တန်ဖိုး `30` ထည့်ပါ။ အကယ်၍ အပူချိန်က `25` ထက် ကြီးနေရင် "Hot day" ဆိုပြီး print ထုတ်ပါ။

**Hints:**
- `if` keyword ကိုသုံးပြီး `>` operator နဲ့ နှိုင်းယှဉ်ပါ
- `if` line အဆုံးမှာ colon (`:`) မမေ့ပါနဲ့
- Indentation (space ၄ ခု) ကို သတိထားပါ

**လိုအပ်တဲ့ ရလဒ်:** ပရိုဂရမ် run ရင် "Hot day" ပေါ်ရပါမယ်။

**Expected behavior:** ပရိုဂရမ် run ရင် "Hot day" ဆိုတာ ပေါ်ရပါမယ်

## ၂ — Password စစ်ဆေးပါ

`password` variable ထဲမှာ `letmein` ဆိုတဲ့ စကားလုံး ထည့်ပါ။ Password က `letmein` နဲ့ တူညီရင် "Access granted" ပြပါ၊ မတူရင် "Access denied" ပြပါ။

**Hints:**
- စကားလုံးနှစ်ခု တူမတူ စစ်ဖို့ `==` operator ကိုသုံးပါ
- မတူတဲ့ လမ်းကြောင်းအတွက် `else` ထည့်ပါ

**လိုအပ်တဲ့ ရလဒ်:** `password` တန်ဖိုးအလိုက် "Access granted" ဒါမှမဟုတ် "Access denied" တစ်ခုထဲ ပေါ်ရပါမယ်။

**Expected behavior:** password က `letmein` ဖြစ်လို့ "Access granted" ပေါ်ရပါမယ်

## ၃ — Health အလိုက် Game Status

`health` variable ထဲမှာ `0` ထည့်ပါ။ အကယ်၍ health က `0` ဖြစ်ရင် "Game over"၊ `30` ထက်နည်းရင် "Warning: low health"၊ ဒါမှမဟုတ် "Healthy" ပြပါ။

**Hints:**
- Condition သုံးခုအတွက် `if`၊ `elif`၊ `else` ကို အသုံးပြုပါ
- ပထမဆုံး `True` ဖြစ်တဲ့ တစ်ခုပဲ အလုပ်လုပ်မှာ ဖြစ်တာကို သတိရပါ

**လိုအပ်တဲ့ ရလဒ်:** `health = 0` မှာ "Game over" ပေါ်ရပါမယ်။ `health` ကို `50` ပြောင်းပြီး run ကြည့်ရင် "Healthy" ပေါ်ရပါမယ်။

**Expected behavior:** "Game over" ပေါ်ရပါမယ်၊ `health` ကို `50` ပြောင်း run ကြည့်ရင် "Healthy" ပေါ်မယ်

## ၄ — မှတ်ချက် စစ်ဆေးပါ (AI chatbot သုံးစွဲမှု)

AI chatbot တစ်ခုက user comment တစ်ခုကို စစ်နေတယ်လို့ ယူဆပါ။ `comment` variable ထဲမှာ `"You are great"` ထည့်ပါ။ Comment ထဲမှာ `"great"` ဆိုတဲ့ စကားလုံး ပါရင် "Positive comment detected" ပြပါ၊ မပါရင် "No positive keyword found" ပြပါ။

**Hints:**
- String တစ်ခုထဲမှာ စကားလုံးတစ်ခု ပါမပါ စစ်ဖို့ `in` keyword ကို သုံးနိုင်ပါတယ်— `"great" in comment`
- ဒါက `True` ဒါမှမဟုတ် `False` ပြန်ပါတယ်

**လိုအပ်တဲ့ ရလဒ်:** "Positive comment detected" ပေါ်ရပါမယ်။

**Expected behavior:** "Positive comment detected" ပေါ်ရပါမယ်၊ comment ထဲမှာ "great" မပါတဲ့ စကားလုံးနဲ့ စမ်းရင် "No positive keyword found" ပေါ်မယ်

## ၅ — နံပါတ် ခန့်မှန်းချက် စစ်ဆေးပါ

`guess` variable ထဲမှာ `7` ထည့်ပါ။ `guess` က `10` ထက် ကြီးရင် "Too high"၊ `10` ထက် နည်းရင် "Too low"၊ ညီရင် "Correct" ပြပါ။

**Hints:**
- Condition သုံးခု ကို `elif` နဲ့ တွဲသုံးပါ
- ညီမည်ကို စစ်ဖို့ `==` သုံးပါ

**လိုအပ်တဲ့ ရလဒ်:** `guess = 7` မှာ "Too low" ပေါ်ရပါမယ်။ `guess = 10` ပြောင်းရင် "Correct" ပေါ်ရပါမယ်။

**Expected behavior:** "Too low" ပေါ်ရပါမယ်၊ `guess = 10` ပြောင်း run ရင် "Correct" ပေါ်မယ်

## ၆ — Age Group ခွဲခြားပါ

`age` variable ထဲမှာ မိမိကြိုက်တဲ့ တန်ဖိုးထည့်ပါ။ အသက် `13` ထက် နည်းရင် "Child"၊ `13` မှ `19` အတွင်း ဖြစ်ရင် "Teenager"၊ `19` ထက် ကြီးရင် "Adult" ပြပါ။ `age` တန်ဖိုးကို သုံးမျိုး ပြောင်းပြီး စမ်းကြည့်ပါ။

**Hints:**
- Teenager စစ်ဖို့ `age >= 13 and age <= 19` လို့ရော၊ `elif 13 <= age <= 19` လို့ရာ ရေးနိုင်ပါတယ်
- ပထမဆုံး `True` ဖြစ်တဲ့ branch ပဲ အလုပ်လုပ်တာကို အားထားပါ

**လိုအပ်တဲ့ ရလဒ်:** အသက်အလိုက် သင့်တော်တဲ့ အုပ်စု တစ်ခုထဲပဲ ပေါ်ရပါမယ်။

**Expected behavior:** အသက်အလိုက် "Child" ဒါမှမဟုတ် "Teenager" ဒါမှမဟုတ် "Adult" တစ်ခုထဲပဲ ပေါ်ရပါမယ်

