# Gologin Agent Skills

Installable Gologin skills for Codex-compatible skill managers.

## Installation Model

CLI and skill are installed differently on purpose.

CLI install:

```bash
npm install -g gologin-web-access
```

Skill install:

```bash
npx skills add GologinLabs/agent-skills@gologin-web-access-skill
```

The CLI repository is:

- [GologinLabs/gologin-web-access](https://github.com/GologinLabs/gologin-web-access)

The installable skill repository is:

- [GologinLabs/agent-skills](https://github.com/GologinLabs/agent-skills)

## Available Skills

### gologin-web-access-skill

Read webpages and interact with websites through Gologin Web Unlocker and Gologin Cloud Browser.

Install:

```bash
npx skills add GologinLabs/agent-skills@gologin-web-access-skill
```

Install globally without prompts:

```bash
npx skills add GologinLabs/agent-skills@gologin-web-access-skill -g -y
```

## Repository Layout

Each installable skill lives in its own top-level folder:

- `gologin-web-access-skill/`

Future Gologin skills can be added as additional top-level folders in this repository.
