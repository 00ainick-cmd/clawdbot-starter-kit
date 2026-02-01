# Task: Set Up Discord for Clawdbot

A step-by-step guided setup for your Discord workspace.

---

## What We're Building

**TWO SERVERS:**
1. **[Your Productivity Server]** - Where work happens
   - #inbox - Quick capture, brain dumps
   - #workbench - Deep work sessions

2. **[Your Fun Server]** (optional) - Chaos zone, no rules

---

## Phase 1: Create Your Server

### Step 1: Create New Server
1. Open Discord desktop or web app
2. Click the + icon in the server list (left sidebar)
3. Select "Create My Own"
4. Select "For me and my friends" (keeps it private)
5. Name it: [Your Server Name]
6. Click Create

**Confirm before continuing.**

### Step 2: Delete Default Channels
1. Right-click #general → Delete Channel → Confirm
2. Right-click the voice channel → Delete Channel → Confirm

You should now have an empty server.

**Confirm before continuing.**

### Step 3: Create Your Channels
1. Click the + next to "Text Channels"
2. Name: `inbox`
3. Click Create
4. Repeat for: `workbench`

**Confirm before continuing.**

### Step 4: Add Channel Descriptions
1. Right-click #inbox → Edit Channel
2. Topic: "Brain dump here. Quick capture. Ace will process."
3. Save Changes
4. Repeat for #workbench: "Main work sessions. Deep work happens here."

**Confirm before continuing.**

### Step 5 (Nitro Users): Apply Server Boosts
1. Click server name at top
2. Select "Server Boost"
3. Click "Boost This Server"
4. Apply both boosts for Level 1 benefits

---

## Phase 2: Collect IDs

Enable Developer Mode:
1. Discord Settings → App Settings → Advanced
2. Turn on "Developer Mode"

Then collect these IDs (right-click → Copy ID):

| Item | How to Get | Your ID |
|------|-----------|---------|
| Server ID | Right-click server name | __________ |
| #inbox Channel ID | Right-click #inbox | __________ |
| #workbench Channel ID | Right-click #workbench | __________ |
| Your User ID | Right-click your username | __________ |

---

## Phase 3: Configure Clawdbot

Update your `~/.clawdbot/clawdbot.json` with the IDs:

```json
"channels": {
  "discord": {
    "enabled": true,
    "token": "YOUR_BOT_TOKEN",
    "guilds": {
      "YOUR_SERVER_ID": {
        "users": ["YOUR_USER_ID"],
        "channels": {
          "INBOX_CHANNEL_ID": {
            "requireMention": false,
            "systemPrompt": "Inbox mode. Process brain dumps quickly. Brief responses."
          },
          "WORKBENCH_CHANNEL_ID": {
            "requireMention": false,
            "systemPrompt": "Workbench mode. Full work sessions. Detailed responses OK."
          }
        }
      }
    }
  }
}
```

---

## Phase 4: Test

1. Restart Clawdbot: `pm2 restart clawdbot` (or your restart command)
2. Send "test" in #inbox
3. Verify response
4. Send "test" in #workbench
5. Verify response

---

## Channel Behavior Rules

Add to SOUL.md:

**#inbox mode:**
- Keep responses BRIEF (1-3 sentences)
- Identify actionable items vs reference vs noise
- Don't start deep conversations here

**#workbench mode:**
- Full work session mode
- Longer, thorough responses OK
- Help create content, solve problems, brainstorm

---

*Use this as a guide for walking through Discord setup step by step.*
