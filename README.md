

# 🎥 YouTube Comment Sentiment Analysis Bot

An RPA-powered automation bot that fetches YouTube video comments, analyzes their sentiment using Google Gemini Pro, stores results in a CSV file, and delivers a rich HTML email report.

This project demonstrates how RPA, APIs, and Generative AI can be combined to create an end-to-end intelligent automation solution.


## ✨ Features

Interactive Input
Prompts the user for a YouTube video URL and Gemini API key.

Dynamic Video ID Extraction
Automatically parses the videoId from the provided YouTube URL.

AI-Powered Sentiment Analysis
Uses Google Gemini Pro API to classify comment sentiment.

Robust Error Handling
Implements Try/Catch logic for fault-tolerant execution.

Data Export
Saves comment sentiment results to sentiment.csv.

HTML Email Reporting
Sends a professional email report with a formatted HTML table.

Secure Authentication
Supports safe email credential handling (App Passwords / Credential Store).

---

## ⚙️ Workflow

### 1️⃣ Get User Inputs & Initialize

Prompts for:

* YouTube Video URL
* Gemini API Key

Extracts videoId from the URL.
Initializes error handling.

### 2️⃣ Fetch YouTube Comments

Calls the YouTube Data API (commentThreads endpoint).
Extracts top-level comments.

### 3️⃣ Analyze Sentiment with Gemini Pro

Sends comments to the Gemini Pro API.
Receives sentiment predictions (Positive, Negative, Neutral).

### 4️⃣ Build Data Table & CSV

Creates a structured table with:

* Comment Text
* Sentiment

Exports results to sentiment.csv.

### 5️⃣ Generate & Send HTML Email Report

Builds an HTML table with sentiment results.
Sends the report via SMTP (IsBodyHtml = true).

### 6️⃣ Final Confirmation & Error Management

Displays:
Process Completed Successfully and Report Sent

Handles exceptions gracefully with meaningful error messages.

---

## 🚀 Getting Started

### 🔧 Prerequisites

An RPA platform capable of HTTP requests
(UiPath, Automation Anywhere, etc.)

YouTube Data API Key
Obtain from Google Cloud Console

Gemini API Key
Obtain from Google AI Studio

SMTP Credentials
(e.g., Gmail with App Password enabled)

---

## 🔑 Configuration

Set the following variables in your RPA tool:

Variable Name | Example Value
YOUTUBE_API_KEY | AIza...
SMTP_HOST | smtp.gmail.com
SMTP_PORT | 587
SENDER_EMAIL | [your_email@gmail.com](mailto:your_email@gmail.com)
RECIPIENT_EMAIL | [recipient@example.com](mailto:recipient@example.com)
SENDER_EMAIL_PASSWORD | App Password / Credential Store

---

## 📂 Output

CSV File
sentiment.csv

Email Report
HTML formatted table
Sent automatically upon successful execution

---

## 🛡️ Error Handling

API failures (YouTube / Gemini)
Invalid video URLs
Email delivery issues
Network or authentication errors

All exceptions are caught and logged without crashing the workflow.

---

## 📌 Use Cases

Social media sentiment monitoring
Brand reputation analysis
Customer feedback insights
AI-powered automation demos
RPA + GenAI proof-of-concept projects

---

## 📜 License

This project is provided for educational and demonstration purposes.
Feel free to modify and extend it as needed.

---
