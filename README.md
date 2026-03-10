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

### gologin-local-agent-browser-skill

Local GoLogin Orbita automation skill for persistent profile sessions, warmup, login flows, and cookie-oriented browser work.

Skill install:

```bash
npx skills add GologinLabs/agent-skills@gologin-local-agent-browser-skill
```

CLI source in this workspace:

- [`gologin-local-agent-browser`](/Users/eugene/Desktop/vibe%20coding%20projects/gologin-local-agent-browser)

## Repository Layout

This repository currently hosts:

- `gologin-web-access-skill/`
- `gologin-local-agent-browser-skill/`

Standalone skill repos:

- [GologinLabs/gologin-scraping-skill](https://github.com/GologinLabs/gologin-scraping-skill)
- [GologinLabs/gologin-agent-browser-skill](https://github.com/GologinLabs/gologin-agent-browser-skill)
