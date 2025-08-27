/*
# 🐦 AI Tweet Summary Agent

Automated Twitter analysis and email reporting system deployed on Vercel.

## Features

- ⏰ Runs every 4 hours automatically via Vercel Cron
- 🐦 Fetches latest tweets from specified Twitter account
- 🤖 Uses Google Gemini AI for intelligent summarization
- 📧 Sends beautiful HTML email reports
- 🚀 Serverless deployment on Vercel

## Setup Instructions

### 1. Clone and Install

```bash
npm install
```

### 2. Environment Variables

Set up the following environment variables in Vercel dashboard:

- `TWITTER_BEARER_TOKEN`: Your Twitter API Bearer Token
- `GOOGLE_API_KEY`: Your Google AI API key
- `GMAIL_USER`: Your Gmail address
- `GMAIL_APP_PASSWORD`: Gmail App Password (not regular password)
- `TARGET_TWITTER_USERNAME`: Username to monitor (without @)
- `RECIPIENT_EMAIL`: Email to receive summaries

### 3. API Keys Setup

**Twitter API:**
1. Go to https://developer.twitter.com
2. Create a new app
3. Get your Bearer Token

**Google AI API:**
1. Go to https://makersuite.google.com/app/apikey
2. Create a new API key

**Gmail App Password:**
1. Enable 2FA on your Google account
2. Generate an App Password for this application

### 4. Deploy to Vercel

```bash
vercel --prod
```

### 5. Manual Testing

Visit: `https://your-app.vercel.app/api/tweet-summary`

## How It Works

1. **Cron Trigger**: Vercel cron runs every 4 hours
2. **Tweet Fetching**: Gets latest 10 tweets from target account
3. **AI Analysis**: Google Gemini analyzes and summarizes content
4. **Email Delivery**: Sends formatted HTML report to your email

## File Structure

```
/
├── package.json          # Dependencies
├── vercel.json           # Vercel configuration & cron
├── .env.local           # Local environment variables
├── pages/api/           # Serverless functions
│   └── tweet-summary.js # Main processing function
└── lib/                 # Utility modules
    ├── twitter.js       # Twitter API service
    ├── llm.js          # Google AI service
    └── email.js        # Email service
```

## Cost Considerations

- Vercel: Free tier includes cron jobs
- Twitter API: Free tier (Basic plan)
- Google AI: Pay-per-use (very affordable)
- Gmail: Free

Estimated monthly cost: $0-5 depending on usage.
*/