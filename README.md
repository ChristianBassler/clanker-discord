# VEX Discord Bot (Node.js)

Fun, ready-to-run Discord bot with silly commands for a VEX robotics team.

## Features
- `/ping` — pong!
- `/robotname` — silly robot name generator
- `/dadjoke` — terrible dad jokes
- `/roast [user]` — gentle roasts
- `/compliment [user]` — wholesome praise
- `/duel @opponent` — random 1v1
- `/fate` — dice of fate
- `/cheese` — random cheese fact
- `/beep <text>` — beep/boop translator
- `/taco [user]` — award a taco
- `/tacos` — taco leaderboard (stored in `data/tacos.json`)

## Quick Start

1. **Create a Discord Application & Bot**
   - https://discord.com/developers/applications → New Application
   - **Bot** → Add Bot → copy the **Token** (keep it secret)
   - **OAuth2 → URL Generator**: Scopes = `bot`, `applications.commands`
     - Bot Permissions: at least **Send Messages** and **Read Messages**
   - Invite the bot to your server with the generated URL

2. **Clone / Download this folder**
   - Put your files somewhere like `~/Desktop/vex-discord-bot`

3. **Install Node.js dependencies**
   ```bash
   npm install
   ```

4. **Configure environment**
   - Copy `.env.example` to `.env` and fill in your values:
     ```env
     DISCORD_TOKEN=YOUR_BOT_TOKEN_HERE
     # Optional: Register commands to a single server for instant updates
     GUILD_ID=YOUR_SERVER_ID
     ```

5. **Run the bot**
   ```bash
   npm start
   ```

6. **Use the commands in your server**
   - If you set `GUILD_ID`, commands appear instantly
   - If not, global commands may take time to show up

## Notes
- Data for tacos is stored in `data/tacos.json`. This is a simple JSON file-based store; for multi-host or heavy use, replace with a database.
- If your token ever leaks, **reset it immediately** in the Developer Portal.
- To add more commands, follow the pattern inside `index.js` in the `InteractionCreate` handler.

## License
MIT
