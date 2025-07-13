# TaskGazeAI

# Screenshot Activity Classifier Agent

This project is a lightweight AI agent that analyzes desktop screenshots to determine the user's activity. It combines **OCR (Tesseract)**, **local LLM reasoning (Mistral via Ollama)**, and **LangChain agents** to build an intelligent activity-tracking system. Activities are grouped, timestamped, and made queryable via a simple toolset.

---

## 📊 Project Overview

The primary objective of this project is to:
- Automatically extract text from desktop screenshots.
- Use an LLM to intelligently interpret the screen's context.
- Classify activities such as `Coding`, `Browsing`, `Idle`, `YouTube`, and `Excel`.
- Maintain a log of activities with timestamps.
- Enable natural language queries on the image classification process using LangChain agents.

---

## 📁 Repository Structure

```
├── screenshots/                    # Folder containing screenshot images
├── main.py                         # Core logic and LangChain agent implementation
├── requirements.txt                # Python dependencies
└── README.md                       # Project overview and documentation
```

---

## 🔧 Tools & Technologies

- **Python** (Pillow, datetime, os, collections)
- **Tesseract OCR** (for text extraction from images)
- **Ollama** (for running the Mistral language model locally)
- **LangChain** (to build AI agents with callable tools)
- **Pytesseract** (Python wrapper for Tesseract OCR)
- **Mistral (7B)** via Ollama (for LLM-based classification)

---

## 🔍 Key Features

### 1. Image Processing & OCR
- Iterates through a folder of screenshots
- Extracts visible text using `pytesseract`

### 2. Activity Classification via LLM
- Sends extracted text to a Mistral LLM
- Returns a single label like `Coding`, `Browsing`, `YouTube`, etc.

### 3. Smart Activity Grouping
- Groups similar results into clean labels
- Handles edge cases and unknown activities

### 4. Timestamped Logging
- Associates each screenshot with its creation time
- Stores logs in memory for quick querying

### 5. Agent Tools via LangChain
- **Classify Tool**: Classifies a given screenshot
- **Summary Tool**: Gives a summary count of each activity
- **Log Tool**: Displays full activity log with timestamps

---

## 📌 How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/screenshot-activity-classifier.git
cd screenshot-activity-classifier
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

You’ll need:
- `pytesseract`
- `Pillow`
- `langchain`
- `ollama`
- `tesseract` installed locally (`.exe` path set in `main.py`)

### 3. Add Screenshots
Place your `.png`, `.jpg`, or `.jpeg` files inside the `/screenshots` directory.

### 4. Run the Agent
Run the main Python script:
```bash
python main.py
```

You can interact with the agent using natural language:
- "Classify image Screenshot_2025-07-12_211154"
- "Show me the activity summary"
- "Give me the full timestamped activity log"

---

## 📈 Results Summary

- Successfully classified screenshots into high-level user activities.
- Enabled timestamped activity tracking from visual screen content.
- Built modular LangChain tools for reusable, extensible interaction.

---

## 🚀 Future Improvements

- Build a Streamlit frontend to visualize the logs.
- Store logs in a local SQLite DB or JSON file.
- Enable multi-user tracking and session logs.

---

## 🙌 Acknowledgments

This project was built as part of my AI agent development journey using local LLMs. Special thanks to the open-source community behind:
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- [LangChain](https://github.com/langchain-ai/langchain)
- [Ollama](https://ollama.com/)

---

## 📬 Contact

For feedback or collaboration opportunities:

- GitHub: [AbdullahRao25](https://github.com/AbdullahRao25)
- Email: AbdullahKaimKhaani@gmail.com
- Linkedin: https://www.linkedin.com/in/abdullah-kaim-khaani-4336b2362/

---
