# လေ့ကျင့်ခန်းများ — Next Steps: Course Summary & AI Agents

ဒီလေ့ကျင့်ခန်းများသည် သင်ခန်းကြားမှုတစ်ခုလုံး၏ အချက်များကို ပြန်လည်သုံးသပ်စေပြီး၊ AI agents ဆက်လက်သင်ယူရန် ပြင်ဆင်စေပါသည်။ အလွယ်ဆုံးမှ အခက်ခဲဆုံးအထိ စီထားပါသည်။

## လေ့ကျင့်ခန်း ၁ — Course Skills စာရင်း

**တာဝန်:** ဤသင်ခန်းကြားမှုမှ အဓိက Python skills ငါးခုကို string list တစ်ခုတွင် ရေးပြီး for loop ဖြင့် တစ်ခုချင်း print ထုတ်ပါ။

**Hints:** list တစ်ခုဖန်တီးပါ။ `for` loop ကို အသုံးပြုပါ။

**မျှော်မှန်းသည့် ရလဒ်:** skills ငါးခု တစ်ကြောင်းချင်း ပေါ်ပါမည်။

## လေ့ကျင့်ခန်း ၂ — မိမိ Course Recap Function

**တာဝန်:** `recap(topic)` ဟူ၍ function တစ်ခုရေးပါ။ အကယ်၍ topic သည် "python" ဖြစ်ပါက "Python basics completed" ကို return ပါ။ "ai" ဖြစ်ပါက "AI fundamentals completed" ကို return ပါ။ အခြားအရာဖြစ်ပါက "Unknown topic" ကို return ပါ။

**Hints:** `if`, `elif`, `else` များကို အသုံးပြုပါ။

**မျှော်မှန်းသည့် ရလဒ်:** function ကို ခေါ်သည့်အခါ မှန်ကန်သော message ပြန်ပါမည်။

## လေ့ကျင့်ခန်း ၃ — Feedback Form

**တာဝန်:** `feedback` ဟူ၍ dictionary တစ်ခု ဖန်တီးပါ။ keys များမှာ `"overall"`၊ `"hardest_topic"`၊ `"suggestion"` ဖြစ်ပြီး မိမိ၏ တကယ့်အမြင်များကို values အဖြစ် ထည့်ပါ။ `for` loop ဖြင့် key နှင့် value တို့ကို `"key: value"` ပုံစံဖြင့် print ထုတ်ပါ။

**Hints:** dictionary တွင် `.items()` method ကို အသုံးပြုနိုင်ပါသည်။

**မျှော်မှန်းသည့် ရလဒ်:** feedback သုံးကြောင်း ပေါ်ပါမည်။

## လေ့ကျင့်ခန်း ၄ — Feedback Rating စစ်ဆေးခြင်း

**တာဝန်:** `check_rating(rating)` ဟူ၍ function ရေးပါ။ rating သည် 1 မှ 5 အတွင်း ဖြစ်ပါက "Valid rating" ကို return ပါ။ မဟုတ်ပါက "Invalid rating" ကို return ပါ။

**Hints:** `if 1 <= rating <= 5:` ပုံစံဖြင့် စစ်နိုင်ပါသည်။

**မျှော်မှန်းသည့် ရလဒ်:** rating 5 ပေးပါက "Valid rating" ပြန်ပါမည်။ rating 9 ပေးပါက "Invalid rating" ပြန်ပါမည်။

## လေ့ကျင့်ခန်း ၅ — Simple AI Agent (အလွယ်)

**တာဝန်:** `simple_agent(command)` ဟူ၍ function ရေးပါ။ command ထဲတွင် "hello" ပါပါက greeting တစ်ခု return ပါ။ "summary" ပါပါက "Summary feature" ဟု return ပါ။ အခြား command ဖြစ်ပါက "Unknown command" ကို return ပါ။

**Hints:** `in` operator ဖြင့် string အတွင်းရှိ စာလုံးကို စစ်နိုင်ပါသည်။

**မျှော်မှန်းသည့် ရလဒ်:** `simple_agent("say hello")` ကို ခေါ်ပါက greeting ပြန်ပါမည်။

## လေ့ကျင့်ခန်း ၆ — Agent Task List

**တာဝန်:** tasks ဟူ၍ list တစ်ခု (အနည်းဆုံး သုံးခု) ဖန်တီးပါ။ `for` loop ဖြင့် တစ်ခုချင်း လုပ်ဆောင်ပြီး၊ လေ့ကျင့်ခန်း ၅ မှ `simple_agent` function ကို အသုံးပြုပြီး တစ်ခုချင်းစီ၏ အဖြေကို print ထုတ်ပါ။

**Hints:** ပုံမှန် for loop တစ်ခုဖြင့် လုံလောက်ပါသည်။

**မျှော်မှန်းသည့် ရလဒ်:** task တစ်ခုချင်းစီအတွက် agent ၏ တုံ့ပြန်မှု ပေါ်ပါမည်။
