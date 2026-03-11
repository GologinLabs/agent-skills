# Gologin Agent Skills

Installable Gologin skills for Codex-compatible skill managers.

## Installation Model

This repository is the monorepo install source for all Gologin skills:

```bash
npx skills add GologinLabs/agent-skills@<skill-name>
```

We also keep standalone repositories for the same skills, so both install models work:

- monorepo install from `GologinLabs/agent-skills@...`
- standalone install from `GologinLabs/<skill-repo>`

## Available Skills

### gologin-web-access-skill

Unified web access skill that combines Web Unlocker scraping and Cloud Browser interaction.

Monorepo install:

```bash
npx skills add GologinLabs/agent-skills@gologin-web-access-skill
```

Standalone repo:

- [GologinLabs/gologin-web-access-skill](https://github.com/GologinLabs/gologin-web-access-skill)

CLI repo:

- [GologinLabs/gologin-web-access](https://github.com/GologinLabs/gologin-web-access)

### gologin-agent-browser-skill

Cloud Browser automation skill for live sessions, snapshots, refs, semantic find flows, and browser artifacts.

Monorepo install:

```bash
npx skills add GologinLabs/agent-skills@gologin-agent-browser-skill
```

Standalone repo:

- [GologinLabs/gologin-agent-browser-skill](https://github.com/GologinLabs/gologin-agent-browser-skill)

CLI repo:

- [GologinLabs/agent-browser](https://github.com/GologinLabs/agent-browser)

### gologin-scraping-skill

Scraping-only skill for HTML, text, markdown, metadata extraction, and SDK-based Web Unlocker usage.

Monorepo install:

```bash
npx skills add GologinLabs/agent-skills@gologin-scraping-skill
```

Standalone repo:

- [GologinLabs/gologin-scraping-skill](https://github.com/GologinLabs/gologin-scraping-skill)

SDK repo:

- [GologinLabs/gologin-webunlocker-sdk](https://github.com/GologinLabs/gologin-webunlocker-sdk)

### gologin-local-agent-browser-skill

Local GoLogin Orbita automation skill for persistent profile sessions, warmup, login flows, cookies, runbooks, and batch jobs.

Monorepo install:

```bash
npx skills add GologinLabs/agent-skills@gologin-local-agent-browser-skill
```

Standalone repo:

- [GologinLabs/gologin-local-agent-browser-skill](https://github.com/GologinLabs/gologin-local-agent-browser-skill)

CLI repo:

- [GologinLabs/gologin-local-agent-browser](https://github.com/GologinLabs/gologin-local-agent-browser)

## Repository Layout

This monorepo currently hosts:

- `gologin-web-access-skill/`
- `gologin-agent-browser-skill/`
- `gologin-scraping-skill/`
- `gologin-local-agent-browser-skill/`

## Notes

- Standalone skill repos and this monorepo are intentionally duplicated so users can install either way.
- If you want the shortest standalone install command, use the dedicated repo.
- If you want one shared source for all skills, use this monorepo.
