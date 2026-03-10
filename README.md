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

### gologin-webunlocker-skill

Scraping-only skill built around the `gologin-webunlocker-sdk` package and `gologin-webunlocker` CLI.

Skill install:

```bash
npx skills add GologinLabs/agent-skills@gologin-webunlocker-skill
```

Package install:

```bash
npm install gologin-webunlocker-sdk
```

Optional CLI install:

```bash
npm install -g gologin-webunlocker-sdk
```

### gologin-agent-browser-skill

Browser-only skill built around the `gologin-agent-browser-cli` package and `gologin-agent-browser` command.

Skill install:

```bash
npx skills add GologinLabs/agent-skills@gologin-agent-browser-skill
```

CLI install:

```bash
npm install -g gologin-agent-browser-cli
```

CLI repo:

- [GologinLabs/agent-browser](https://github.com/GologinLabs/agent-browser)

## Repository Layout

Each installable skill lives in its own top-level folder:

- `gologin-web-access-skill/`
- `gologin-webunlocker-skill/`
- `gologin-agent-browser-skill/`

Future Gologin skills can be added as additional top-level folders in this repository.
