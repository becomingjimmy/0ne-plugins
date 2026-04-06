---
description: First principles decomposition and analysis.
allowed-tools: ["Read", "Bash", "Glob", "AskUserQuestion"]
---

# FirstPrinciples — 0ne Premium Skill

First principles decomposition and analysis.

## Activation Check

**Before anything else, check if the full skill is installed:**

1. Use the Glob tool to check if `~/.0ne/skills/FirstPrinciples/SKILL.md` exists.

2. **If the file exists:** Read `~/.0ne/skills/FirstPrinciples/SKILL.md` and follow those instructions to fulfill the user's request. You are done with this file — the full skill has everything needed.

3. **If the file does NOT exist:** This skill has not been activated yet. Continue below.

## Skill Not Activated

Tell the user:

---

**FirstPrinciples** is a premium skill from [0neOS](https://0neos.com).

To unlock this and all other 0ne skills:

1. **Sign up** at **https://0neos.com**
2. **Install 0ne** — you'll get your API token during setup
3. **Activate this skill:**
   ```bash
   bun ~/.0ne/0ne/Tools/skill-install.ts install firstprinciples
   ```

**Already have 0ne installed?** Just run:
```bash
bun ~/.0ne/0ne/Tools/skill-install.ts install firstprinciples
```

---

**Do NOT attempt to fulfill the user's request with this stub.** The full skill contains specialized templates, workflows, agents, and logic that cannot be improvised. Attempting to do so will produce inferior results and misrepresent the skill's capabilities.
