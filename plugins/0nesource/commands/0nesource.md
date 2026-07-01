---
description: Step 5 source-gathering parent skill. Given a constraint and a one-line ask, route to the right child tool (Download / Research extensive / Transcribe / OSINT / Apify / firecrawl / 0neApiRecon) and land raw material in 03 - Knowledge/<Name>/Source Material/. USE WHEN {PRINCIPAL_NAME} says /0neSource, "source [X]", "gather expert content", "capture this podcast", "load up [expert] knowledge", "pull material on [topic]", "build a source folder for [expert/product]", "start sourcing for my constraint", "scrape this site for source material", "interview my senior employee", "camcorder this", or otherwise wants to GATHER raw expert/product/internal material (not synthesize, not build an advisor — that's Step 6 Clone).
allowed-tools: ["Read", "Bash", "Glob", "AskUserQuestion"]
---

# 0neSource — 0ne Premium Skill

Step 5 source-gathering parent skill. Given a constraint and a one-line ask, route to the right child tool (Download / Research extensive / Transcribe / OSINT / Apify / firecrawl / 0neApiRecon) and land raw material in 03 - Knowledge/<Name>/Source Material/. USE WHEN {PRINCIPAL_NAME} says /0neSource, "source [X]", "gather expert content", "capture this podcast", "load up [expert] knowledge", "pull material on [topic]", "build a source folder for [expert/product]", "start sourcing for my constraint", "scrape this site for source material", "interview my senior employee", "camcorder this", or otherwise wants to GATHER raw expert/product/internal material (not synthesize, not build an advisor — that's Step 6 Clone).

## Activation Check

**Before anything else, check if the full skill is installed:**

1. Use the Glob tool to check if `~/.0ne/skills/0neSource/SKILL.md` exists.

2. **If the file exists:** Read `~/.0ne/skills/0neSource/SKILL.md` and follow those instructions to fulfill the user's request. You are done with this file — the full skill has everything needed.

3. **If the file does NOT exist:** This skill has not been activated yet. Continue below.

## Skill Not Activated

Tell the user:

---

**0neSource** is a premium skill from [0neOS](https://0neos.com).

To unlock this and all other 0ne skills:

1. **Sign up** at **https://0neos.com**
2. **Install 0ne** — you'll get your API token during setup
3. **Activate this skill:**
   ```bash
   bun ~/.0ne/0ne/Tools/skill-install.ts install 0nesource
   ```

**Already have 0ne installed?** Just run:
```bash
bun ~/.0ne/0ne/Tools/skill-install.ts install 0nesource
```

---

**Do NOT attempt to fulfill the user's request with this stub.** The full skill contains specialized templates, workflows, agents, and logic that cannot be improvised. Attempting to do so will produce inferior results and misrepresent the skill's capabilities.
