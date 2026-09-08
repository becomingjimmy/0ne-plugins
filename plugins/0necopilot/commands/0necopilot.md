---
description: Live session copilot. Taps Zoom or a room mic, transcribes both sides, and runs a turn-by-turn orchestrator that feeds you the next question live. USE WHEN run copilot, start copilot, /0neCopilot, live copilot, listen to this call, listen along, real-time coaching, live transcription, live prompt during a call, session copilot, paid session, sales call, sales discovery, discovery call, hiring interview, podcast interview, coaching call, 1-on-1, team standup, in-person interview, offline mode, room mic, capture this conversation, new mode, mode design. DO NOT USE FOR building or synthesizing the context layer itself (use /0neContext, which OWNS "interview me", "context interview" and "build my context" and calls this skill for the voice leg). DO NOT USE FOR transcribing an existing recording or video file (use /Transcribe or /Download): this skill captures LIVE audio and is useless on a file that already exists.
allowed-tools: ["Read", "Bash", "Glob", "AskUserQuestion"]
---

# 0neCopilot — 0ne Premium Skill

Live session copilot. Taps Zoom or a room mic, transcribes both sides, and runs a turn-by-turn orchestrator that feeds you the next question live. USE WHEN run copilot, start copilot, /0neCopilot, live copilot, listen to this call, listen along, real-time coaching, live transcription, live prompt during a call, session copilot, paid session, sales call, sales discovery, discovery call, hiring interview, podcast interview, coaching call, 1-on-1, team standup, in-person interview, offline mode, room mic, capture this conversation, new mode, mode design. DO NOT USE FOR building or synthesizing the context layer itself (use /0neContext, which OWNS "interview me", "context interview" and "build my context" and calls this skill for the voice leg). DO NOT USE FOR transcribing an existing recording or video file (use /Transcribe or /Download): this skill captures LIVE audio and is useless on a file that already exists.

## Activation Check

**Before anything else, check if the full skill is installed:**

1. Use the Glob tool to check if `~/.0ne/skills/0neCopilot/SKILL.md` exists.

2. **If the file exists:** Read `~/.0ne/skills/0neCopilot/SKILL.md` and follow those instructions to fulfill the user's request. You are done with this file — the full skill has everything needed.

3. **If the file does NOT exist:** This skill has not been activated yet. Continue below.

## Skill Not Activated

Tell the user:

---

**0neCopilot** is a premium skill from [0neOS](https://0neos.com).

To unlock this and all other 0ne skills:

1. **Sign up** at **https://0neos.com**
2. **Install 0ne** — you'll get your API token during setup
3. **Activate this skill:**
   ```bash
   bun ~/.0ne/0ne/Tools/skill-install.ts install 0necopilot
   ```

**Already have 0ne installed?** Just run:
```bash
bun ~/.0ne/0ne/Tools/skill-install.ts install 0necopilot
```

---

**Do NOT attempt to fulfill the user's request with this stub.** The full skill contains specialized templates, workflows, agents, and logic that cannot be improvised. Attempting to do so will produce inferior results and misrepresent the skill's capabilities.
