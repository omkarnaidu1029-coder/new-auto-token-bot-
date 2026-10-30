# Auto Bot Token Sender

Telegram bot for token sending and SMS forwarding with Firebase integration.

## Features
- 🤖 Telegram bot automation
- 📱 SMS forwarding capabilities
- 🔥 Firebase Realtime Database integration
- 👥 Group monitoring
- 🔐 Admin controls
- 📊 User management and statistics

## Deployment Options

This bot can be deployed to multiple platforms:
- ✅ Render.com (Recommended - Free tier available)
- ✅ Fly.io
- ✅ Heroku

## Setup

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd Auto-bot-token-sender-main
```

### 2. Configure Settings
Copy the example settings file:
```bash
cp settings.example.json settings.json
```

Edit `settings.json` with your configuration:
- `telegramAutoBotToken`: Your Telegram bot token from [@BotFather](https://t.me/BotFather)
- `admin_ids`: Array of Telegram user IDs who can access admin commands
- `channel_username`: (Optional) Force join channel username
- `smsForwarderNumber`: (Optional) SMS forwarder phone number

### 3. Environment Variables

For production deployment, set these as environment variables instead of using `settings.json`:

- `BOT_TOKEN` or `TELEGRAM_AUTO_BOT_TOKEN`: Your bot token
- `ADMIN_IDS`: Comma-separated admin user IDs (e.g., `123456,789012`)
- `CHANNEL_USERNAME`: (Optional) Channel username
- `SMS_FORWARDER_NUMBER`: (Optional) SMS forwarder number

## Deploy to Render

1. Fork/Push this repo to GitHub
2. Go to [render.com](https://render.com) and sign up
3. Click **New +** → **Blueprint**
4. Connect your GitHub repository
5. Add environment variables in Render dashboard
6. Deploy!

## Deploy to Fly.io

1. Install Fly CLI:
```bash
curl -L https://fly.io/install.sh | sh
```

2. Login:
```bash
flyctl auth login
```

3. Deploy:
```bash
flyctl launch
```

4. Set secrets:
```bash
flyctl secrets set BOT_TOKEN="your_bot_token"
flyctl secrets set ADMIN_IDS="123456,789012"
```

## Deploy to Heroku

1. Install Heroku CLI
2. Login: `heroku login`
3. Create app: `heroku create your-app-name`
4. Set environment variables:
```bash
heroku config:set BOT_TOKEN="your_bot_token"
heroku config:set ADMIN_IDS="123456,789012"
```
5. Deploy: `git push heroku main`

## Local Development

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the bot:
```bash
python 2.py
```

## Requirements

- Python 3.11+
- python-telegram-bot >= 20.7
- Firebase Admin SDK (optional, for private databases)

## Database

The bot uses SQLite for storing user configurations and data. The database file (`bot_data.db`) is automatically created on first run.

## License

MIT License - Feel free to use and modify!
