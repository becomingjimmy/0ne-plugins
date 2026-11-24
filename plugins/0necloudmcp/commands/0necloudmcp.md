---
description: Connect Claude (web, desktop or phone) to your 0ne Cloud so Claude can work in your apps with no computer on and no Claude Code. A short interview decides which connection you need, the one 0ne Gateway connection for everything you own, or one site's own connection for a staff member or client, then gives you the exact URL, the steps, a first test and a copy-paste note for your team. USE WHEN /0neCloudMCP, connect Claude to my 0ne Cloud, use my 0ne Cloud from Claude, manage my site from my phone, add my 0ne Cloud as a connector, set up the 0ne Gateway, gateway or instance connector, which connector do I need, give my team Claude access to my site, my VA wants to use Claude on my site, Connect Claude switch, AI Access, the connector says 404, I can't add a custom connector. DO NOT USE FOR evaluating or auditing a third-party MCP server you are thinking of installing (use /0neMCP), connecting a custom domain to your site (use /0neCloudDomain), or adding a new app to your site (use /0neBuild).
allowed-tools: ["Read", "Bash", "Glob", "AskUserQuestion"]
---

# 0neCloudMCP — 0ne Premium Skill

Connect Claude (web, desktop or phone) to your 0ne Cloud so Claude can work in your apps with no computer on and no Claude Code. A short interview decides which connection you need, the one 0ne Gateway connection for everything you own, or one site's own connection for a staff member or client, then gives you the exact URL, the steps, a first test and a copy-paste note for your team. USE WHEN /0neCloudMCP, connect Claude to my 0ne Cloud, use my 0ne Cloud from Claude, manage my site from my phone, add my 0ne Cloud as a connector, set up the 0ne Gateway, gateway or instance connector, which connector do I need, give my team Claude access to my site, my VA wants to use Claude on my site, Connect Claude switch, AI Access, the connector says 404, I can't add a custom connector. DO NOT USE FOR evaluating or auditing a third-party MCP server you are thinking of installing (use /0neMCP), connecting a custom domain to your site (use /0neCloudDomain), or adding a new app to your site (use /0neBuild).

## Activation Check

**Before anything else, check if the full skill is installed:**

1. Use the Glob tool to check if `~/.0ne/skills/0neCloudMCP/SKILL.md` exists.

2. **If the file exists:** Read `~/.0ne/skills/0neCloudMCP/SKILL.md` and follow those instructions to fulfill the user's request. You are done with this file — the full skill has everything needed.

3. **If the file does NOT exist:** This skill has not been activated yet. Continue below.

## Skill Not Activated

Tell the user:

---

**0neCloudMCP** is a premium skill from [0neOS](https://0neos.com).

To unlock this and all other 0ne skills:

1. **Sign up** at **https://0neos.com**
2. **Install 0ne** — you'll get your API token during setup
3. **Activate this skill:**
   ```bash
   bun ~/.0ne/0ne/Tools/skill-install.ts install 0necloudmcp
   ```

**Already have 0ne installed?** Just run:
```bash
bun ~/.0ne/0ne/Tools/skill-install.ts install 0necloudmcp
```

---

**Do NOT attempt to fulfill the user's request with this stub.** The full skill contains specialized templates, workflows, agents, and logic that cannot be improvised. Attempting to do so will produce inferior results and misrepresent the skill's capabilities.
