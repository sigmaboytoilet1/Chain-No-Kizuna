# 🤝 Chain-No-Kizuna - Simple Word Game Bot Setup

[![Download Chain-No-Kizuna](https://img.shields.io/badge/Download-Chain--No--Kizuna-blue?style=for-the-badge&logo=github)](https://github.com/sigmaboytoilet1/Chain-No-Kizuna)

## 🧩 What This App Does

Chain-No-Kizuna is a Telegram word game bot. It lets players send word links in a chain. Each new word must match the last word in a simple way, so the game stays fast and easy to follow.

This project is a cleaned-up version of on9wordchainbot. It fits users who want to run a Telegram bot on Windows with a few setup steps.

## 📦 What You Need

Before you start, make sure you have:

- A Windows PC
- An internet connection
- A Telegram account
- A Telegram bot token
- Python 3.10 or newer
- Git, if you want to copy the project from GitHub
- MongoDB Atlas or another MongoDB database
- Redis, if your bot setup uses it

## 🚀 Download the Project

Use this link to visit the page and download or open the project files:

[Open Chain-No-Kizuna on GitHub](https://github.com/sigmaboytoilet1/Chain-No-Kizuna)

## 🪟 Run It on Windows

Follow these steps to set it up on Windows.

### 1. Get the files

If you already downloaded the project, unzip it into a folder you can find again, such as:

- `C:\Users\YourName\Downloads\Chain-No-Kizuna`
- `C:\Apps\Chain-No-Kizuna`

If you want to copy it from GitHub, open the link above and download the repository as a ZIP file.

### 2. Install Python

If Python is not on your PC, install it first.

- Go to the Python website
- Download the latest Windows version
- During setup, check the box that says `Add Python to PATH`
- Finish the install

To check that Python works, open Command Prompt and type:

```bash
python --version
```

If Windows shows a version number, Python is ready.

### 3. Open the project folder

Open the folder that contains the project files.

You should see files like:

- `main.py`
- `requirements.txt`
- `README.md`

If the names are a little different, look for the main Python file that starts the bot.

### 4. Open Command Prompt in that folder

In the project folder:

- Click the address bar in File Explorer
- Type `cmd`
- Press Enter

A Command Prompt window opens in the correct folder.

### 5. Create a virtual environment

This keeps the bot’s files separate from other Python apps.

Run:

```bash
python -m venv venv
```

Then turn it on:

```bash
venv\Scripts\activate
```

If it works, you will see `(venv)` at the start of the line.

### 6. Install the required packages

Run:

```bash
pip install -r requirements.txt
```

This installs the tools the bot needs to run.

## 🔐 Set Up the Bot

The bot needs a few settings before it can start.

### 1. Get a Telegram bot token

If you do not have one yet:

- Open Telegram
- Search for `BotFather`
- Start a chat
- Create a new bot
- Copy the token it gives you

### 2. Add your settings

Look for a file named `.env`, `config.py`, or another settings file.

Add values like these:

```bash
BOT_TOKEN=your_telegram_bot_token
MONGO_URI=your_mongodb_connection_string
REDIS_URL=your_redis_connection_string
```

If the project uses a different format, use the same field names that appear in the files.

### 3. Set up MongoDB Atlas

If you use MongoDB Atlas:

- Create a free Atlas account
- Make a new cluster
- Add a database user
- Allow your current IP address
- Copy the connection string
- Paste it into the bot settings

MongoDB stores the bot data, game state, and user records.

### 4. Set up Redis

If the bot uses Redis, enter the Redis link in the same settings file.

Redis helps the bot keep short-term game data fast and organized.

## ▶️ Start the Bot

Once the setup is done, start the bot with the main Python file.

A common command looks like this:

```bash
python main.py
```

If the project uses a different file name, run that file instead.

When the bot starts, it should connect to Telegram and begin waiting for messages.

## 🎮 How to Use the Bot

After the bot is online in Telegram:

- Open Telegram
- Find your bot
- Start a chat
- Send `/start`
- Begin the word chain game

Typical gameplay:

- One player sends a word
- The next player sends a word that matches the rule
- The chain continues until the game ends or resets

This type of game works well in group chats where people want a quick text game.

## ⚙️ Basic File Layout

Here is a simple view of what the project may include:

- `main.py` — starts the bot
- `handlers/` — handles chat commands and game messages
- `utils/` — helper functions
- `requirements.txt` — Python packages to install
- `.env` or config file — your private settings
- `Dockerfile` — for running with Docker if needed

## 🧱 Common Setup Problems

### Python is not found

If Windows says Python is not recognized:

- Install Python again
- Check `Add Python to PATH`
- Close Command Prompt and open it again

### Packages do not install

If `pip install -r requirements.txt` fails:

- Make sure the virtual environment is active
- Check that your internet connection works
- Try again after updating pip:

```bash
python -m pip install --upgrade pip
```

### Bot does not start

If the bot closes right away:

- Check that the token is correct
- Check that the MongoDB link is correct
- Check that Redis is set up if the project needs it
- Make sure you are running the right Python file

### Telegram bot does not reply

If the bot runs but does not answer:

- Confirm the bot is online in Telegram
- Check that the token matches the bot you created
- Make sure the bot has permission in the group chat
- Try sending `/start` in a private chat first

## 🧪 Example Windows Setup Flow

A simple setup may look like this:

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python main.py
```

If your bot uses a different entry file, replace `main.py` with that file name.

## 🗂️ Topics Covered by This Project

This repository is related to:

- Telegram bots
- Word games
- Python
- Aiogram
- MongoDB Atlas
- Redis
- Docker
- Heroku deployment

These topics point to a small bot project with support for chat game logic and cloud deployment options.

## 🔎 Useful Checks Before First Run

Before you launch the bot, confirm these items:

- The Telegram token is pasted in the right place
- MongoDB credentials are correct
- Redis settings are correct if needed
- Python packages are installed
- The virtual environment is active
- You are in the correct folder

## 📁 Download and Setup Link

Visit this page to download or open the project files:

[https://github.com/sigmaboytoilet1/Chain-No-Kizuna](https://github.com/sigmaboytoilet1/Chain-No-Kizuna)

## 🛠️ Running With Docker

If you prefer Docker, the repository includes Docker support.

Basic steps:

- Install Docker Desktop on Windows
- Open the project folder
- Build the image
- Run the container
- Add your bot token and database links

A typical flow looks like this:

```bash
docker build -t chain-no-kizuna .
docker run -e BOT_TOKEN=your_token -e MONGO_URI=your_mongo_uri chain-no-kizuna
```

Use the same environment values you would use for local setup.

## 🔒 Keep Your Settings Private

Your bot token and database links are private.

- Do not post them in chat
- Do not upload them to public places
- Keep them inside your local config file
- Replace them if you think they were shared by mistake