# အဖြေများ — Data Types

## လေ့ကျင့်ခန်း ၁ — Accuracy နှင့် Loss ကိန်းများ

အဓိက အယူအဆ: float နှင့် int ကိန်းတွေကို variable ထဲ တိုက်ရိုက် သိမ်းလို့ ရပါတယ်။

```python
# Store a float and an int
accuracy = 0.85  # float value
epochs = 5       # int value

print(accuracy)  # 0.85
print(epochs)    # 5
```

အဓိကအယူအဆ — float နှင့် int ကိန်းများကို variable ထဲတွင် တိုက်ရိုက်သိမ်းဆည်းနိုင်သည်။

## လေ့ကျင့်ခန်း ၂ — Model Name String

အဓိက အယူအဆ: string တွေကို `+` နဲ့ ပေါင်းလို့ ရပါတယ်။

```python
# Store a string and join two strings
model_name = "GPT-4"

full_message = model_name + " is ready"
print(full_message)  # GPT-4 is ready
```

အဓိကအယူအဆ — string များကို `+` ဖြင့် ဆက်စပ်ပေါင်းလှန်နိုင်သည်။

## လေ့ကျင့်ခန်း ၃ — Confidence Check (Boolean)

အဓိက အယူအဆ: `>` နဲ့ နှိုင်းယှဉ်ရင် `True` ဒါမှမဟုတ် `False` ရပါတယ်။

```python
# Compare a float with a threshold
confidence = 0.92

is_confident = confidence > 0.90
print(is_confident)  # True, because 0.92 is greater than 0.90
```

အဓိကအယူအဆ — `>` ဖြင့် နှိုင်းယှဉ်ခြင်းအားဖြင့် `True` သို့မဟုတ် `False` ကို ရရှိသည်။

## လေ့ကျင့်ခန်း ၄ — type() နဲ့ Type စစ်တာ

အဓိက အယူအဆ: `type()` က value တစ်ခုရဲ့ data type ကို ပြပါတယ်။

```python
# Check the type of different values
print(type(42))      # <class 'int'>
print(type(3.14))    # <class 'float'>
print(type('Hello')) # <class 'str'>
print(type(True))    # <class 'bool'>
```

အဓိကအယူအဆ — `type()` သည် value တစ်ခု၏ data type ကို ပြသသည်။

## လေ့ကျင့်ခန်း ၅ — String ကိန်းကို ပြောင်းပြီး တွက်တာ

အဓိက အယူအဆ: string ထဲက ကိန်းကို တွက်ချင်ရင် `int()` နဲ့ အရင် ပြောင်းရပါတယ်။

```python
# Convert a string to an int before doing math
score_text = "25"

score = int(score_text) + 5
print(score)  # 30
```

အဓိကအယူအဆ — string ထဲရှိကိန်းကို တွက်ချက်ချင်း `int()` ဖြင့် အရင်ပြောင်းရသည်။

## လေ့ကျင့်ခန်း ၆ — AI Agent Message Builder

အဓိက အယူအဆ: float ကို string နဲ့ ပေါင်းချင်ရင် `str()` နဲ့ ပြောင်းပြီးမှ ပေါင်းရပါတယ်။

```python
# Build a message from a float confidence score
confidence = 0.88

# Check the type first
print(type(confidence))  # <class 'float'>

# Convert the float to a string and join it with text
message = "Confidence: " + str(confidence)
print(message)  # Confidence: 0.88
```


အဓိကအယူအဆ — float ကို string နှင့် ပေါင်းချင်ပါက `str()` ဖြင့် ပြောင်းပြီးမှ ပေါင်းရသည်။

