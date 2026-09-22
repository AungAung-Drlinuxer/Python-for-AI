# လေ့ကျင့်ခန်းများ

အောက်ပါ လေ့ကျင့်ခန်းများကို လွယ်ကူတာကနေ ခက်ခဲတာဆီ အစီအစဉ်နဲ့ လုပ်ကြည့်ပါ။

## ၁။ Project Folder Structure တည်ဆောက်ပါ

Task: `sales_analysis` ဆိုတဲ့ project folder အောက်မှာ `data` folder နဲ့ `output` folder တို့ကို Python code သုံးပြီး တည်ဆောက်ပါ။

Hints: `os.makedirs()` ကို `exist_ok=True` နဲ့ သုံးကြည့်ပါ။

Expected behavior: Program လုပ်တဲ့အခါ folder နှစ်ခု ပေါ်လာပြီး နောက်ထပ် run ရင် error မထွက်ပါ။

**Hints:** `os.makedirs()` ကို `exist_ok=True` parameter နဲ့ တွဲသုံးပြီး nested folder တွေကို တစ်ခါတည်း ဖန်တီးနိုင်ပါတယ်။

**Expected behavior:** Program ကို run တဲ့အခါ `sales_analysis` folder အောက်မှာ `data` နဲ့ `output` folder နှစ်ခု ပေါ်လာပြီး ဒီ code ကို နောက်တစ်ကြိမ် ပြန် run ရင်ပါ error မထွက်တော့ပါဘူး။

## ၂။ Path တည်ဆောက်ပြီး File ရှိမရှိ စစ်ပါ

Task: `pathlib` သုံးပြီး `data/sales.csv` path ကို တည်ဆောက်ပါ။ File ရှိလျှင် "File found"၊ မရှိရင် "File missing" ထုတ်ပြပါ။

Hints: `Path("data") / "sales.csv"` နဲ့ `.exists()` method ကို သုံးပါ။

Expected behavior: File ရှိ/မရှိ အပေါ်မူတည်ပြီး မှန်ကန်တဲ့ message ထွက်ပါ။

**Hints:** `Path("data") / "sales.csv"` နဲ့ `.exists()` method ကို သုံးပြီး `if` / `else` နဲ့ စစ်ပါ။

**Expected behavior:** ပရိုဂရမ်ကို လည်ပတ်စေတဲ့အခါ `data/sales.csv` file ရှိနေလျှင် "File found" ဆိုတဲ့ message ထွက်ပြီး၊ file မရှိပါက "File missing" ဆိုတဲ့ message ထွက်ပြရမည်။

## ၃။ CSV File ရေးပြီး ဖတ်ပါ

Task: `data/sales.csv` ထဲမှာ `product` နဲ့ `amount` column ပါတဲ့ data ၃ ကြောင်း ရေးပါ။ ပြီးရင် အဲဒီ file ကို ပြန်ဖတ်ပြီး row တိုင်းကို print လုပ်ပါ။

Hints: `csv.writer` နဲ့ရေးပါ၊ `csv.DictReader` နဲ့ ဖတ်ပါ။

Expected behavior: CSV ဖိုင်တည်ရှိပြီး ဖတ်တဲ့အခါ row တိုင်း dictionary ပုံစံနဲ့ ထွက်ပါ။

**Hints:** `csv` module ထဲက `writer()` / `DictReader()` ကို `open()` နဲ့ တွဲသုံးပြီး `newline` parameter ကို သတိထားပါ။

**Expected behavior:** `data/sales.csv` ဖိုင်ကို ဖန်တီးပြီးနောက် ပြန်ဖတ်လိုက်တဲ့အခါ `product` နဲ့ `amount` key ပါတဲ့ dictionary ၃ ခုကို တစ်ခုစီ အလီလီ print ထုတ်ပြနိုင်ပါမယ်။

## ၄။ Total တွက်ပြီး JSON မှာ Save လုပ်ပါ

Task: CSV ထဲက amount တွေအားလုံး ပေါင်းပြီး `{"total": ...}` ပုံစံနဲ့ `output/summary.json` မှာ save လုပ်ပါ။

Hints: `int()` နဲ့ string ကို number ပြောင်းပါ။ `json.dump()` ကို `indent=2` နဲ့ သုံးပါ။

