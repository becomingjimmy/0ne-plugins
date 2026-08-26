---
description: Track and grade the things you've built, automations, skills, apps, processes, and get told where to go back to when they aren't working. Keeps a registry at `05 - Context/Monitors.md`. USE WHEN start monitoring this, add this to what i track, capture a baseline, record the before, grade this automation, did my automation work, is this thing still running, how is that skill performing, what should i fix next, build me a watcher for this, alert me if this stops. DO NOT USE FOR checking whether your website or cloud app is up (use /0neCloudStatus), or checking 0ne system health (use /0neDoctor).
allowed-tools: ["Read", "Bash", "Glob", "AskUserQuestion"]
---

# 0neMonitor — 0ne Premium Skill

Track and grade the things you've built, automations, skills, apps, processes, and get told where to go back to when they aren't working. Keeps a registry at `05 - Context/Monitors.md`. USE WHEN start monitoring this, add this to what i track, capture a baseline, record the before, grade this automation, did my automation work, is this thing still running, how is that skill performing, what should i fix next, build me a watcher for this, alert me if this stops. DO NOT USE FOR checking whether your website or cloud app is up (use /0neCloudStatus), or checking 0ne system health (use /0neDoctor).

## Activation Check

**Before anything else, check if the full skill is installed:**

1. Use the Glob tool to check if `~/.0ne/skills/0neMonitor/SKILL.md` exists.

2. **If the file exists:** Read `~/.0ne/skills/0neMonitor/SKILL.md` and follow those instructions to fulfill the user's request. You are done with this file — the full skill has everything needed.

3. **If the file does NOT exist:** This skill has not been activated yet. Continue below.

## Skill Not Activated

Tell the user:

---

**0neMonitor** is a premium skill from [0neOS](https://0neos.com).

To unlock this and all other 0ne skills:

1. **Sign up** at **https://0neos.com**
2. **Install 0ne** — you'll get your API token during setup
3. **Activate this skill:**
   ```bash
   bun ~/.0ne/0ne/Tools/skill-install.ts install 0nemonitor
   ```

**Already have 0ne installed?** Just run:
```bash
bun ~/.0ne/0ne/Tools/skill-install.ts install 0nemonitor
```

---

**Do NOT attempt to fulfill the user's request with this stub.** The full skill contains specialized templates, workflows, agents, and logic that cannot be improvised. Attempting to do so will produce inferior results and misrepresent the skill's capabilities.
