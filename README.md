# Habitica Skill for Clawdbot

A comprehensive command-line interface (CLI) and Agent Skill for managing [Habitica](https://habitica.com) directly from your terminal or AI Agent.

This tool allows you to perform almost all Habitica actions—managing tasks, checking stats, casting skills, and interacting with your party—without leaving your command line.

## 🚀 Features

- **Task Management**: List, create, score, update, and delete Habits, Dailies, and To-Dos.
- **User Stats**: View HP, MP, XP, Gold, and Class attributes (STR/CON/INT/PER).
- **Collections**: View your Pets, Mounts, and Inventory (Eggs, Potions, Food).
- **Social**: Chat with your party, view guild memberships.
- **Class Skills**: Cast class-specific skills (e.g., Rogue's *Pickpocket*, Mage's *Fireball*) on tasks or self.
- **Quests**: Check quest progress and **auto-accept quest invitations**.
- **Automation**: Includes cron-ready scripts for daily maintenance or auto-joining quests.

## 📦 Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/TONYUNTURN/habitica-skill.git
   ```

2. Configure your credentials. Create a `~/.habitica` file (or set environment variables):
   ```bash
   # ~/.habitica
   export HABITICA_USER_ID="your-user-id-here"
   export HABITICA_API_TOKEN="your-api-token-here"
   ```
   > You can find these in Habitica -> Settings -> API.

3. Make the script executable:
   ```bash
   chmod +x scripts/habitica.sh
   ```

## 🛠️ Usage

Run the script directly:

```bash
./scripts/habitica.sh <command> [arguments...]
```

### Common Commands

**Tasks**
```bash
./scripts/habitica.sh list todos       # List all active To-Dos
./scripts/habitica.sh score <uuid> up  # Complete a task
./scripts/habitica.sh create todo "Buy milk" "Notes: 2% fat"
```

**Character**
```bash
./scripts/habitica.sh user             # Show quick summary
./scripts/habitica.sh stats            # Show detailed stats
./scripts/habitica.sh cast pickPocket  # Cast a skill
```

**Party & Quests**
```bash
./scripts/habitica.sh party-chat       # Read recent party chat
./scripts/habitica.sh quest            # Check current quest progress
./scripts/habitica.sh quest-accept     # Accept pending quest invite (useful for cron)
```

## 🤖 AI Agent Integration (Clawdbot)

If you are using [Clawdbot](https://github.com/clawdbot/clawdbot), this folder structure is ready to be used as a Skill.

1. Place this folder in your skills directory (e.g., `/root/clawd/skills/habitica`).
2. The agent will read `SKILL.md` to understand how to use the tool.
3. You can ask your agent:
   - "Check my Habitica dailies"
   - "Cast Valorous Presence"
   - "Buy a healing potion" (if extended)
   - "Auto-join quests for me"

## 📄 License

MIT License. Feel free to fork and modify!
