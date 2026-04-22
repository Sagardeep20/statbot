# Statbot - AI Codebase Assistant

Statbot is an AI-powered codebase assistant that runs directly in your terminal. It analyzes your code, finds bugs, explains logic, and helps you fix issues using Google Gemini AI.

---

## Quick Demo

```
$ python -m statbot.statbot
---------------------------------
| Welcome to Statbot!                |
| Your AI Codebase Assistant         |
---------------------------------
Working directory: /your/project
Codebase loaded: 18 files, ~23K tokens
Multi-language support: Python, JavaScript, TypeScript, C++, Java, Rust, Go, and more!
You: analyze demo_code.py
```

---

## Features

- Multi-Language Support - Analyzes 17 programming languages
- Bug Detection - Finds bugs with exact line numbers
- Auto-Fix Suggestions - Provides corrected code
- Code Explanation - Explains complex logic
- Socratic Coaching - Guides you to fix bugs yourself
- Context-Aware - Reads entire codebase at once

### Supported Languages

Python, JavaScript, TypeScript, C, C++, Java, HTML, CSS, JSON, YAML, TOML, XML, Rust, Go, Bash, Markdown, Plain Text

---

## Installation

### Prerequisites

- Python 3.10+
- Gemini API Key (free)

### Step 1: Clone the Project

```bash
git clone https://github.com/Sagardeep20/statbot.git
cd statbot
```

### Step 2: Install Dependencies

```bash
pip install -e .
```

### Step 3: Get Free API Key

1. Go to: https://aistudio.google.com/apikey
2. Click "Create API key"
3. Copy the key

### Step 4: Save API Key

Create a .env file in the project root:

```
GEMINI_API_KEY=your_api_key_here
```

---

## How to Use

### Basic Usage

```bash
python -m statbot.statbot
```

### Commands Inside Statbot

| Command | Example | Description |
|---------|---------|-------------|
| analyze | analyze main.py | Find bugs in file |
| explain | explain utils.py | Explain the code |
| iterate | iterate app.py | Socratic coaching |
| exit | exit | Quit Statbot |

### Example Sessions

#### 1. Find Bugs
```
You: analyze statbot/demo_code.py
Found: Infinite loop at line 19
Fix: Change high = mid to high = mid - 1
```

#### 2. Explain Code
```
You: explain main.py
Explains what each function does
```

#### 3. Socratic Learning
```
You: iterate algorithm.py
Hint: Check your loop condition
Fix it yourself, then type: reiterate
```

---

## Project Structure

```
statbot/
├── statbot/
│   ├── __init__.py
│   ├── statbot.py          - Main application
│   ├── demo_code.py       - Demo with bugs
│   ├── demo_code.cpp      - C++ demo
│   ├── demo_code.js      - JavaScript demo
│   └── language_support/  - Language detection
│       ├── detection.py
│       ├── profiles.py
│       ├── prompt_builder.py
│       └── registry.py
├── test_language_support.py  - Unit tests
├── pyproject.toml       - Package config
├── README.md
└── .env.example
```

---

## Run Tests

```bash
pip install pytest
python -m pytest test_language_support.py -v
```

Test Results: 73/73 PASSED

---

## What Makes Statbot Special?

### 1. Multi-Language Detection
Automatically detects Python, JavaScript, C++, Java, and 13 more languages.

### 2. Bug Pattern Database
Each language has specific bug patterns:
- Python: Mutable defaults, bare except, late binding
- JavaScript: == vs ===, var closures, missing await
- C++: Buffer overflow, memory leaks, null pointers

### 3. Precise Line Numbers
Finds exact line numbers and provides fixes.

### 4. Free to Use
Uses Google's free tier Gemini API.

---

## License

MIT License

---

## Author

Group-24 project

---

## Acknowledgments

- Google Gemini AI (https://ai.google/) - Powered by Gemini
- Rich Library (https://github.com/Textualize/rich) - Beautiful CLI output