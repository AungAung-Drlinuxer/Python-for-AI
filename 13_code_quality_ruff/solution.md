# ဖြေရှင်းချက်များ — Formatting with Ruff

## ၁ — Style ပြဿနာများ ရှာဖွေခြင်း

```python
# The style violations found by eye:
# 1. No space after comma: (a,b) should be (a, b)
# 2. No spaces around = and + operators
# 3. The variable c is unnecessary (style note)

def add(a, b):
    c = a + b
    return c
```

**Key idea** — operator နှင့် comma ပတ်ဝန်းကျင် space ထည့်ခြင်းသည် PEP 8 ၏ အခြေခံကျသော rule ဖြစ်သည်။

## ၂ — Ruff Format လုပ်ပြီး နှိုင်းယှဉ်ခြင်း

Format လုပ်ပြီးသည့် code —

```python
# After Ruff formatting (save the file in VS Code)
def greet(name):
    message = "Hi " + name
    return message


def double(x):
    return x * 2
```

**Key idea** — Ruff က save လုပ်သည့်အခါ space များထည့်ပြီး function များကြား blank line နှစ်ကြောင်း ချပေးသည်။

## ၃ — Indent ၄ ခုဖြင့် ရေးခြင်း

```python
# Correct PEP 8 indentation: 4 spaces per level
def check_score(score):
    if score >= 90:
        return "Excellent"
    else:
        return "Keep learning"


print(check_score(95))   # Expected: Excellent
print(check_score(50))   # Expected: Keep learning
```

**Key idea** — nesting အလိုက် space ၄ ခုစီထည့်ခြင်းဖြင့် code block များကို ရှင်းလင်းစွာ ခွဲခြားနိုင်သည်။

## ၄ — Import Sorting

Ruff စီပေးပြီးသည့် code —

```python
# After Ruff sorts imports alphabetically
import math
import os
import sys

result = math.sqrt(16)
print(result)     # Expected: 4.0
print(os.name)    # Expected: posix or nt
print(sys.version)  # Expected: your Python version string
```

**Key idea** — import များကို alphabet အလိုက် စီပေးခြင်းက file ထဲပါသည့် dependency များကို တစ်ကြည့်တည်းနားလည်စေသည်။

## ၅ — Line Length စစ်ဆေးခြင်း

Ruff ခွဲပေးပြီးသည့် code —

```python
# Ruff splits the long line to stay within the 88 character limit
def build_prompt(system_message, user_message, temperature, max_tokens):
    prompt = (
        "System: "
        + system_message
        + " User: "
        + user_message
        + " Temp: "
        + str(temperature)
        + " Tokens: "
        + str(max_tokens)
    )
    return prompt


print(build_prompt("You are helpful.", "Hello!", 0.7, 100))
```

**Key idea** — line ရှည်လွန်းပါက Ruff က parenthesized string concatenation ဖြင့် ခွဲပေးသည်။

## ၆ — AI Agent Prompt Builder

```python
# Build a one-shot prompt for an AI agent, formatted cleanly by Ruff
def build_agent_prompt(agent_name, task, tools):
    tool_list = ", ".join(tools)
    prompt = (
        f"Agent: {agent_name}\n"
        f"Task: {task}\n"
        f"Available tools: {tool_list}"
    )
    return prompt


# Example usage
result = build_agent_prompt(
    "DataBot",
    "Summarize the dataset",
    ["search", "calculator", "file_reader"],
)
print(result)
# Expected output:
# Agent: DataBot
# Task: Summarize the dataset
# Available tools: search, calculator, file_reader
```

**Key idea** — AI agent prompt တည်ဆောက်သည့် function ကို ရေးပြီး Ruff format က  code block များ ရှင်းလင်းအဆင်ပြေအောင် အလိုအလျောက် ပြင်ပေးသည်။
