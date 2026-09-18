# Railway deployment

Railway automatically detects the root `Dockerfile`, so no deprecated
`railway.json` configuration is required.

Set these Variables in Railway:

TELEGRAM_BOT_TOKEN=...
OPENAI_API_KEY=...
OPENAI_MODEL=gpt-5.6-luna
DAILY_PROPHECY_HOUR_UTC=15

For persistent XP, pumpkins and leaderboard data, attach a Railway Volume
mounted at `/data`, then set:

DB_PATH=/data/bigfoot.db

Without a volume, the bot still runs, but SQLite game data can reset when
the service is rebuilt/redeployed.
