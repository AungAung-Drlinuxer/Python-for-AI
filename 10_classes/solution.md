# Solutions — Classes လေ့ကျင့်ခန်းများ

---

## ၁ — ရိုးရိုး Class

`__init__` က object ဖန်တီးချိန်မှာ attributes တွေကို သတ်မှတ်ပေးတဲ့ နေရာဖြစ်ပါတယ်။

```python
class Book:
    def __init__(self, title, author):
        # Store data as attributes
        self.title = title
        self.author = author

# Create two independent objects
book_a = Book("Python Basics", "John")
book_b = Book("AI for Beginners", "Mary")

print(book_a.title)   # Python Basics
print(book_a.author)  # John
print(book_b.title)   # AI for Beginners
print(book_b.author)  # Mary
```

---

## ၂ — Method ထည့်ခြင်း

Method တစ်ခုချင်းစီရဲ့ ပထမ parameter က `self` ဖြစ်ပြီး object ရဲ့ attributes တွေကို ယူသုံးနိုင်ပါတယ်။

```python
class Book:
    def __init__(self, title, author):
        self.title = title
        self.author = author

    def describe(self):
        # Return a formatted description using attributes
        return f"{self.title} by {self.author}"

book = Book("Python Basics", "John")
print(book.describe())  # Python Basics by John
```

---

## ၃ — Attribute ပြောင်းလဲနိုင်တဲ့ Class

Object ထဲမှာ state (`count`) ကို သိမ်းထားပြီး method တိုင်း ပြောင်းလဲနိုင်ပါတယ် — ဒါက class ရဲ့ အားသာချက်ပါ။

```python
class RequestCounter:
    def __init__(self):
        # Initial state
        self.count = 0

    def add(self):
        # Update state and return the new value
        self.count += 1
        return self.count

counter = RequestCounter()
print(counter.add())  # 1
print(counter.add())  # 2
print(counter.add())  # 3
```

---

## ၄ — AI Client Class

Object တစ်ခုစီမှာ `api_key` က သီးသန့်ဖြစ်ပြီး method တွေက ကိုယ့် object ရဲ့ attribute ကိုပဲ သုံးပါတယ်။

```python
class OpenAIClient:
    def __init__(self, api_key):
        # Each object stores its own API key
        self.api_key = api_key

    def generate(self, prompt):
        # Return a fake response (no real API call)
        return f"Response to: {prompt}"

client_a = OpenAIClient("sk-key-AAA")
client_b = OpenAIClient("sk-key-BBB")

print(client_a.api_key)                # sk-key-AAA
print(client_b.api_key)                # sk-key-BBB
print(client_a.generate("Hello AI"))   # Response to: Hello AI
print(client_b.generate("What is AI?"))  # Response to: What is AI?
```

---

## ၅ — Inheritance

Child class က parent class ရဲ့ attributes နှင့် methods အားလုံးကို ဆက်ခံရပြီး လိုအပ်တာတွေကိုပဲ ထပ်ထည့်ရေးပါတယ်။

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
        # New method only for ChatModel
        return f"{self.name} replies to: {message}"

model = ChatModel("gpt-mini")
print(model.describe())          # Model: gpt-mini
print(model.chat("Hi there"))    # gpt-mini replies to: Hi there
```

---

##
