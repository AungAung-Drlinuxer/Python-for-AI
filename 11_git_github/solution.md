# Solution — Git & GitHub

## Exercise ၁ — Version မှတ်တမ်း စနစ်တကျ ရေးခြင်း

**အဓိကအယူအဆ** — Git က လုပ်တာက version တွေကို စနစ်တကျ မှတ်တမ်းတင်တာ ဖြစ်တယ်။

```python
# Keep a record of file versions like Git does
history = [
    {"version": 1, "date": "2024-01-05", "message": "first version of train.py"},
    {"version": 2, "date": "2024-01-07", "message": "fix data loading bug"},
    {"version": 3, "date": "2024-01-09", "message": "add accuracy report"},
]

# Print every saved version
for entry in history:
 print(f"Version {entry['version']} ({entry['date']}): {entry['message']}")

# Expected output:
# Version 1 (2024-01-05): first version of train.py
# Version 2 (2024-01-07): fix data loading bug
# Version 3 (2024-01-09): add accuracy report
```

## Exercise ၂ — Git Command စာရင်း ဖန်တီးခြင်း

**အဓိကအယူအဆ** — တကယ်လိုအပ်တဲ့ Git command က ၅-၆ ခုပဲ ရှိတယ်။

```python
# The essential Git commands for a beginner
commands = {
    "git status": "See which files changed",
    "git add": "Select files to save",
    "git commit": "Save a version with a message",
    "git clone": "Download a project from GitHub",
    "git push": "Upload your commits to GitHub",
}

# Print each command with its purpose
for name, desc in commands.items():
 print(f"{name:15} -> {desc}")

# Expected output:
# git status      -> See which files changed
# git add         -> Select files to save
# git commit      -> Save a version with a message
# git clone       -> Download a project from GitHub
# git push        -> Upload your commits to GitHub
```

## Exercise ၃ — Repository URL ဆောက်ခြင်း

**အဓိကအယူအဆ** — GitHub repository တိုင်းမှာ ပုံမှန် URL ပုံစံ တစ်ခု ရှိတယ်။

```python
def make_repo_url(username, repo_name):
    # Build the standard GitHub repository address
 return f"https://github.com/{username}/{repo_name}"

# Test the function with different names
print(make_repo_url("aung", "chat-bot"))
print(make_repo_url("mya", "image-classifier"))

# Expected output:
# https://github.com/aung/chat-bot
# https://github.com/mya/image-classifier
```

## Exercise ၄ — Clone လုပ်မယ့် Project ရွေးချယ်ခြင်း

**အဓိကအယူအဆ** — အခြားသူရဲ့ project တွေထဲကမှ စိတ်ဝင်စားစရာကောင်းတာ ရွေးတတ်ဖို့ လိုတယ်။

```python
# A list of AI projects found on GitHub
projects = [
    {"name": "tiny-agent", "stars": 2400, "language": "Python"},
    {"name": "chat-bot-kit", "stars": 5100, "language": "Python"},
    {"name": "data-cleaner", "stars": 900, "language": "Python"},
]

# Define the helper BEFORE using it
def make_repo_url(username, repo_name):
    # Helper to build a GitHub URL
 return f"https://github.com/{username}/{repo_name}"

# Find the project with the most stars
best = max(projects, key=lambda p: p["stars"])

print(f"Recommended project: {best['name']} ({best['stars']} stars)")
print(f"Clone it with: git clone {make_repo_url('user', best['name'])}.git")

# Expected output:
# Recommended project: chat-bot-kit (5100 stars)
# Clone it with: git clone https://github.com/user/chat-bot-kit.git
```

## Exercise ၅ — Commit Message စစ်ဆေးခြင်း

**အဓိကအယူအဆ** — ကောင်းတဲ့ commit message က နောက်ကြည့်တဲ့အခါ ဘာပြင်ခဲ့လဲ ပြောပြနိုင်ရတယ်။

```python
def check_commit_message(message):
    # Check if a commit message follows the rules
    if len(message) == 0:
        return "Invalid: message is empty"
    if len(message) < 5:
        return "Invalid: message is too short"
    if len(message) > 100:
        return "Invalid: message is too long"
    return "Valid"


# Test with different messages
print(check_commit_message(""))                  # Empty message
print(check_commit_message("ok"))                # Too short
print(check_commit_message("fix data loading bug"))  # Good message

# Expected output:
# Invalid: message is empty
# Invalid: message is too short
# Valid
```

## Exercise ၆ — AI Project Backup Plan

**အဓိကအယူအဆ** — AI project တစ်ခုကို Git နဲ့ GitHub မှာ backup လုပ်တဲ့ အဆင့်တွေက command အနည်းငယ်နဲ့ပဲ ပြီးတယ်။

```python
# Five-step backup plan for a small AI project
project_files = ["train.py", "bot.py", "data.csv"]

steps = [
    {"step": 1, "action": "Check what changed", "command": "git status"},
    {"step": 2, "action": "Stage the project files", "command": "git add train.py bot.py data.csv"},
    {"step": 3, "action": "Record a clear commit", "command": 'git commit -m "Add backup plan"'},
    {"step": 4, "action": "Push to GitHub", "command": "git push origin main"},
    {"step": 5, "action": "Verify the remote copy", "command": "git log --oneline -1"},
]

print("Backup plan for:", ", ".join(project_files))
for item in steps:
    print(f'{item["step"]}. {item["action"]}  ->  {item["command"]}')
```

**မျှော်မှန်ရလဒ်:**

```text
Backup plan for: train.py, bot.py, data.csv
1. Check what changed  ->  git status
2. Stage the project files  ->  git add train.py bot.py data.csv
3. Record a clear commit  ->  git commit -m "Add backup plan"
4. Push to GitHub  ->  git push origin main
5. Verify the remote copy  ->  git log --oneline -1
```

Step တစ်ခုချင်းကို dictionary အဖြစ် list ထဲမှာ သိမ်းထားတဲ့အတွက် အဆင့်အသစ် ထပ်ထည့်ချင်ရင် dictionary တစ်ခု
ထပ်ဖြည့်ရုံပါ — loop က ကျန် output ကို အလိုအလျောက် ဆက်ထုတ်ပေးမယ်။ Backup plan ကို data အဖြစ် ထားခြင်းက
အဆင့်တွေကို version control ထဲမှာ ပြန်စစ်လို့ရစေပြီး၊ script ကို ပြန်ရေးစရာ မလိုတော့ပါ။
