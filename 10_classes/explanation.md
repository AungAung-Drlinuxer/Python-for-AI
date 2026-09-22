# Classes — Object-Oriented Python (ရှင်းလင်းချက်)

ဒီ file မှာ class တွေ ဘယ်လို အလုပ်လုပ်လဲ၊ ဘာကြောင့် လိုအပ်လဲဆိုတာကို အဆင့်ဆင့် ရှင်းပြပါမယ်။

---

## ၁။ Class နှင့် Object ဆိုတာ ဘာလဲ

### ဘာကို ဆိုလိုတာလဲ

Class ဆိုသည်မှာ object တစ်ခု ဖန်တီးရန် blueprint (အကြောင်းပြုစည်းမျဉ်း) ဖြစ်ပါသည်။ Blueprint ကိုယ်တိုင်က အိမ် မဟုတ်ပါ။ ဒါပေမယ့် အဲဒီ blueprint အတိုင်း အိမ်အများကြီး ဆောက်နိုင်ပါတယ်။ တူညီပါတယ် — class က blueprint ဖြစ်ပြီး၊ class ကနေ ဖန်တီးထားတဲ့ အရာတစ်ခုချင်းစီက object (သို့ instance) ဖြစ်ပါတယ်။

### ဘာကြောင့် လဲ

Program ရှည်လာတဲ့အခါ data တွေနှင့် function တွေက အနှံ့အပြား ကွဲပြားသွားပါတယ်။ တစ်ခုနဲ့တစ်ခု ဆက်စပ်နေတဲ့ data နှင့် လုပ်ဆောင်ချက်တွေကို တစ်နေရာတည်းမှာ စုစည်းထားခြင်းအားဖြင့် ကုဒ်ကို စနစ်တကျ စီမံနိုင်ပါတယ်။ Toolbox (ကိရိယာဘူး) ဥပမာနှင့် တူပါသည် — ကိရိယာတွေကို မျိုးအလိုက် ဘူးတွေထဲ သီးသန့်ထည့်ထားသလိုပါပဲ။

### ဘယ်လို အလုပ်လုပ်လဲ

Python မှာ class ကို `class` keyword နဲ့ ရေးပါတယ်။ Class ကနေ object ဖန်တီးရန် class နာမည်ကို function ခေါ်သလို ခေါ်ပါတယ်။ Object တစ်ခုစီမှာ ကိုယ်ပိုင် data တွေ ရှိပါတယ်။

### ဥပမာ

```python
# Define a simple class as a blueprint
class Student:
 pass

# Create objects (instances) from the class
student_a = Student()
student_b = Student()

# Each object is independent
print(student_a)  # <__main__.Student object at 0x...>
print(student_b)  # <__main__.Student object at 0x...>
```

Object နှစ်ခုက တစ်ခုနှင့်တစ်ခု မတူပါ။ တူညီတဲ့ blueprint ကနေ လာပေမယ့် အသီးသန့် ဖြစ်ကြပါတယ်။

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI project မှာ `OpenAIClient` လို class တွေကို တစ်ခါရေးပြီးရင် project အနှံ့ ပြန်သုံးနိုင်ပါတယ်။ အသုံးပြုသူတိုင်းက အတူတူ blueprint ကနေ ကိုယ်ပိုင် client object ဆောက်ပြီး သုံးကြတာပါ။

---

## ၂။ Attributes နှင့် Methods

### ဘာကို ဆိုလိုတာလဲ

Attribute က object ထဲက data ဖြစ်ပါတယ်။ Method က object ထဲက လုပ်ဆောင်ချက် (function) ဖြစ်ပါတယ်။ Class ဆိုတဲ့ blueprint ထဲမှာ data (attributes) နှင့် လုပ်ဆောင်ချက် (methods) နှစ်မျိုးလုံး ပါဝင်ပါတယ်။

### ဘာကြောင့် လဲ

Data နှင့် အဲဒီ data ကို ကိုင်တွယ်တဲ့ လုပ်ဆောင်ချက်တွေက သီးခြားစီ ရှိနေရင် ကုဒ်က ရှုပ်ထွေးသွားပါတယ်။ အတူတူ စုစည်းထားရင် လွယ်ကူသလို ပြင်ဆင်ရလည်း လွယ်ပါတယ်။

### ဘယ်လို အလုပ်လုပ်လဲ

`__init__` ဆိုတာ special method တစ်ခုဖြစ်ပြီး object ဖန်တီးချိန်မှာ အလိုအလျောက် ခေါ်ပါတယ်။ ဒီနေရာမှာ object ရဲ့ အစပြု data တွေကို သတ်မှတ်ပေးပါတယ်။ `self` က လက်ရှိ object ကို ကိုယ်စားပြုပါတယ်။

### ဥပမာ

```python
# A class representing an AI client
class OpenAIClient:
    def __init__(self, api_key):
        # Store the API key as an attribute
        self.api_key = api_key

    def generate(self, prompt):
        # A method that uses the object's attribute
        return f"Key {self.api_key} -> Response for: {prompt}"

# Create an object; __init__ runs automatically
client = OpenAIClient("sk-test-123")
print(client.api_key)          # sk-test-123
print(client.generate("Hello"))  # Key sk-test-123 -> Response for: Hello
```

Object တစ်ခုစီမှာ `api_key` သီးသန့် ရှိပါတယ်။ Method တစ်ခုချင်းစီရဲ့ ပထမ parameter က `self` ဖြစ်ရပါတယ်။

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI library အများစုမှာ ဒီပုံစံအတိုင်း — `__init__` မှာ setup လုပ်ပြီး method တွေနဲ့ အလုပ်လုပ်တဲ့ — client class တွေပါပါတယ်။ ဒီ pattern ကို နားလည်ရင် ဘယ် library မှာမဆို မြန်မြန် လေ့လာနိုင်ပါတယ်။