Expected behavior: JSON file ထဲမှာ total တန်ဖိုး မှန်ကန်စွာ သိမ်းခံရပါ။

**Hints:** CSV file ကိုဖတ်တဲ့အခါ `csv.DictReader` ကိုသုံးပြီး `amount` column တန်ဖိုးကို `int()` နဲ့ number အဖြစ်ပြောင်း၊ total ကို loop ပတ်ပေါင်းပြီး `json.dump()` ကို `indent=2` ထည့်သုံးပါ။

**Expected behavior:** လေ့ကျင့်ခန်းပြီးဆုံးတဲ့အခါ `output/summary.json` ဖိုင်ကို ဖွင့်ကြည့်လိုက်ရင် `{"total": <CSV ထဲက amount အားလုံးပေါင်းလဒ်>}` ဆိုတဲ့ JSON ပုံစံအတိအကျ၊ `indent=2` နဲ့ format လုပ်ထားတဲ့ အနေနဲ့ total တန်ဖိုး မှန်ကန်စွာ တွေ့ရမှာ ဖြစ်ပါတယ်။

## ၅။ Code ကို Function တွေအဖြစ် ပြန်စုပါ

Task: Exercise ၃ နဲ့ ၄ က code တွေကို `read_sales()`, `calculate_total()`, `save_summary()` function သုံးခုအဖြစ် ပြန်ရေးပါ။ `main()` function ကနေ အစဉ်လိုက် ခေါ်ပါ။

Hints: Function တစ်ခုက အလုပ်တစ်ခုပဲ လုပ်ပါ။ Parameter နဲ့ return value ကို သေချာ စဉ်းစားပါ။

Expected behavior: `main()` ကို run လိုက်တာနဲ့ ရှေ့ကလို ရလဒ်တူ ထွက်ပါ။

**Hints:** `def` keyword နဲ့ function တွေကို သီးသန့်ရေးပြီး `return` နဲ့ တန်ဖိုးပြန်ပေးပါ၊ `main()` ထဲမှာ အစဉ်လိုက် ခေါ်ယူပါ။

**Expected behavior:** `main()` function ကို run လိုက်ရင် `read_sales()` က sales data တွေကိုဖတ်ပြီး၊ `calculate_total()` က စုစုပေါင်းကိုတွက်ချက်ကာ၊ `save_summary()` က အနှစ်ချုပ်ဖိုင်ကိုသိမ်းဆည်းပြီး Exercise ၃ နဲ့ ၄ မှာရခဲ့တဲ့ ရလဒ်အတိုင်း အတူတူထွက်ပါလိမ့်မယ်။

## ၆။ Product Report Function တစ်ခု ထပ်ထည့်ပါ

Task: `build_report(rows)` ဆိုတဲ့ function ရေးပါ။ CSV rows တွေကနေ product တစ်ခုချင်းစီရဲ့ စုစုပေါင်း amount ကို dictionary အဖြစ် ပြန်ပေးပါ။ ရလဒ်ကို `output/report.json` မှာ save လုပ်ပါ။

Hints: Dictionary ထဲမှာ product ရှိရင် ပေါင်း၊ မရှိရင် အသစ်ထည့်ပါ။ AI agent တစ်ခုကို data ပေးပြီး ဆုံးဖြတ်ခိုင်းရင် ဒီလို report ပုံစံက အသုံးဝင်ပါတယ်။

Expected behavior: Product တိုင်းရဲ့ total ပါတဲ့ JSON file ရပါ။

**Hints:** Loop နဲ့ rows တွေကို ထပ်ကြည့်ပြီး dictionary ထဲ `in` keyword (သို့) `.get()` method ကို သုံးပြီး total စုပေါက်ပါ၊ ပြီးရင် `json.dump()` နဲ့ save လုပ်ပါ။

**Expected behavior:** CSV rows တွေကို loop လုပ်ပြီး product တစ်ခုချင်းစီရဲ့ amount တွေကို ပေါင်းစည်းထားတဲ့ dictionary ကို `build_report(rows)` က ပြန်ပေးပြီး `output/report.json` file ထဲမှာ product နာမည်တွေနဲ့ စုစုပေါင်း total amount တွေကို JSON format အဖြစ် မြင်ရပါမယ်။

