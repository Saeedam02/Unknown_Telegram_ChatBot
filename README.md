# Unknown_Telegram_ChatBot
A Python-based Telegram bot that enables anonymous messaging between users. Built on **Cloudflare Workers** with **D1 database**, this bot allows users to generate unique anonymous messaging links and securely exchange messages while keeping their identity hidden.

## Features

- **Anonymous Messaging**: Users can send messages without revealing their identity.
- **Secure Database Integration**: Uses Cloudflare **D1** for user data storage.
- **Inline Reply Feature**: Recipients can respond directly to anonymous messages.
- **User Authentication**: Controls who can access the bot.
- **Webhook Setup**: Easy deployment via webhook integration.

## Getting Started

### Prerequisites

- A **Cloudflare Workers** account.
- A **D1 database** instance.
- A **Telegram Bot Token** from [BotFather](https://t.me/BotFather).

### Installation & Setup

1. **Create a Cloudflare Worker** and bind it to a D1 database.

2. **Create the necessary database table** in D1:
   ```sql
   CREATE TABLE users (
       "id" INTEGER PRIMARY KEY,
       "telegram_user_id" TEXT,
       "rkey" TEXT,
       "target_user" TEXT
   );
3. **Deploy the bot**:
  ```
Open the Worker in your browser and visit:
https://yourworker.username.workers.dev/init
```

## Configuration
Edit the script to configure your bot:

- BOT_TOKEN: Set your Telegram Bot Token.
- BOT_ID: Your bot's username (e.g., YourBotUsername).
- ALLOWED: Set to "ALL" for public access or specify allowed usernames.

## Usage
- Start the bot: /start
- Generate an anonymous messaging link: Click "✅ ساخت لینک ناشناس برای من"
- Send anonymous messages by sharing the generated link.
- Respond anonymously using the inline reply feature.

## Technologies Used
- Python (for bot logic)
- Cloudflare Workers (serverless execution)
- D1 Database (lightweight database storage)
- Telegram Bot API (for interaction)

## Contributing
Feel free to submit issues, feature requests, or pull requests.
