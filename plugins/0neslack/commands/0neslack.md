---
description: Slack app setup and configuration. USE WHEN slack, slack bot, set up slack, configure slack, slack token, slack app, slack workspace, 0neslack.
allowed-tools: ["Read", "Bash", "Glob", "AskUserQuestion"]
---

# 0neSlack — 0ne Premium Skill

Slack app setup and configuration. USE WHEN slack, slack bot, set up slack, configure slack, slack token, slack app, slack workspace, 0neslack.

## Activation Check

**Before anything else, check if the full skill is installed:**

1. Use the Glob tool to check if `~/.0ne/skills/0neSlack/SKILL.md` exists.

2. **If the file exists:** Read `~/.0ne/skills/0neSlack/SKILL.md` and follow those instructions to fulfill the user's request. You are done with this file — the full skill has everything needed.

3. **If the file does NOT exist:** This skill has not been activated yet. Continue below.

## Skill Not Activated

Tell the user:

---

**0neSlack** is a premium skill from [0neOS](https://0neos.com).

To unlock this and all other 0ne skills:

1. **Sign up** at **https://0neos.com**
2. **Install 0ne** — you'll get your API token during setup
3. **Activate this skill:**
   ```bash
   bun ~/.0ne/0ne/Tools/skill-install.ts install 0neslack
   ```

**Already have 0ne installed?** Just run:
```bash
bun ~/.0ne/0ne/Tools/skill-install.ts install 0neslack
```

---

**Do NOT attempt to fulfill the user's request with this stub.** The full skill contains specialized templates, workflows, agents, and logic that cannot be improvised. Attempting to do so will produce inferior results and misrepresent the skill's capabilities.
