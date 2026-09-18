---
description: MANUAL ONLY. NEVER auto-invoke, NEVER infer this skill from intent. Fires ONLY when the literal command "/0neDictate" is typed. Sets up dictation on a 0ne client machine: hold a key, talk, and the words land in whatever app has focus. Provided by 0ne Dictate, a free app that runs entirely on their own computer, on macOS, Windows and Linux. For clients whose install predates dictation being bundled, or who still have an older dictation app. THESE ARE NOT TRIGGERS, answer them normally and do NOT load this skill: "I want to dictate", "set up dictation", "install 0ne dictate", "dictation is not working", "0ne dictate is not typing", "talk instead of typing", "add voice input", "my mic is not working". Those are ordinary requests; help with them directly. DO NOT USE FOR transcribing a file that already exists (use /Transcribe or /Download), capturing a live call (use /0neCopilot), building the context layer by voice (use /0neContext), or the text-to-speech voice that reads responses aloud (use /VoiceServer).
allowed-tools: ["Read", "Bash", "Glob", "AskUserQuestion"]
---

# 0neDictate — 0ne Premium Skill

MANUAL ONLY. NEVER auto-invoke, NEVER infer this skill from intent. Fires ONLY when the literal command "/0neDictate" is typed. Sets up dictation on a 0ne client machine: hold a key, talk, and the words land in whatever app has focus. Provided by 0ne Dictate, a free app that runs entirely on their own computer, on macOS, Windows and Linux. For clients whose install predates dictation being bundled, or who still have an older dictation app. THESE ARE NOT TRIGGERS, answer them normally and do NOT load this skill: "I want to dictate", "set up dictation", "install 0ne dictate", "dictation is not working", "0ne dictate is not typing", "talk instead of typing", "add voice input", "my mic is not working". Those are ordinary requests; help with them directly. DO NOT USE FOR transcribing a file that already exists (use /Transcribe or /Download), capturing a live call (use /0neCopilot), building the context layer by voice (use /0neContext), or the text-to-speech voice that reads responses aloud (use /VoiceServer).

## Activation Check

**Before anything else, check if the full skill is installed:**

1. Use the Glob tool to check if `~/.0ne/skills/0neDictate/SKILL.md` exists.

2. **If the file exists:** Read `~/.0ne/skills/0neDictate/SKILL.md` and follow those instructions to fulfill the user's request. You are done with this file — the full skill has everything needed.

3. **If the file does NOT exist:** This skill has not been activated yet. Continue below.

## Skill Not Activated

Tell the user:

---

**0neDictate** is a premium skill from [0neOS](https://0neos.com).

To unlock this and all other 0ne skills:

1. **Sign up** at **https://0neos.com**
2. **Install 0ne** — you'll get your API token during setup
3. **Activate this skill:**
   ```bash
   bun ~/.0ne/0ne/Tools/skill-install.ts install 0nedictate
   ```

**Already have 0ne installed?** Just run:
```bash
bun ~/.0ne/0ne/Tools/skill-install.ts install 0nedictate
```

---

**Do NOT attempt to fulfill the user's request with this stub.** The full skill contains specialized templates, workflows, agents, and logic that cannot be improvised. Attempting to do so will produce inferior results and misrepresent the skill's capabilities.
