# Choosing the Right GoLogin Tool

Use this as the first routing checkpoint before the agent opens a browser or scrapes a page.

## Quick Decision Table

Use `gologin-web-access` when:

- the user already has a target URL or a known site
- the task is reading, extracting, mapping, crawling, monitoring, or scrape-first research
- stateless access through Web Unlocker is likely enough
- the task starts as read-only and may escalate into light browser work later

Use `gologin-agent-browser` when:

- the task is primarily a live Cloud Browser session
- the agent must log in, click, type, upload, wait, capture screenshots or PDFs, or manage cloud session slots
- multiple cloud sessions should run in parallel with explicit `--session` ids
- session cleanup itself is part of the task

Use `gologin-local-agent-browser` when:

- the task must run through a local Orbita profile
- cookies, local storage, and browsing state should persist across runs on this machine
- the target is a SPA and repeated rendered-DOM navigation matters more than stateless scraping
- the user wants profile preparation, account routines, cookie persistence, or multi-account local automation

## Hard Boundaries

- Do not use `gologin-web-access` as a substitute for a pure cloud-browser workflow.
- Do not use `gologin-agent-browser` when the task is really scrape-first reading on a known site.
- Do not use `gologin-local-agent-browser` by importing the raw `gologin` SDK. Use the CLI.

## Proxy Rules

- `gologin-web-access`: ask for both `GOLOGIN_TOKEN` and `GOLOGIN_WEB_UNLOCKER_API_KEY` up front.
- `gologin-agent-browser`: temporary cloud sessions support no proxy or a custom proxy host/port. Use an explicit cloud `--profile` for GoLogin country traffic or predictable browser settings.
- `gologin-local-agent-browser`: always ask which proxy mode to use before creating or mutating a profile.

## Language That Works Better With Models

When asking the agent to do persistent account work, prefer:

- `profile preparation`
- `session setup`
- `routine browsing`
- `account session initialization`

Avoid relying on loaded wording when a neutral phrase will do.
