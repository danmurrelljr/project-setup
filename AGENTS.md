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

Individual skills sync to their GitHub repos via `git subtree push`. Each skill's push command is listed in the Skills table below.

When asked to "sync skills" or "publish {skill-name}":
1. Commit any changes in the monorepo
2. Run the skill's subtree push command (see Skills table)
3. Remind the user to re-upload the zip to Claude at Customize > Skills if `Skill.md` or any resource file changed

## Skills

| Skill | GitHub Repo | Subtree Push Command |
|-------|-------------|----------------------|
| [project-setup](./project-setup/) | [danmurrelljr/project-setup](https://github.com/danmurrelljr/project-setup) (private) | `git subtree push --prefix=project-setup project-setup main` |

## Creating a New Skill

1. Create `{skill-name}/Skill.md` with proper frontmatter
2. Add `README.md` and `LICENSE` (MIT)
3. Add any supporting files (REFERENCE.md, scripts, assets)
4. Update the Skills table in this file and in `README.md`
5. Commit to this monorepo and push to madcap
6. Create the GitHub repo: `gh repo create danmurrelljr/{skill-name} --private --description "..."`
7. Add the remote: `git remote add {skill-name} https://github.com/danmurrelljr/{skill-name}.git`
8. Push via subtree: `git subtree push --prefix={skill-name} {skill-name} main`

## Inbox / Notes

Drop rough ideas or drafts in `inbox/` and ask the agent to scaffold them into a proper skill folder.
