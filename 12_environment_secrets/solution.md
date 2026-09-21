# အဖြေများ — Environment & Secrets

## ၁ — Environment Variable ဖတ်ခြင်း

Terminal မှာ သတ်မှတ်ပါ —

```bash
export MY_NAME="Aung Aung"
```

Python code —

```python
import os

# Read the MY_NAME environment variable
my_name = os.environ.get("MY_NAME")

print("Hello,", my_name)
# Expected output: Hello, Aung Aung
```

**Key idea —** `os.environ.get()` က system environment variable ကို နာမည်နဲ့ ဖတ်ယူတာပါ။

## ၂ — Key ရှိ/မရှိ စစ်ခြင်း

```python
import os

# Read the key; returns None if it is not set
api_key = os.environ.get("API_KEY")

if api_key:
    print("Key found")
else:
    print("Key missing")
# Expected output (not set): Key missing
```

**Key idea —** `get()` က variable မရှိရင် `None` ပြန်လို့ `if` နဲ့ စစ်လို့ ရပါတယ်။

## ၃ — `.env` File ဖန်တီးပြီး ဖတ်ခြင်း

`.env` file —

```
OPENAI_API_KEY=test-key-123
```

Python code —

```python
import os
from dotenv import load_dotenv

# Load variables from the .env file
load_dotenv()

# Now read it like a normal environment variable
api_key = os.environ.get("OPENAI_API_KEY")

print(api_key)
# Expected output: test-key-123
```

**Key idea —** `load_dotenv()` က `.env` file ထဲက value တွေကို environment variable အဖြစ် ရောက်စေပါတယ်။

## ၄ — Project Structure ဆောက်ခြင်း

`.env` file —

```
DATABASE_URL=postgres://localhost/mydb
```

`.gitignore` file —

```
.env
```

`main.py` —

```python
import os
from dotenv import load_dotenv

# Load secrets from the .env file
load_dotenv()

# Read the database URL
db_url = os.environ.get("DATABASE_URL")

print("Connecting to:", db_url)
# Expected output: Connecting to: postgres://localhost/mydb
```

**Key idea —** `.gitignore` မှာ `.env` ထည့်ထားရင် secret တွေ Git ဆီ တင်မိတော့ပါ။

## ၅ — AI Agent Setting File ဖန်တီးခြင်း

`.env` file —

```
OPENAI_API_KEY=test-key-123
MODEL_NAME=gpt-4o-mini
```

Python code —

```python
import os
from dotenv import load_dotenv

# Load settings from the .env file
load_dotenv()

# Read both settings
api_key = os.environ.get("OPENAI_API_KEY")
model_name = os.environ.get("MODEL_NAME")

if api_key:
    # Show only the first few characters of the key
    print("Using model:", model_name)
    print("API key ends with:", api_key[-4:])
else:
    print("No API key found.")
# Expected output:
# Using model: gpt-4o-mini
# API key ends with: -123
```

**Key idea —** Setting တွေအားလုံးကို `.env` တစ်ခုထဲ စုသိမ်းပြီး key အပြည့်အစုံကို မပြပါနဲ့။

## ၆ — Safety Check Function

`.env` file —

```
OPENAI_API_KEY=test-key-123
```

Python code —

```python
import os
from dotenv import load_dotenv


def check_secrets():
    # Load the .env file first
    load_dotenv()

    # Stop the program if the key is missing
    api_key = os.environ.get("OPENAI_API_KEY")
    if not api_key:
        raise SystemExit("Error: OPENAI_API_KEY is missing in .env")


def main():
    # Check secrets before doing any work
    check_secrets()
    print("All secrets ready. Starting the AI agent...")


main()
# Expected output: All secrets ready. Starting the AI agent...
```

**Key idea —** Program အစမှာ secret စစ်ပြီးမှ ဆက်လုပ်တာက နောက်ပိုင်းမှာ မှားယွင်းမှုကို ကြိုတင်ကာကွယ်ပေးပါတယ်။
