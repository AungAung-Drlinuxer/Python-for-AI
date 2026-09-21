# Exercise — Git & GitHub

ဒီ exercise တွေက Git နဲ့ GitHub ရဲ့ အခြေခံအယူအဆတွေကို လက်တွေ့ လေ့ကျင့်ဖို့ ရေးထားတာပါ။

## Exercise ၁ — Version မှတ်တမ်း စနစ်တကျ ရေးခြင်း

Git မသုံးခင် ပထမဆုံး ပြဿနာကို နားလည်အောင် လေ့ကျင့်ကြမယ်။

**Task:** Python file တစ်ခုကို ကိုယ်တိုင် ရေးပြီး အဲဒီ file ရဲ့ version history ကို dictionary နဲ့ မှတ်တမ်းတင်ပါ။ version နံပါတ်၊ ရက်စွဲ၊ commit message သုံးမျိုး ထည့်ပါ။

**Hint:** Dictionary ထဲမှာ list of dictionaries ထည့်လို့ရတယ်။

**Expected behavior:** Program run ရင် version ၃ ခုရဲ့ မှတ်တမ်း စီရင်ပြီး ပေါ်လာမယ်။

## Exercise ၂ — Git Command စာရင်း ဖန်တီးခြင်း

**Task:** Git ရဲ့ အရေးကြီးတဲ့ command တွေနဲ့ အလုပ်အသီးသီးကို ဖော်ပြတဲ့ Python program တစ်ခု ရေးပါ။ အနည်းဆုံး command ၅ ခု ထည့်ပါ (ဥပမာ — `git status`, `git add`, `git commit`, `git clone`, `git push`)။

**Hint:** Dictionary မှာ key = command name၊ value = description အဖြစ် သိမ်းပါ။

**Expected behavior:** Program run ရင် command တစ်ခုစီနဲ့ ရှင်းလင်းချက် တစ်ပိုဒ်စီ ပေါ်လာမယ်။

## Exercise ၃ — Repository နာမည် URL ဆောက်ခြင်း

**Task:** GitHub username နှင့် repository နာမည်ကို လက်ခံပြီး repository ရဲ့ ပုံမှန် address (URL) ကို ထုတ်ပေးတဲ့ function တစ်ခု ရေးပါ။ Function ကို နာမည်အမျိုးမျိုးနဲ့ စမ်းပါ။

**Hint:** f-string သုံးပြီး `https://github.com/username/repo-name` ပုံစံ ဆောက်ပါ။

**Expected behavior:** `make_repo_url("aung", "chat-bot")` ကို ခေါ်ရင် `https://github.com/aung/chat-bot` ပေါ်လာမယ်။

## Exercise ၄ — Clone လုပ်မယ့် Project ရွေးချယ်ခြင်း

**Task:** AI project dictionary list တစ်ခု ရှိတယ် (နာမည်၊ star အရေအတွက်၊ language)။ Star အများဆုံး project ကို ရွေးပြီး ကိုယ့်ကွန်ပျူတာထဲ clone လုပ်သင့်တဲ့ project အဖြစ် အကြံပေးတဲ့ program ရေးပါ။

**Hint:** `max()` function ကို `key=` နဲ့ တွဲသုံးပါ။

**Expected behavior:** Program run ရင် star အများဆုံး project နာမည်နဲ့ အကြံပေးစာ ပေါ်လာမယ်။

## Exercise ၅ — Commit Message စစ်ဆေးခြင်း

**Task:** Commit message တစ်ခုက ကောင်းတဲ့ message လား မကောင်းဘူးလား စစ်ပေးတဲ့ function ရေးပါ။ စည်းကမ်း — စာလုံး ၅ လုံးထက် တိုတာ မကောင်း၊ စာလုံး ၁၀၀ ထက် ရှည်တာ မကောင်း၊ ဗလာဖြစ်နေရင် မကောင်း။

**Hint:** `len()` function နဲ့ အရှည်စစ်ပါ။

**Expected behavior:** ကောင်းရင် `valid` ပေါ်မယ်၊ မကောင်းရင် ဘာကြောင့်ဆိုတာ ပေါ်မယ်။

## Exercise ၆ — AI Project Backup Plan

**Task:** ကိုယ့်ရဲ့ AI project (ဥပမာ — chat bot script) တစ်ခုအတွက် backup အဆင့်ဆင့်ကို ဖော်ပြတဲ့ program ရေးပါ။ Project မှာ file ၃ ခု ရှိတယ် — `train.py`, `bot.py`, `data.csv`။ အဆင့်တိုင်းမှာ ဘယ် command သုံးမလဲ၊ VS Code မှာ ဘယ် button နှိပ်မလဲ ဆိုတာ ပေါ်အောင် ရေးပါ။

**Hint:** List ထဲမှာ dictionary တွေ သိမ်းပြီး loop နဲ့ ပြပါ။

**Expected behavior:** Backup အဆင့် ၅ ဆင့် ဘယ်လိုလုပ်မလဲ စီရင်ပြီး ပေါ်လာမယ်။
