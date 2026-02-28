# Claude Skills Monorepo — Agent Instructions

## Overview

This is a private monorepo of custom Claude skills. Each subdirectory is a complete, self-contained skill that is also published as its own public GitHub repo.

## Skill Format

Claude skills follow the official format:

- **`Skill.md`** (required): YAML frontmatter + markdown instructions
  - `name`: Human-friendly name (max 64 chars)
  - `description`: When/why Claude invokes this skill (max 200 chars)
  - `dependencies`: Optional (e.g. `python>=3.8`)
  - Body: Instructions, reference material, behavioral rules
- **Resource files**: e.g. `REFERENCE.md`, supporting docs
- **Scripts**: Python or JS/Node.js executables (optional)
- **Assets**: Logo, fonts, etc. (optional)

To use a skill: zip the skill folder and upload at Claude **Customize > Skills**.

## Repository Structure

```
skills/
  AGENTS.md            # This file
  README.md            # Monorepo overview and skills index
  {skill-name}/        # One folder per skill (also a public GitHub repo)
    Skill.md
    ...
```

## Git Remotes

- `madcap`: Private Forgejo on NAS — this monorepo lives here
- Each individual skill also has its own public GitHub repo: `github.com/danmurrelljr/{skill-name}`

## Sync Workflow

Individual skills are kept in sync manually:
1. Edit the skill here in the monorepo
2. When ready, copy changed files to the individual skill's local repo clone
3. Commit and push to the public GitHub repo
4. Zip the skill folder for upload to Claude if the skill content changed

If asked to "sync skills" or "publish {skill-name}", follow the steps above. Remind the user to re-upload the zip to Claude if `Skill.md` or any resource file changed.

## Creating a New Skill

1. Create `{skill-name}/Skill.md` with proper frontmatter
2. Add any supporting files (REFERENCE.md, scripts, assets)
3. Update the Skills table in `README.md`
4. Commit to this monorepo
5. Create the public GitHub repo (`gh repo create danmurrelljr/{skill-name} --public`)
6. Copy skill folder there, commit, and push

## Inbox / Notes

Drop rough ideas or drafts in `inbox/` and ask the agent to scaffold them into a proper skill folder.
