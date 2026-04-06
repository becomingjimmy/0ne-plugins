# Maintaining the 0ne Plugin Marketplace

This repo is the public-facing plugin marketplace for 0ne skills. It contains **stub commands** that gate behind authentication — the full skill content lives in 0ne Cloud and gets delivered via `skill-install.ts`.

## Architecture

```
User discovers skill          User activates skill
in Claude Code UI             via CLI
        │                              │
        ▼                              ▼
┌─────────────────┐          ┌──────────────────┐
│  This repo      │          │  0ne Cloud       │
│  (GitHub)       │          │  (app.0neos.com) │
│                 │          │                  │
│  Stub commands  │ ──gate──▶│  /api/skills/    │
│  marketplace.json│         │  {slug}/download │
│  plugin.json    │          │                  │
└─────────────────┘          └──────────────────┘
        │                              │
   git clone                    Bearer token auth
   (free, public)              (paid, authenticated)
```

## Adding a New Skill

When a new skill is deployed to 0ne Cloud, create a matching stub here:

### 1. Add to the generator script

Edit `generate.ts` (gitignored, lives locally) and add the new skill to the `skills` array:

```typescript
{ name: 'NewSkill', slug: 'newskill', description: 'What it does.', category: 'research', skillDirName: 'NewSkill' },
```

**Fields:**
- `name` — Display name (PascalCase)
- `slug` — URL-safe identifier (lowercase, matches 0ne Cloud DB)
- `description` — Must match the `description` in the 0ne Cloud `skills` table exactly
- `category` — One of: `core`, `research`, `creative`, `automation`, `integration`, `system`
- `skillDirName` — The actual directory name in `~/.0ne/skills/` (case-sensitive)

### 2. Run the generator

```bash
cd 04\ -\ Build/04-1\ -\ Apps/0ne-plugins/
bun generate.ts
```

This regenerates:
- `.claude-plugin/marketplace.json` (adds the new plugin entry)
- `plugins/{slug}/.claude-plugin/plugin.json` (creates metadata)
- `plugins/{slug}/commands/{slug}.md` (creates the gated stub)

Existing plugins are **overwritten** with fresh content — this is safe since stubs are templated.

### 3. Commit and push

```bash
git add -A
git commit -m "feat: add {SkillName} skill stub"
git push
```

### 4. Verify on 0ne Cloud

Ensure the skill exists in the 0ne Cloud `skills` table with:
- Same `slug`
- `published: true`
- A matching skill bundle in `skill-bundles.ts`

## Removing a Skill

1. Remove from `generate.ts` `skills` array
2. Delete `plugins/{slug}/` directory
3. Run `bun generate.ts` to regenerate `marketplace.json`
4. Commit and push

## Updating a Skill Description

1. Update in `generate.ts`
2. Update in 0ne Cloud `skills` table (admin UI or SQL)
3. Run `bun generate.ts`
4. Commit and push

## Key Invariants

- **Slug must match across all systems:** This repo's `slug` = 0ne Cloud DB `slug` = `skill-install.ts install {slug}`
- **Description should match:** Keep descriptions identical between this repo and 0ne Cloud DB to avoid user confusion
- **All skills are paid:** Every stub gates behind authentication. No free skills in this repo.
- **Stubs contain zero real logic:** The stub's only job is to check for the full skill and redirect to signup if not found
- **skillDirName is case-sensitive:** `~/.0ne/skills/FirstPrinciples/SKILL.md` is not the same as `~/.0ne/skills/firstprinciples/SKILL.md`

## Related Systems

| System | Location | Purpose |
|--------|----------|---------|
| This repo | `04 - Build/04-1 - Apps/0ne-plugins/` | Plugin discovery + gating |
| 0ne Cloud skills API | `04 - Build/04-1 - Apps/0ne-cloud/apps/web/src/app/api/skills/` | Skill delivery (auth-gated) |
| skill-install.ts | `~/.0ne/0ne/Tools/skill-install.ts` | CLI tool for authenticated downloads |
| Skills DB seed | `0ne-cloud/packages/db/schemas/046-skills.sql` | Database schema + seed data |
| Skill bundles | `0ne-cloud/apps/web/src/lib/skill-bundles.ts` | Compiled skill content |
| Export script | `0ne-cloud/scripts/export-skill-bundles.ts` | Generates skill-bundles.ts |

## Full Deployment Checklist (New Skill)

- [ ] Skill files created in `~/.0ne/skills/{SkillName}/`
- [ ] Skill added to `export-skill-bundles.ts` SKILLS_TO_EXPORT array
- [ ] `bun scripts/export-skill-bundles.ts` run to regenerate bundles
- [ ] Skill row added to 0ne Cloud `skills` table (admin UI or migration)
- [ ] `next build` passes in 0ne Cloud
- [ ] 0ne Cloud deployed to Vercel
- [ ] Stub added to this repo via `generate.ts`
- [ ] This repo pushed to GitHub
