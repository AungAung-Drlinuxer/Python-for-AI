# Functions — ပြန်သုံးနိုင်တဲ့ Code Block တွေ

ဒီ file မှာ function ရဲ့ အခြေခံ သုံးသတ္တိကို အဆင့်ဆင့် ရှင်းပြပါမယ်။

---

## Topic ၁ — Function ကို Define လုပ်ခြင်း

### ဘာကို ဆိုလိုတာလဲ

Function ဆိုတာ code command တွေကို အမည်တစ်ခုနဲ့ စုထားတဲ့ block တစ်ခုဖြစ်တယ်။ လိုက်နာနိုင်တဲ့ ဟင်းချက်နည်း (recipe) လိုမျိုး — တစ်ခေါက် ရေးပြီးရင် အမည်နဲ့ ခေါ်ရုံပဲ။

### ဘာကြောင့် လဲ

တူညီတဲ့ code ကို ထပ်ရေးနေရင် "DRY" မူ (Don't Repeat Yourself) ချိုးသလို ဖြစ်တယ်။ Function နဲ့ ရေးထားရင် — ၁) code ထပ်စရာ မလိုဘူး၊ ၂) project မှာ order ရှိရှိ စီမံလို့ရတယ်၊ ၃) bug ရှိရင် function တစ်နေရာမှာပဲ ပြင်ရတယ်၊ ၄) ခွဲခြားပြီး သီးသန့် စမ်းသပ်လို့ရတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

`def` keyword နဲ့ စပြီး အမည်ပေး၊ ကောက်ကွင်း `(` `)` နဲ့ colon `:` တင်ရတယ်။ အောက်မှာ indent လုပ်ထားတဲ့ code တွေက function ရဲ့ ကိုယ်ထည်ဖြစ်တယ်။ ခေါ်သုံးချင်ရင် အမည်နောက်မှာ `()` ထည့်ပြီး ခေါ်ရတယ်။

### ဥပမာ

```python
# Define a simple function with no parameters
def greet():
 print("Hello from the function!")

# Call the function twice
greet()
greet()
# Expected output:
# Hello from the function!
# Hello from the function!
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

`print()` နဲ့ `len()` တို့ဟာ Python မှာ ရှိပြီးသား built-in function တွေဖြစ်တယ်။ ကိုယ်ပိုင် function တွေ (ဥပမာ — `calculate_tax()`, `send_email()`) ရေးတတ်သွားရင် ကိုယ့် project ကို သန့်သန့်ရှင်ရှင် စီမံနိုင်မယ်။

---

## Topic ၂ — Parameters (Function ရဲ့ Input)

### ဘာကို ဆိုလိုတာလဲ

Parameter ဆိုတာ function ထဲကို ပို့လိုက်တဲ့ input ဖြစ်တယ်။ Function က စက်လိုမျိုး — input တစ်ခု ထည့်ပြီးရင် output တစ်ခု ရတယ်။

### ဘာကြောင့် လဲ

Parameter မပါရင် function တစ်ခုက အမြဲတမ်း အတူတူပဲ လုပ်ရတယ်။ Parameter ပါရင်တော့ function တစ်ခုတည်းနဲ့ ကွဲပြားတဲ့ အချက်အလက်များစွာကို ဆက်ဆံနိုင်တယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Function ရဲ့ ကောက်ကွင်းထဲမှာ variable အမည်တွေ ရေးပြီး define လုပ်တယ်။ ခေါ်တဲ့အခါ တကယ့် တန်ဖိုး (argument) တွေ အစားထိုးပေးရတယ်။ Parameter တွေ တစ်ခုထက် ပိုလည်း ရေးလို့ရတယ်။

### ဥပမာ

```python
# Define a function that takes two parameters
def greet_person(name, greeting):
 print(greeting + ", " + name + "!")

# Call it with different arguments
greet_person("Aung", "Hello")
greet_person("Su", "Hi")
# Expected output:
# Hello, Aung!
# Hi, Su!
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI နဲ့ data project တွေမှာ တူညီတဲ့ လုပ်ငန်းစဉ်ကို input ကွဲပြားလို့ ထပ်ခါထပ်ခါ သုံးရတတ်တယ် — ဥပမာ message အမျိုးမျိုးကို စစ်ဆေးတာ၊ dataset အမျိုးမျိုးကို ဖတ်တာ။ Parameter နဲ့ ရေးထားရင် function တစ်ခုပဲ လုံလောက်တယ်။

---

## Topic ၃ — Return Values (Function ရဲ့ Output)

### ဘာကို ဆိုလိုတာလဲ

Return value ဆိုတာ function က အလုပ်လုပ်ပြီးရင် ပြန်ပေးတဲ့ ရလဒ်ဖြစ်တယ်။ `print()` က မျက်နှာပြင်မှာ ပြတာပဲ။ `return` ကတော့ တန်ဖိုးကို ကိုယ့် program ထဲ ပြန်ပေးတာဖြစ်တယ်။

### ဘာကြောင့် လဲ

`return` မသုံးရင် function ရဲ့ ရလဒ်ကို နောက်ထပ် ဆက်သုံးလို့မရဘူး။ ရလဒ်ကို variable တစ်ခုမှာ သိမ်းပြီး တွက်ချက်မှုအသစ်မှာ ဆက်သုံးချင်ရင် `return` က မဖြစ်မနေ လိုအပ်တယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

Function ကိုယ်ထည်ထဲမှာ `return` keyword နောက် ပြန်ချင်တဲ့ တန်ဖိုးကို ရေးရတယ်။ ခေါ်တဲ့အခါ တန်ဖိုးကို variable တစ်ခုမှာ သိမ်းလို့ရတယ်။

### ဥပမာ

```python
# Define a function that returns a value
def calculate_tax(price, rate):
 tax = price * rate
 return tax

# Store the returned value and use it
tax_amount = calculate_tax(10000, 0.05)
total = 10000 + tax_amount
print("Tax:", tax_amount)
print("Total:", total)
# Expected output:
# Tax: 500.0
# Total: 10500.0
```

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

`len("hello")` ကို ခေါ်တဲ့အခါ `5` ဆိုတဲ့ တန်ဖိုး ပြန်ရတယ် — ဒါက return value ဖြစ်တယ်။ ကိုယ်ပိုင် function တွေမှာလည်း `return` သုံးတတ်သွားရင် ရလဒ်တွေကို ချိတ်ဆက်ပြီး ပိုကြီးတဲ့ တွက်ချက်မှုတွေ တည်ဆောက်နိုင်မယ်။

---

## အနှစ်ချုပ်

- `def` နဲ့ function ကို define လုပ်တယ်၊ အမည်နဲ့ `()` ခေါ်တယ်။
- Parameter တွေက function ရဲ့ input ဖြစ်တယ်။
- `return` က function ရဲ့ output ကို ပြန်ပေးတယ်။
