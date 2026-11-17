---
description: Installs and runs 0neEmail, the cloud inbox sorter (sender rules, a Review queue, a 30-day undo log), as an optional module on a member's OWN 0ne Cloud site, then is its chat front door. Same API as the app, with an email agent token. USE WHEN install 0neEmail, add the email app to my site, update 0neEmail, remove 0neEmail, inbox status, how is my inbox, 0neEmail, clean my inbox in 0neEmail, deep clean my inbox, remove duplicate emails, email rules, add an email rule, label this sender's email, email labels, turn off an email rule, delete an email rule, archive this sender's marketing, review queue, clear email review, what's in my inbox, read my inbox, archive everything from this sender, undo email action, undo that archive, 0neEmail setup, connect Gmail to 0neEmail, email doctor, is 0neEmail syncing, gmail filter audit, audit my gmail filters, which filters hide my mail, a filter archived my bill, bring back hidden notices, set up a Google Cloud OAuth app, create Google OAuth client, Gmail API credentials, new GCP project for OAuth, enable Gmail API, enable a Google API, OAuth consent screen, publish OAuth app to production, add OAuth scopes, verify Google client secret, is my Google client secret valid, GOCSPX, Gmail push, Pub/Sub topic for Gmail, instant email sync. DO NOT USE FOR a one-off bulk triage of the inbox with the local gws CLI, "triage", "clean inbox", nuke cold emails (use /EmailTriage), undoing code changes (use /0neCloudUndo), 0ne system health (use /0neDoctor), sending or drafting mail (use /Google).
allowed-tools: ["Read", "Bash", "Glob", "AskUserQuestion"]
---

# 0neEmail — 0ne Premium Skill

Installs and runs 0neEmail, the cloud inbox sorter (sender rules, a Review queue, a 30-day undo log), as an optional module on a member's OWN 0ne Cloud site, then is its chat front door. Same API as the app, with an email agent token. USE WHEN install 0neEmail, add the email app to my site, update 0neEmail, remove 0neEmail, inbox status, how is my inbox, 0neEmail, clean my inbox in 0neEmail, deep clean my inbox, remove duplicate emails, email rules, add an email rule, label this sender's email, email labels, turn off an email rule, delete an email rule, archive this sender's marketing, review queue, clear email review, what's in my inbox, read my inbox, archive everything from this sender, undo email action, undo that archive, 0neEmail setup, connect Gmail to 0neEmail, email doctor, is 0neEmail syncing, gmail filter audit, audit my gmail filters, which filters hide my mail, a filter archived my bill, bring back hidden notices, set up a Google Cloud OAuth app, create Google OAuth client, Gmail API credentials, new GCP project for OAuth, enable Gmail API, enable a Google API, OAuth consent screen, publish OAuth app to production, add OAuth scopes, verify Google client secret, is my Google client secret valid, GOCSPX, Gmail push, Pub/Sub topic for Gmail, instant email sync. DO NOT USE FOR a one-off bulk triage of the inbox with the local gws CLI, "triage", "clean inbox", nuke cold emails (use /EmailTriage), undoing code changes (use /0neCloudUndo), 0ne system health (use /0neDoctor), sending or drafting mail (use /Google).

## Activation Check

**Before anything else, check if the full skill is installed:**

1. Use the Glob tool to check if `~/.0ne/skills/0neEmail/SKILL.md` exists.

2. **If the file exists:** Read `~/.0ne/skills/0neEmail/SKILL.md` and follow those instructions to fulfill the user's request. You are done with this file — the full skill has everything needed.

3. **If the file does NOT exist:** This skill has not been activated yet. Continue below.

## Skill Not Activated

Tell the user:

---

**0neEmail** is a premium skill from [0neOS](https://0neos.com).

To unlock this and all other 0ne skills:

1. **Sign up** at **https://0neos.com**
2. **Install 0ne** — you'll get your API token during setup
3. **Activate this skill:**
   ```bash
   bun ~/.0ne/0ne/Tools/skill-install.ts install 0neemail
   ```

**Already have 0ne installed?** Just run:
```bash
bun ~/.0ne/0ne/Tools/skill-install.ts install 0neemail
```

---

**Do NOT attempt to fulfill the user's request with this stub.** The full skill contains specialized templates, workflows, agents, and logic that cannot be improvised. Attempting to do so will produce inferior results and misrepresent the skill's capabilities.
