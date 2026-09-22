# Solutions — uv Package Manager လေ့ကျင့်ခန်းများ

## လေ့ကျင့်ခန်း ၁ — Solution

**အဓိကအယူအဆ** — `uv --version` command တစ်ခုတည်းနဲ့ install status စစ်လို့ရသည်။

```bash
# Check if uv is installed and show its version
uv --version
# Expected output: something like "uv 0.5.x (home dir)"
```

## လေ့ကျင့်ခန်း ၂ — Solution

**အဓိကအယူအဆ** — `uv init` က project folder, `main.py`, `pyproject.toml` တို့ကို အလိုအလျောက် ဖန်တီးပေးသည်။

```bash
# Create a new project called first_project
uv init first_project

# Move into the project folder
cd first_project

# List the files inside the project
ls
# Expected output: main.py pyproject.toml  (plus other files)
```

## လေ့ကျင့်ခန်း ၃ — Solution

**အဓိကအယူအဆ** — `uv add` နဲ့ package ထည့်ပြီးမှ import လုပ်လို့ရသည်။ `uv run` က environment ကို အလိုအလျောက် သုံးပေးသည်။

```bash
# Add the rich package to the project
uv add rich
```

```python
# main.py
# Import the rich library for colorful terminal output
from rich import print

# Print a styled message with blue bold text
print("[bold blue]My uv project works![/bold blue]")
# Expected output: bold blue text in the terminal
```

```bash
# Run the script inside the project environment
uv run main.py
```

## လေ့ကျင့်ခန်း ၄ — Solution

**အဓိကအယူအဆ** — `uv add` နဲ့ ထည့်လိုက်တဲ့ package တွေက `pyproject.toml` ထဲက `dependencies` section မှာ မှတ်တမ်းတင်သည်။

```bash
# Open pyproject.toml in a text editor
# (use any editor you like)
```

`pyproject.toml` ထဲမှာ ဒီလို မြင်ရမည်:

```toml
# pyproject.toml (relevant part)
[project]
dependencies = [
    "rich",
]
```

Package တွေက ဒီ list ထဲမှာ တစ်ခုချင်းစီ ရောင်းနေမည်။ Project က ဘယ် package တွေ သုံးနေလဲ ဆိုတာ ဒီ file တစ်ခုတည်းနဲ့ သိနိုင်သည်။

## လေ့ကျင့်ခန်း ၅ — Solution

**အဓိကအယူအဆ** — AI project setup လည်း `uv` workflow အတိုင်းပင် — `uv init` -> `uv add numpy` -> `uv run`။

```bash
# Create a new AI starter project
uv init ai_starter

# Move into the project
cd ai_starter

# Add numpy, a core library for AI work
uv add numpy
```

```python
# main.py
# Import numpy for numerical operations
import numpy as np

# Create a small array of numbers (like simple data)
data = np.array([10, 20, 30, 40, 50])

# Calculate and print the average of the data
print("Average:", np.mean(data))
# Expected output: Average: 30.0
```

```bash
# Run the script
uv run main.py
```

## လေ့ကျင့်ခန်း ၆ — Solution

**အဓိကအယူအဆ** — Workflow တစ်ခုလုံး ကိုယ့်ကိုယ်ကိုယ် လုပ်နိုင်ရင် `uv` ကို စိတ်ကျေနပ်စွာ သုံးနိုင်ပြီ။ ဥပမာ တစ်ခု အောက်မှာ ပြထားသည်။

```bash
# Step 1: create a project with a custom name
uv init my_experiment
cd my_experiment

# Step 2: add a package of your choice
uv add rich
```

```python
# main.py
# A simple personal experiment script
from rich import print

# Print a welcome banner for the project
print("[bold magenta]Welcome to my experiment![/bold magenta]")
# Expected output: bold magenta welcome message
```

```bash
# Step 3: run the script
uv run main.py
```

Workflow မှန်ကန်စွာ လိုက်နာတတ်ရင် နောက်အခါ AI project ကြီးတွေကိုပင် ဒီနည်းအတိုင်း စတင်နိုင်မည်။
