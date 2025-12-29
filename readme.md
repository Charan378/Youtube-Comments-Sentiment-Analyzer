# 🎥 YouTube Comment Sentiment Analysis Bot

This project is a **Robotic Process Automation (RPA) bot** that automates sentiment analysis of YouTube video comments.  
It fetches comments using the **YouTube Data API**, performs sentiment analysis with **Google Gemini Pro**, stores results in a CSV, and delivers a rich **HTML email report**.

---

## ✨ Features
- **Interactive Input** → Prompts user for YouTube video URL & Gemini API key.  
- **Dynamic Video ID Extraction** → Parses video ID from URL.  
- **AI-Powered Sentiment Analysis** → Uses Gemini Pro API.  
- **Robust Error Handling** → Try...Catch blocks for resilience.  
- **Data Export** → Saves results into `sentiment.csv`.  
- **HTML Email Reporting** → Sends a professional email report with a formatted table.  
- **Secure Authentication** → Uses safe email credential handling.

---

## ⚙️ Workflow
1. **Get User Inputs & Initialize**
   - Prompts for YouTube URL and Gemini API Key.
   - Extracts `videoId` from URL.
   - Starts error handling.

2. **Fetch YouTube Comments**
   - Calls YouTube Data API (`commentThreads` endpoint).
   - Extracts top-level comments.

3. **Analyze Sentiment with Gemini API**
   - Sends comments to Gemini Pro.
   - Receives sentiment predictions.

4. **Build Data Table & CSV**
   - Creates table with `Comment` + `Sentiment`.
   - Exports results to `sentiment.csv`.

5. **Generate & Send HTML Email Report**
   - Builds HTML `<table>` report.
   - Sends via SMTP (with `IsBodyHtml = true`).

6. **Final Confirmation & Error Management**
   - Displays *"Process Completed Successfully and Report Sent"*.
   - Handles exceptions gracefully.

---

## 🚀 Getting Started

### Prerequisites
- An RPA platform (e.g., **UiPath**, **Automation Anywhere**) capable of HTTP requests.
- **Google API Key** → [Get from Google Cloud Console](https://console.cloud.google.com/).  
- **Gemini API Key** → [Get from Google AI Studio](https://aistudio.google.com/).  
- **SMTP Credentials** (e.g., Gmail with App Password).

### Configuration
Set these variables in your RPA tool:

| Variable              | Example Value                         |
|------------------------|---------------------------------------|
| `YOUTUBE_API_KEY`     | `AIza...`                            |
| `SMTP_HOST`           | `smtp.gmail.com`                     |
| `SMTP_PORT`           | `587`                                |
| `SENDER_EMAIL`        | `your_email@gmail.com`               |
| `RECIPIENT_EMAIL`     | `recipient@example.com`              |
| `SENDER_EMAIL_PASSWORD` | App Password / Credential Store     |

---

## 🛠️ How to Run
```bash
# Clone the repository
git clone https://github.com/varshanth-c/Youtube-Comments-Sentiment-Analyzer.git

# Open the project in your RPA tool
# Run the main workflow

