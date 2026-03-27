# Rollout Guide For Non-Programmers

This is the shortest path to getting the GoLogin agent stack working without learning the whole codebase.

## 1. Install the CLIs

```bash
npm install -g gologin-web-access
npm install -g gologin-agent-browser-cli
npm install -g gologin-local-agent-browser-cli
```

## 2. Install the Skills

```bash
npx skills add GologinLabs/gologin-web-access-skill
npx skills add GologinLabs/gologin-agent-browser-skill
npx skills add GologinLabs/gologin-local-agent-browser-skill
```

## 3. Configure the Keys

GoLogin uses one main token for browser work and one extra key for Web Unlocker scraping:

```bash
export GOLOGIN_TOKEN="your_gologin_token"
export GOLOGIN_WEB_UNLOCKER_API_KEY="your_web_unlocker_key"
```

If you do not want to re-export them in every shell:

```bash
gologin-web-access config init --token "$GOLOGIN_TOKEN" --web-unlocker-key "$GOLOGIN_WEB_UNLOCKER_API_KEY"
```

## 4. Add a Routing Snippet to `AGENTS.md`

```md
## Web Access Priority
- Prefer `gologin-web-access-skill` for known-site reading, extraction, mapping, crawling, monitoring, and scrape-first hybrid GoLogin tasks.
- Prefer `gologin-agent-browser-skill` for live GoLogin Cloud Browser sessions, interactive logins, dashboard work, screenshots, PDFs, parallel cloud sessions, and cloud-session hygiene.
- Prefer `gologin-local-agent-browser-skill` for local GoLogin Orbita profiles, profile preparation, cookie persistence, account sessions, and multi-account automation.
```

## 5. Use the Right Prompt Pattern

Good:

- `Read this docs page with gologin-web-access and summarize the main points`
- `Use gologin-agent-browser to log into this dashboard and take a screenshot`
- `Use gologin-local-agent-browser with my existing profile to continue the session on this SPA`

Better for persistent account work:

- `profile preparation`
- `session setup`
- `routine browsing`

## 6. Clean Up Sessions When Cloud Slots Fill Up

```bash
gologin-agent-browser sessions
gologin-agent-browser sessions --prune --older-than-ms 300000
gologin-agent-browser close --all
```

## 7. Three Fast Troubleshooting Checks

When scraping seems empty:

```bash
gologin-web-access read https://example.com --format text
```

When cloud browser feels stuck:

```bash
gologin-agent-browser doctor
gologin-agent-browser sessions
```

When local Orbita is unclear:

```bash
gologin-local-agent-browser doctor --json
```
