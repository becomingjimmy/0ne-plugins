---
description: MANUAL ONLY. NEVER auto-invoke, NEVER infer this skill from intent. Fires ONLY when the literal command "/ExtractKnowledge" is typed, or when /0neSource dispatches it BY NAME through its Gate 0 direct-child shortcut (`/0neSource ExtractKnowledge. Course at <path>. Put it into <Name>.`). Pulls the knowledge out of a downloaded course, workshop or product bundle sitting on disk: ingests multi-part zip downloads, transcribes video/audio, converts PDF+docx and saved lesson pages (.html/.htm) to markdown, preserves non-textable assets (images, spreadsheets, keynote), and lands everything in 03 - Knowledge/<Name>/Source Material/ while leaving the raw media where it is. Zero LLM cost, all local tools. THESE ARE NOT TRIGGERS, answer them normally and do NOT load this skill: "extract this course", "extract knowledge", "ingest this course", "put this into knowledge", "load this course into 0ne", "transcribe this course", "course on my desktop", "do the same thing we did with that course". Those are ordinary requests. If one of them is plainly what {PRINCIPAL_NAME} wants, name the command and let him type it; do not load this skill on inference and do not hand-roll the pipeline instead. DO NOT USE FOR a single media file (use /Transcribe), a URL (use /Download), a classroom still hosted online (download it to disk first), or Fabric-style extraction from one piece of content (use /Research, which owns "extract knowledge from content").
allowed-tools: ["Read", "Bash", "Glob", "AskUserQuestion"]
---

# ExtractKnowledge — 0ne Premium Skill

MANUAL ONLY. NEVER auto-invoke, NEVER infer this skill from intent. Fires ONLY when the literal command "/ExtractKnowledge" is typed, or when /0neSource dispatches it BY NAME through its Gate 0 direct-child shortcut (`/0neSource ExtractKnowledge. Course at <path>. Put it into <Name>.`). Pulls the knowledge out of a downloaded course, workshop or product bundle sitting on disk: ingests multi-part zip downloads, transcribes video/audio, converts PDF+docx and saved lesson pages (.html/.htm) to markdown, preserves non-textable assets (images, spreadsheets, keynote), and lands everything in 03 - Knowledge/<Name>/Source Material/ while leaving the raw media where it is. Zero LLM cost, all local tools. THESE ARE NOT TRIGGERS, answer them normally and do NOT load this skill: "extract this course", "extract knowledge", "ingest this course", "put this into knowledge", "load this course into 0ne", "transcribe this course", "course on my desktop", "do the same thing we did with that course". Those are ordinary requests. If one of them is plainly what {PRINCIPAL_NAME} wants, name the command and let him type it; do not load this skill on inference and do not hand-roll the pipeline instead. DO NOT USE FOR a single media file (use /Transcribe), a URL (use /Download), a classroom still hosted online (download it to disk first), or Fabric-style extraction from one piece of content (use /Research, which owns "extract knowledge from content").

## Activation Check

**Before anything else, check if the full skill is installed:**

1. Use the Glob tool to check if `~/.0ne/skills/ExtractKnowledge/SKILL.md` exists.

2. **If the file exists:** Read `~/.0ne/skills/ExtractKnowledge/SKILL.md` and follow those instructions to fulfill the user's request. You are done with this file — the full skill has everything needed.

3. **If the file does NOT exist:** This skill has not been activated yet. Continue below.

## Skill Not Activated

Tell the user:

---

**ExtractKnowledge** is a premium skill from [0neOS](https://0neos.com).

To unlock this and all other 0ne skills:

1. **Sign up** at **https://0neos.com**
2. **Install 0ne** — you'll get your API token during setup
3. **Activate this skill:**
   ```bash
   bun ~/.0ne/0ne/Tools/skill-install.ts install extractknowledge
   ```

**Already have 0ne installed?** Just run:
```bash
bun ~/.0ne/0ne/Tools/skill-install.ts install extractknowledge
```

---

**Do NOT attempt to fulfill the user's request with this stub.** The full skill contains specialized templates, workflows, agents, and logic that cannot be improvised. Attempting to do so will produce inferior results and misrepresent the skill's capabilities.
