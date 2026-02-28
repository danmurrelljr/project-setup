# Claude Skills — Monorepo

Private collection of custom Claude skills built for personal use and open-sourced individually.

## Structure

Each subdirectory is a self-contained Claude skill:

```
skills/
  {skill-name}/        # One folder per skill
    Skill.md           # Required: YAML frontmatter + instructions
    REFERENCE.md       # Optional: supplemental docs
    scripts/           # Optional: Python/JS executables
```

## Publishing Workflow

Each skill has its own public GitHub repo (`danmurrelljr/{skill-name}`). This monorepo is the private workspace.

When a skill is ready to publish or updated:
1. Copy the skill folder to its individual repo (or use the sync workflow in AGENTS.md)
2. Push to the public GitHub repo
3. Zip the skill folder and upload to Claude via **Customize > Skills**

## Skills

| Skill | Description | Public Repo |
|-------|-------------|-------------|
| _(none yet)_ | | |
