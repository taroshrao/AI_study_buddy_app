<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# help me create a readme file for github repo for the following assignment:

Assignment:

🤖 Make Your Own AI Chatbot for Study – AI Study Buddy 📚

1️⃣ Save the Python file

Create a Python file named ai_study_buddy_streamlit.py and paste the following code inside:

import streamlit as st
import requests
import urllib.parse

st.set_page_config(page_title="AI Study Buddy", layout="centered")
st.title("📘 AI Study Buddy")

API_BASE_URL = "https://skillcaptain.app/unicorn/p/llm/openai"
USER_ID = "48"

def query_skillcaptain(prompt):
try:
encoded_prompt = urllib.parse.quote(prompt)
url = f"{API_BASE_URL}?userId={USER_ID}\&prompt={encoded_prompt}"
response = requests.get(url, headers={"Content-Type": "application/json"})
if response.status_code == 200:
return response.text
else:
return f"API Error {response.status_code}: {response.text}"
except Exception as e:
return f"Exception: {str(e)}"

mode = st.sidebar.selectbox("Choose a mode", ["Ask a Question", "Summarize Notes", "Generate MCQs"])

if mode == "Ask a Question":
question = st.text_area("Enter your question:")
if st.button("Get Answer"):
if question.strip():
prompt = question.strip()
result = query_skillcaptain(prompt)
st.success("Answer:")
st.write(result)

elif mode == "Summarize Notes":
notes = st.text_area("Paste your notes:")
if st.button("Summarize"):
if notes.strip():
prompt = f"Summarize the following notes:\n{notes.strip()}"
result = query_skillcaptain(prompt)
st.success("Summary:")
st.write(result)

elif mode == "Generate MCQs":
topic = st.text_input("Enter a topic for MCQs:")
if st.button("Generate"):
if topic.strip():
prompt = f"Generate 3 multiple choice questions (with answers) on the topic: {topic.strip()}"
result = query_skillcaptain(prompt)
st.success("Generated MCQs:")
st.write(result)

2️⃣ Set up your environment and run the app

🔹 For Mac/Linux users:

Open Terminal and run:

# Create and enter a folder

mkdir AI_study_buddy_app
cd AI_study_buddy_app

# Move your Python file into this folder (manually or via command)

# Create a virtual environment

python3 -m venv venv
source venv/bin/activate

# Install required packages

pip install streamlit requests

# Run the Streamlit app

streamlit run ai_study_buddy_streamlit.py

🔹 For Windows users:

Open Command Prompt or PowerShell and run:

:: Create and enter a folder
mkdir AI_study_buddy_app
cd AI_study_buddy_app

:: Move your Python file into this folder (manually or via File Explorer)

:: Create a virtual environment
python -m venv venv
venv\Scripts\activate

:: Install required packages
pip install streamlit requests

:: Run the Streamlit app
streamlit run ai_study_buddy_streamlit.py

3️⃣ Using the app

- After running, your browser will open the app at http://localhost:8501.
- Use the sidebar to choose one of the modes:

• Ask a Question: Type your question and click Get Answer.
• Summarize Notes: Paste notes and click Summarize.
• Generate MCQs: Enter a topic and click Generate.

4️⃣ Submission:
Click on "Submit via link" and submit your GitHub repository link

Here’s a README.md file template for your GitHub repository based on the assignment:

```markdown
# AI Study Buddy – Your Personalized Study Chatbot 🤖📚

A Streamlit-powered web application that acts as your AI study assistant. Ask questions, summarize notes, or generate multiple-choice questions (MCQs) on any topic—all through a simple web interface.

---

## Features

- **Ask a Question**: Get answers to your study-related queries.
- **Summarize Notes**: Paste your notes and receive a concise summary.
- **Generate MCQs**: Enter a topic and get three multiple-choice questions with answers.

---

## How to Run the App

### 1. Prerequisites

- **Python 3.7 or higher**
- **pip** installed

### 2. Setup Instructions

#### For Mac/Linux Users

```


# Create and enter a folder

mkdir AI_study_buddy_app
cd AI_study_buddy_app

# Move your Python file into this folder manually or via command

# Create a virtual environment

python3 -m venv venv
source venv/bin/activate

# Install required packages

pip install streamlit requests

# Run the Streamlit app

streamlit run ai_study_buddy_streamlit.py

```

#### For Windows Users

```

:: Create and enter a folder
mkdir AI_study_buddy_app
cd AI_study_buddy_app

:: Move your Python file into this folder manually or via File Explorer

:: Create a virtual environment
python -m venv venv
venv\Scripts\activate

:: Install required packages
pip install streamlit requests

:: Run the Streamlit app
streamlit run ai_study_buddy_streamlit.py

```

---

## Using the App

1. **After running the app**, your browser will open at `http://localhost:8501`.
2. **Choose a mode** from the sidebar:
   - **Ask a Question**: Type your question and click "Get Answer".
   - **Summarize Notes**: Paste your notes and click "Summarize".
   - **Generate MCQs**: Enter a topic and click "Generate".

---

## File Structure

```

AI_study_buddy_app/
├── ai_study_buddy_streamlit.py    \# Main application file
└── venv/                          \# (Optional) Virtual environment directory

```

---

## Notes

- **You need an internet connection** to use the chatbot, as it queries an external API.
- **Customize the `USER_ID` and `API_BASE_URL`** in the code if required by your provider.

---

## Submission

**Submit your GitHub repository link** as instructed by your assignment.

---
```

This README provides clear instructions for setup, usage, and submission, making it easy for anyone to clone and run your project.

