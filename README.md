# Clawdbot Starter Kit

Ready-to-use templates for setting up your Clawdbot AI assistant.

## What's Included

```
clawdbot-starter-kit/
├── templates/
│   ├── SOUL.md        # AI personality & behavior
│   ├── USER.md        # Your profile & context
│   ├── MEMORY.md      # Long-term memory structure
│   ├── AGENTS.md      # Operating instructions
│   ├── TOOLS.md       # Tool-specific notes
│   └── HEARTBEAT.md   # Proactive check-in rules
├── config/
│   └── clawdbot.example.json   # Sample config
└── README.md
```

## Quick Start

### 1. Copy Templates to Your Workspace

```bash
cp -r templates/* ~/clawd/
```

### 2. Customize Each File

**SOUL.md** — Define your AI's personality
- Replace `[ASSISTANT_NAME]` with your AI's name
- Adjust behavior rules to match your preferences

**USER.md** — Tell the AI about yourself
- Fill in your professional context
- List current projects
- Note communication preferences

**MEMORY.md** — Seed initial context
- Add current priorities
- Note any recent decisions
- List key people

### 3. Configure Clawdbot

Copy the example config:
```bash
cp config/clawdbot.example.json ~/.clawdbot/clawdbot.json
```

Then edit with your actual values:
- Anthropic API key
- Discord bot token
- Guild and channel IDs
- Your Discord user ID

### 4. Start Clawdbot

```bash
clawdbot gateway run
```

## Getting IDs

**Discord Guild ID:** 
Settings > Enable Developer Mode > Right-click server > Copy Server ID

**Discord Channel ID:**
Right-click channel > Copy Channel ID

**Discord User ID:**
Right-click your username > Copy User ID

## Tips

1. **Start simple** — Get basic chat working before adding integrations
2. **Customize gradually** — Adjust SOUL.md based on what works
3. **Update MEMORY.md regularly** — This is your AI's continuity
4. **Use HEARTBEAT.md wisely** — Proactive pings should add value, not annoy

## Learn More

- [Clawdbot Docs](https://docs.clawd.bot)
- [OpenClaw GitHub](https://github.com/clawdbot/clawdbot)
- [Discord Community](https://discord.com/invite/clawd)

---

*Built by Nick Brown | Based on production Clawdbot setups*
