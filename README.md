

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

## Using the App

1. **After running the app**, your browser will open at `http://localhost:8501`.
2. **Choose a mode** from the sidebar:
   - **Ask a Question**: Type your question and click "Get Answer".
   - **Summarize Notes**: Paste your notes and click "Summarize".
   - **Generate MCQs**: Enter a topic and click "Generate".

## File Structure

```

AI_study_buddy_app/
├── ai_study_buddy_streamlit.py    \# Main application file
└── venv/                          \# (Optional) Virtual environment directory

```

## Notes

- **You need an internet connection** to use the chatbot, as it queries an external API.
- **Customize the `USER_ID` and `API_BASE_URL`** in the code if required by your provider.

---

## Submission

**Submit your GitHub repository link** as instructed by your assignment.

```

