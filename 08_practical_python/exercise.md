# လေ့ကျင့်ခန်းများ

အောက်ပါ လေ့ကျင့်ခန်းများကို လွယ်ကူတာကနေ ခက်ခဲတာဆီ အစီအစဉ်နဲ့ လုပ်ကြည့်ပါ။

## ၁။ Project Folder Structure တည်ဆောက်ပါ

Task: `sales_analysis` ဆိုတဲ့ project folder အောက်မှာ `data` folder နဲ့ `output` folder တို့ကို Python code သုံးပြီး တည်ဆောက်ပါ။

Hints: `os.makedirs()` ကို `exist_ok=True` နဲ့ သုံးကြည့်ပါ။

Expected behavior: Program လုပ်တဲ့အခါ folder နှစ်ခု ပေါ်လာပြီး နောက်ထပ် run ရင် error မထွက်ပါ။

## ၂။ Path တည်ဆောက်ပြီး File ရှိမရှိ စစ်ပါ

Task: `pathlib` သုံးပြီး `data/sales.csv` path ကို တည်ဆောက်ပါ။ File ရှိလျှင် "File found"၊ မရှိရင် "File missing" ထုတ်ပြပါ။

Hints: `Path("data") / "sales.csv"` နဲ့ `.exists()` method ကို သုံးပါ။

Expected behavior: File ရှိ/မရှိ အပေါ်မူတည်ပြီး မှန်ကန်တဲ့ message ထွက်ပါ။

## ၃။ CSV File ရေးပြီး ဖတ်ပါ

Task: `data/sales.csv` ထဲမှာ `product` နဲ့ `amount` column ပါတဲ့ data ၃ ကြောင်း ရေးပါ။ ပြီးရင် အဲဒီ file ကို ပြန်ဖတ်ပြီး row တိုင်းကို print လုပ်ပါ။

Hints: `csv.writer` နဲ့ရေးပါ၊ `csv.DictReader` နဲ့ ဖတ်ပါ။

Expected behavior: CSV ဖိုင်တည်ရှိပြီး ဖတ်တဲ့အခါ row တိုင်း dictionary ပုံစံနဲ့ ထွက်ပါ။

## ၄။ Total တွက်ပြီး JSON မှာ Save လုပ်ပါ

Task: CSV ထဲက amount တွေအားလုံး ပေါင်းပြီး `{"total": ...}` ပုံစံနဲ့ `output/summary.json` မှာ save လုပ်ပါ။

Hints: `int()` နဲ့ string ကို number ပြောင်းပါ။ `json.dump()` ကို `indent=2` နဲ့ သုံးပါ။

Expected behavior: JSON file ထဲမှာ total တန်ဖိုး မှန်ကန်စွာ သိမ်းခံရပါ။

## ၅။ Code ကို Function တွေအဖြစ် ပြန်စုပါ

Task: Exercise ၃ နဲ့ ၄ က code တွေကို `read_sales()`, `calculate_total()`, `save_summary()` function သုံးခုအဖြစ် ပြန်ရေးပါ။ `main()` function ကနေ အစဉ်လိုက် ခေါ်ပါ။

Hints: Function တစ်ခုက အလုပ်တစ်ခုပဲ လုပ်ပါ။ Parameter နဲ့ return value ကို သေချာ စဉ်းစားပါ။

Expected behavior: `main()` ကို run လိုက်တာနဲ့ ရှေ့ကလို ရလဒ်တူ ထွက်ပါ။

## ၆။ Product Report Function တစ်ခု ထပ်ထည့်ပါ

Task: `build_report(rows)` ဆိုတဲ့ function ရေးပါ။ CSV rows တွေကနေ product တစ်ခုချင်းစီရဲ့ စုစုပေါင်း amount ကို dictionary အဖြစ် ပြန်ပေးပါ။ ရလဒ်ကို `output/report.json` မှာ save လုပ်ပါ။

Hints: Dictionary ထဲမှာ product ရှိရင် ပေါင်း၊ မရှိရင် အသစ်ထည့်ပါ။ AI agent တစ်ခုကို data ပေးပြီး ဆုံးဖြတ်ခိုင်းရင် ဒီလို report ပုံစံက အသုံးဝင်ပါတယ်။

Expected behavior: Product တိုင်းရဲ့ total ပါတဲ့ JSON file ရပါ။