---

## ၃။ Inheritance (ဆက်ခံခြင်း)

### ဘာကို ဆိုလိုတာလဲ

Inheritance ဆိုသည်မှာ class အသစ်တစ်ခုက ရှိပြီးသား class (parent) ရဲ့ attributes နှင့် methods တွေကို ဆက်ခံယူခြင်းဖြစ်ပါတယ်။ ပြီးရင် လိုအပ်တဲ့ အပိုင်းတွေကိုပဲ ထပ်ဖြည့်ရေးပါတယ်။

### ဘာကြောင့် လဲ

တူညီတဲ့ လုပ်ဆောင်ချက်တွေကို နောက်ထပ် ထပ်မရေးရပါ။ Parent class မှာ အထွက် ရေးထားပြီး child class တွေက ငြိမ်ငြိမ် သုံးလို့ရပါတယ်။ Code ထပ်တူများ လျှော့ပြီး 유စိုးမှု လွယ်ပါတယ်။

### ဥပမာ

```python
# Parent class
class AIModel:
    def __init__(self, name):
        self.name = name

    def describe(self):
        return f"Model: {self.name}"

# Child class inherits from AIModel
class ChatModel(AIModel):
    def chat(self, message):
        # Only ChatModel has this method
        return f"{self.name} says: reply to '{message}'"

# ChatModel can use both inherited and new methods
model = ChatModel("gpt-mini")
print(model.describe())            # Model: gpt-mini
print(model.chat("Hi there"))     # gpt-mini says: reply to 'Hi there'<|assistant|>
```

`ChatModel` ထဲမှာ `describe` ကို မရေးထားပေမယ့် parent ဆီကနေ ဆက်ခံရလို့ အလုပ်လုပ်ပါတယ်။

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI tool တွေမှာ အမျိုးမျိုးသော model တွေ (chat model၊ image model) ရှိပါတယ်။ အတူတူဖြစ်တဲ့ အပိုင်းတွေကို base class မှာ ရေးပြီး မတူတဲ့ အပိုင်းတွေကို child class တွေမှာ ရေးရင် စနစ်တကျ ဖြစ်ပါတယ်။

---

## ၄။ ဘယ်အချိန်မှာ Class သုံးသင့်လဲ

### ဘာကို ဆိုလိုတာလဲ

Program တစ်ခုရဲ့ ကြီးထွားလာပုံကို ကြည့်ပြီး function နဲ့ ရေးမလဲ class နဲ့ ရေးမလဲဆိုတာ ဆုံးဖြတ်ရပါတယ်။

### ဘာကြောင့် လဲ

Class တွေက ချက်ချင်း လိုအပ်တဲ့ အရာ မဟုတ်ပါ။ ပုံမှန် တိုးတက်ပုံက — single-file script နဲ့ စပြီး၊ ရှုပ်လာရင် functions နဲ့ ခွဲရေး၊ ပြီးရင် multiple files သုံး၊ နောက်ဆုံးမှာ state နဲ့ ပြန်လည်အသုံးပြုနိုင်တဲ့ အစိတ်အပိုင်းတွေ များလာတဲ့အခါ classes နဲ့ ပြောင်းရေးခြင်း ဖြစ်ပါတယ်။

### ဘယ်လို ဆုံးဖြတ်မလဲ

- Program တိုရင် script လောက် လုံလောက်ပါတယ်။
- ထပ်ခိုက်နေတဲ့ logic ရှိရင် functions နဲ့ ခွဲပါ။
- Object တွေက state (အခြေအနေ data) သိမ်းထားရရင် class သင့်ပါတယ်။
- ပြန်သုံးနိုင်တဲ့ component တွေ လိုရင် class သင့်ပါတယ်။

### ဥပမာ

```python
# A stateful counter is a good fit for a class
class RequestCounter:
    def __init__(self):
        # State stored inside the object
        self.count = 0

    def add(self):
        self.count += 1
        return self.count


counter = RequestCounter()
print(counter.add())  # 1
print(counter.add())  # 2
```

State က global variable မဟုတ်ပဲ object ထဲမှာ သီးသန့် သိမ်းထားတာကို သတိပြုပါ။

### လက်တွေ့မှာ ဘာကြောင့် အရေးကြီးလဲ

AI application တွေက stateful operation တွေ များပါတယ် — API key သိမ်းခြင်း၊ conversation history ထိန်းခြင်း၊ request အရေအတွက် မှတ်ခြင်းတို့ ဖြစ်ပါတယ်။ ဒီလို အခြေအနေ သိမ်းရတဲ့ အလုပ်တွေက class ရဲ့ အားသာချက် ဖြစ်ပါတယ်။

---

## အနှစ်ချုပ်

- Class = blueprint။ Object = blueprint ကနေ ဖန်တီးထားတဲ့ အရာ။
- Attributes = data၊ Methods = လုပ်ဆောင်ချက်။ `__init__` က object ဖန်တီးချိန်မှာ အလိုအလျောက် run ပါတယ်။
- Inheritance နဲ့ ရှိပြီး class ကနေ အသစ် ဆက်ခံနိုင်ပါတယ်။
- ရှုပ်ထွေးမှု ရှိမှသာ class သုံးပါ။ Script တိုတွေမှာ function က လုံလောက်ပါတယ်။
