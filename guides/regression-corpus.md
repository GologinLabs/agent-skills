# Regression Corpus From Real Agent Sessions

Use these scenarios to verify routing, defaults, and error handling after any CLI or skill change.

## 1. Known Docs Page

Intent:

- `Read the Browserbase docs page about contexts and summarize it`

Expected lane:

- `gologin-web-access`

Expected behavior:

- one-command path through `read`
- if the page is JS-heavy, the readable path still returns useful content
- no manual `open -> eval -> close` loop

## 2. Live Dashboard Login

Intent:

- `Use GoLogin Cloud Browser to log into this dashboard and take a screenshot`

Expected lane:

- `gologin-agent-browser`

Expected behavior:

- no drift into `gologin-web-access`
- no drift into local Orbita unless cloud capacity is unavailable and the user agrees
- session cleanup guidance is obvious

## 3. Local SPA With Persistent State

Intent:

- `Use my existing local GoLogin profile to continue browsing this React SPA and extract the rendered DOM`

Expected lane:

- `gologin-local-agent-browser`

Expected behavior:

- no raw `gologin` SDK scripts
- no cloud-browser reroute
- rendered DOM is read from the live local profile

## 4. Parallel Cloud Sessions

Intent:

- `Open two cloud sessions in parallel and inspect both pages`

Expected lane:

- `gologin-agent-browser`

Expected behavior:

- explicit `--session` ids such as `s1` and `s2`
- no unnecessary serialization
- cleanup path documented with `sessions --prune` and `close --all`

## 5. Proxy Strategy Preflight

Intent:

- `Create a new profile for LinkedIn and prepare it for routine browsing`

Expected lane:

- `gologin-local-agent-browser`

Expected behavior:

- ask whether to use no proxy, GoLogin country traffic, or a custom proxy
- do not invent free proxies
- use `profile-create --template linkedin`

## 6. Temporary Cloud Session With Explicit Country Requirement

Intent:

- `Use Cloud Browser with a US GoLogin proxy`

Expected lane:

- `gologin-agent-browser`

Expected behavior:

- explain that temporary cloud sessions do not support `--proxy-country`
- recommend an existing preconfigured cloud `--profile`
- do not silently fall back to some other proxy path
