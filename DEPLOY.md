# 🚀 Deploy Bigfoot Cryptoween

This package is deployment-ready. You do **not** upload the ZIP to BotFather.
BotFather supplies the Telegram token; a cloud host runs `bot.py` 24/7.

## Easiest route: Render Blueprint

1. Create a new GitHub repository.
2. Upload **all files inside this folder** to the repository root.
3. In Render, choose **New → Blueprint** and connect that GitHub repository.
4. Render will automatically read `render.yaml`.
5. When prompted, enter:
   - `TELEGRAM_BOT_TOKEN`
   - `OPENAI_API_KEY`
6. Deploy the Blueprint.
7. When the worker says it is live, open your Telegram bot and send `/start`.

The included Blueprint uses a persistent `/data` disk so XP, pumpkins,
subscriptions, loot and leaderboard records survive redeploys.

## Railway alternative

1. Create a new Railway project from your GitHub repository.
2. Railway detects the included `Dockerfile`.
3. Add these Variables:
   - `TELEGRAM_BOT_TOKEN`
   - `OPENAI_API_KEY`
   - `OPENAI_MODEL=gpt-5.6-luna`
   - `DAILY_PROPHECY_HOUR_UTC=15`
4. Deploy.
5. For persistent game data, attach a Volume at `/data` and add:
   - `DB_PATH=/data/bigfoot.db`

## Before deploying

Create your Telegram bot with **@BotFather** and copy its token.
Never put either secret directly into GitHub or commit a `.env` file.

## BotFather menu

Use `/setcommands` in BotFather and paste `botfather_commands.txt`.

## What is included

AI Bigfoot personality; very bullish-on-Cryptoween comedy; XP and levels;
pumpkins; loot; cryptid battles; pumpkin-roll mini-game; leaderboard;
daily prophecies; subscriptions; riddles; roasts; lore; sightings;
fake headlines; secret commands; SQLite persistence.

Bigfoot's bullish behavior is written as comedy/personality, not a promise
of financial returns or personalized investment advice.
