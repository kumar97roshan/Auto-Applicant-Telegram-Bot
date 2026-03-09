# Auto-Applicant-Telegram-Bot
This is an automated Python Telegram bot that turbocharges your job application process! Simply take a screenshot of a job posting, send it to the bot via Telegram, and it will:
1. Contact Google Gemini AI to extract the email address, hiring manager's name, and job role via advanced OCR.
2. Read your personal CV and automatically draft a tailored cover letter demonstrating why you are a great fit.
3. Automatically email the hiring manager directly with the cover letter and your CV attached.

![Architecture Diagram](https://raw.githubusercontent.com/yourusername/telegram_job_bot/main/telegram_bot_architecture.png)
*(Note: Be sure to upload `telegram_bot_architecture.png` to your repo!)*

## 🛠️ Features
- **Zero-Friction Applying:** See a job ad on LinkedIn or Twitter? Just snap a screenshot on your phone and forward it to your bot.
- **Smart Data Extraction:** Powered by Google's cutting-edge Gemini 2.5 Flash vision model to intelligently extract contact info from messy screenshots.
- **Custom-Tailored Pitches:** Gemini compares the job requirements with your personal CV to write a highly focused, professional cover letter body.
- **Background Execution:** Fully asynchronous—handles the heavy Gemini AI text generation in a background thread so the Telegram event loop never freezes.

## 🚀 Setup & Installation

**1. Clone the repository**
```bash
git clone https://github.com/yourusername/telegram_job_bot.git
cd telegram_job_bot
```

**2. Install requirements**
```bash
pip install -r requirements.txt
```

**3. Configure Environment Variables**
Rename `.env.example` to `.env` and fill in your actual API keys and credentials:
```env
TELEGRAM_BOT_TOKEN=your_telegram_bot_token_here
GEMINI_API_KEY=your_gemini_api_key_here
GMAIL_ADDRESS=your_email@gmail.com
GMAIL_APP_PASSWORD=your_16_digit_app_password
CV_FILE_PATH=./Your_CV_File.pdf
```
*(Need a Gmail App Password? Go to your Google Account Settings -> Security -> 2-Step Verification -> App Passwords)*

**4. Add your CV**
Place your Resume/CV into the same directory and make sure the `CV_FILE_PATH` in the `.env` file points to it exactly. Python `docx` and `PyPDF2` formats are supported.

## 🏃 Running the Bot

Run the bot script:
```bash
python bot.py
```

Then open Telegram, find your bot, and send it a screenshot! 📸

## ☁️ Cloud Hosting (Optional)
This bot is perfectly suited to be hosted on a cloud platform like **PythonAnywhere** so that it can remain online 24/7 without needing your PC to stay on. 
*(Note: PythonAnywhere's free tier blocks outgoing SMTP emails. You will need a paid plan or use an alternative like Render or an AWS EC2 instance).*

## 📄 License
This project is open-source. Feel free to fork and customize the email signature or AI prompts to fit your needs!
