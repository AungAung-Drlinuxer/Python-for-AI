# အဖြေများ — External Tools: Packages & APIs

## လေ့ကျင့်ခန်း ၁ — Built-in Module သုံးခြင်း

**အဓိကအယူအဆ** — Built-in module ကို `import` လုပ်ရုံနဲ့ သုံးလို့ရပါတယ်။

```python
# Import the built-in math module
import math

# Calculate the square root of 25
square_root = math.sqrt(25)
print(square_root)  # Expected output: 5.0

# Print the value of pi
print(math.pi)  # Expected output: 3.141592653589793
```

---

## လေ့ကျင့်ခန်း ၂ — External Package Install လုပ်ခြင်း

**အဓိကအယူအဆ** — External package ကို အရင် install လုပ်မှ import လုပ်လို့ရပါတယ်။

Terminal မှာ ရိုက်ပါ —

```text
pip install requests
```

Python script —

```python
# Import the requests package (installed with pip)
import requests

# Print the installed version number
print(requests.__version__)  # Expected output: e.g. 2.31.0
```

---

## လေ့ကျင့်ခန်း ၃ — API ကနေ Data ယူခြင်း

**အဓိကအယူအဆ** — `requests.get()` နဲ့ API ကို ခေါ်ပြီး `.json()` နဲ့ Python dictionary အဖြစ် ပြောင်းပါ။

```python
# Import the requests package
import requests

# Send a GET request to the currency API
response = requests.get("https://api.exchangerate-api.com/v4/latest/USD")

# Convert the JSON response into a Python dictionary
data = response.json()

# Read the exchange rates from the "rates" key
rates = data["rates"]

# Print the USD to MMK rate
print("USD to MMK:", rates["MMK"])  # Expected output: e.g. 2100.0

# Print the USD to JPY rate
print("USD to JPY:", rates["JPY"])  # Expected output: e.g. 151.5
```

---

## လေ့ကျင့်ခန်း ၄ — API Key ကို လုံခြုံစွာ သုံးခြင်း

**အဓိကအယူအဆ** — API key ကို code ထဲမှာ မရေးဘဲ `.env` file ထဲမှာ သိမ်းပါ။

အရင် `pip install python-dotenv` လုပ်ပါ။ `.env` file ထဲမှာ —

```text
MY_API_KEY=hello123
```

Python script —

```python
# Import the os module to read environment variables
import os

# Import load_dotenv from the python-dotenv package
from dotenv import load_dotenv

# Load the variables from the .env file
load_dotenv()

# Read the API key from the environment
api_key = os.getenv("MY_API_KEY")
print(api_key)  # Expected output: hello123
```

---

## လေ့ကျင့်ခန်း ၅ — API Data ကို pandas နဲ့ Analyze လုပ်ခြင်း

**အဓိကအယူအဆ** — API data ကို `pandas` DataFrame အဖြစ် ပြောင်းလိုက်ရင် table လို ကိုင်တွယ်လို့ရပါတယ်။

```python
# Import requests and pandas
import requests
import pandas as pd

# Get the list of users from the public API
response = requests.get("https://jsonplaceholder.typicode.com/users")
users = response.json()

# Convert the list of dictionaries into a DataFrame
df = pd.DataFrame(users)

# Count the total number of users
print("Total users:", len(df))  # Expected output: Total users: 10

# Show only the name and email columns
print(df[["name", "email"]])
# Expected output: a table with 10 rows of names and emails
```

---

## လေ့ကျင့်ခန်း ၆ — AI Agent အတွက် Data Pipeline (Bonus)

**အဓိကအယူအဆ** — API ကနေ data ယူပြီး AI agent ကို feed လုပ်နိုင်တဲ့ format တစ်ခု ဖန်တီးပါ။

```python
# Import the requests package
import requests

# Get the list of users from the public API
response = requests.get("https://jsonplaceholder.typicode.com/users")
users = response.json()

# Take the first 5 users only
first_five = users[:5]

# Build a list of formatted strings for the AI agent
prompts = [f"User: {user['name']}" for user in first_five]

# Print the list
print(prompts)
# Expected output:
# ['User: Leanne Graham', 'User: Ervin Howell',
#  'User: Clementine Bauch', 'User: Patricia Lebsack',
#  'User: Chelsey Dietrich']
```

---

## နိဂုံးချုပ်

ဒီလေ့ကျင့်ခန်းတွေအားလုံးက module ရဲ့ အဓိက (၃) ချက်ကို လက်တွေ့လုပ်စေပါတယ် — module import လုပ်တာ၊ API ကနေ data ယူတာ၊ ရထားတဲ့ data ကို analyze လုပ်တာပါ။ ဒီအခြေခံတွေအပေါ်မှာ AI application တွေနဲ့ data pipeline တွေက တည်ဆောက်ထားပါတယ်။ နောက် module မှာ ဒီအသိစွမ်းအားတွေကို ပိုမိုနက်နဲတဲ့ project တွေထိ တိုးချဲ့သွားပါမယ်။
