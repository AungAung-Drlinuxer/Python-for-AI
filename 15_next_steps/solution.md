# ဖြေရှင်းချက်များ — Next Steps: Course Summary & AI Agents

## လေ့ကျင့်ခန်း ၁ — Course Skills စာရင်း

အဓိကအကြောင်းအရာမှာ list တစ်ခုဖန်တီးပြီး `for` loop ဖြင့် တစ်ခုချင်း ထုတ်ပြခြင်း ဖြစ်ပါသည်။

```python
# List of core skills learned in the course
skills = [
    "Variables and data types",
    "Functions",
    "Loops",
    "Dictionaries",
    "AI basics with Python"
]

# Print each skill one by one
for skill in skills:
    print(skill)
# Expected output:
# Variables and data types
# Functions
# Loops
# Dictionaries
# AI basics with Python
```

## လေ့ကျင့်ခန်း ၂ — မိမိ Course Recap Function

အဓိကအကြောင်းအရာမှာ `if/elif/else` ဖြင့် topic အလိုက် ကွဲပြားသော အဖြေပြန်ခြင်း ဖြစ်ပါသည်။

```python
# A function that gives a recap message for a topic
def recap(topic):
    if topic == "python":
        return "Python basics completed"
    elif topic == "ai":
        return "AI fundamentals completed"
    else:
        return "Unknown topic"

# Test the function
print(recap("python"))
# Expected output: Python basics completed
print(recap("ai"))
# Expected output: AI fundamentals completed
print(recap("java"))
# Expected output: Unknown topic
```

## လေ့ကျင့်ခန်း ၃ — Feedback Form

အဓိကအကြောင်းအရာမှာ dictionary ဖန်တီးပြီး `.items()` ဖြင့် loop လုပ်ခြင်း ဖြစ်ပါသည်။

```python
# A dictionary holding course feedback
feedback = {
    "overall": "Good",
    "hardest_topic": "Functions",
    "suggestion": "Add more exercises"
}

# Print each key and value pair
for key, value in feedback.items():
    print(f"{key}: {value}")
# Expected output:
# overall: Good
# hardest_topic: Functions
# suggestion: Add more exercises
```

## လေ့ကျင့်ခန်း ၄ — Feedback Rating စစ်ဆေးခြင်း

အဓိကအကြောင်းအရာမှ် နံပါတ်အပိုင်းအကွက် (range) ကို စစ်ဆေးခြင်း ဖြစ်ပါသည်။

```python
# Check if a rating is between 1 and 5
def check_rating(rating):
    if 1 <= rating <= 5:
        return "Valid rating"
    else:
        return "Invalid rating"

# Test the function
print(check_rating(5))
# Expected output: Valid rating
print(check_rating(9))
# Expected output: Invalid rating
```

## လေ့ကျင့်ခန်း ၅ — Simple AI Agent (အလွယ်)

အဓိကအကြောင်းအရာမှာ `in` operator ဖြင့် command ထဲရှိ စာလုံးကို ရှာဖွေပြီး ဆုံးဖြတ်ချက်ချခြင်း ဖြစ်ပါသည်။

```python
# A very simple agent that responds to commands
def simple_agent(command):
    if "hello" in command:
        return "Hello! I am your agent."
    elif "summary" in command:
        return "Summary feature"
    else:
        return "Unknown command"

# Test the agent
print(simple_agent("say hello"))
# Expected output: Hello! I am your agent.
print(simple_agent("give me a summary"))
# Expected output: Summary feature
print(simple_agent("dance"))
# Expected output: Unknown command
```

## လေ့ကျင့်ခန်း ၆ — Agent Task List

အဓိကအကြောင်းအရာမှာ task list တစ်ခုကို loop ဖြင့် လုပ်ဆောင်ပြီး agent function ကို တစ်ခုချင်း ခေါ်ခြင်း ဖြစ်ပါသည်။

```python
# Reuse the simple_agent function from exercise 5
def simple_agent(command):
    if "hello" in command:
        return "Hello! I am your agent."
    elif "summary" in command:
        return "Summary feature"
    else:
        return "Unknown command"

# A list of tasks for the agent
tasks = [
    "say hello to the user",
    "create a summary of the lesson",
    "delete all files"
]

# Process each task through the agent
for task in tasks:
    response = simple_agent(task)
    print(f"Task: {task}")
    print(f"Agent: {response}")
# Expected output:
# Task: say hello to the user
# Agent: Hello! I am your agent.
# Task: create a summary of the lesson
# Agent: Summary feature
# Task: delete all files
# Agent: Unknown command
```

ဤဖြေရှင်းချက်များကို လေ့လာပြီးပါက သင်ခန်းကြားမှု၏ အဓိက skills များကို အတည်ပြုနိုင်ပြီး၊ AI agents ဆက်လက်သင်ယူရန် အသင့်ပြင်ဆင်နိုင်ပါသည်။
