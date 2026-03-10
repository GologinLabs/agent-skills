# Gologin Agent Skills

Installable Gologin skills for Codex-compatible skill managers.

## Installation Model

CLI packages and skills are installed differently on purpose.

Skill install pattern:

```bash
npx skills add GologinLabs/agent-skills@<skill-name>
```

## Available Skills

### gologin-web-access-skill

Unified web access skill that combines Web Unlocker scraping and Cloud Browser interaction.

Skill install:

```bash
npx skills add GologinLabs/agent-skills@gologin-web-access-skill
```

CLI install:

```bash
npm install -g gologin-web-access
```

CLI repo:

- [GologinLabs/gologin-web-access](https://github.com/GologinLabs/gologin-web-access)

## Repository Layout

This repository currently hosts:

- `gologin-web-access-skill/`

Standalone skill repos:

- [GologinLabs/gologin-webunlocker-skill](https://github.com/GologinLabs/gologin-webunlocker-skill)
- [GologinLabs/gologin-agent-browser-skill](https://github.com/GologinLabs/gologin-agent-browser-skill)
