# Bigfoot Cryptoween Deluxe 🦶🎃

A full Telegram AI personality/game bot starring **Bigfoot, Mayor of Cryptoween**.

Bigfoot is loudly, comedically **bullish on Cryptoween** — the culture, pumpkins, spooky memes,
forest lore, and general chaos — while avoiding promises of real investment returns.

## New deluxe features

- AI Bigfoot personality with persistent chat flavor
- XP + levels
- Pumpkins as an in-bot game currency
- Collectible loot
- Cryptid battles
- Haunted pumpkin roll mini-game
- Global leaderboard
- Secret commands and easter eggs
- Daily Cryptoween prophecies
- Optional daily Telegram subscription
- Brainbusters, roasts, lore, campfire stories, fake headlines, sightings
- SQLite persistence
- Safe financial guardrails in the persona prompt

## Quick setup

1. Open **@BotFather** in Telegram.
2. Send `/newbot`, name it **Bigfoot**, and pick a unique username.
3. Copy the Telegram bot token.
4. Create an OpenAI API key.
5. Install Python 3.10+.
6. Open a terminal in this folder and run:

```bash
python -m venv .venv

# macOS / Linux
source .venv/bin/activate

# Windows
# .venv\Scripts\activate

pip install -r requirements.txt
```

7. Copy `.env.example` to `.env`.
8. Paste your Telegram token and OpenAI key into `.env`.
9. Run:

```bash
python bot.py
```

## BotFather command menu

In BotFather, use `/setcommands` and paste the contents of `botfather_commands.txt`.

## Daily prophecy time

`DAILY_PROPHECY_HOUR_UTC=15` means the scheduled prophecy goes out around 15:00 UTC.
Change that number in `.env` to any UTC hour from 0-23.

## Secret commands

Two secret commands are already hidden in the code. They are intentionally not listed in `/help`.
Add more by copying their pattern in `bot.py`.

## Data

Player XP, pumpkins, battle stats, subscriptions, and collectibles are stored in `bigfoot.db`.

## Production ideas

For a public bot, host it on a persistent service and back up the SQLite database.
For larger communities, swap SQLite for PostgreSQL and add admin/moderation commands.

## Security

Never commit `.env`, your Telegram bot token, or your OpenAI API key.

## One-click/cloud deployment

See `DEPLOY.md`. The repository includes a root Dockerfile and Render Blueprint.
