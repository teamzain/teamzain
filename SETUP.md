# How this profile works

Built on the generators from [gargibhardwaj24's profile guide](https://github.com/gargibhardwaj24/gargibhardwaj24), re-themed in navy/steel blue to match my photo.

## What regenerates itself

| workflow | makes | when |
|---|---|---|
| **Charts and cards** (`radar.yml`) | dot-matrix portrait (from my current avatar), both skill radars, stat card, project cards | daily + on changes to `assets/*.json` / `scripts/` |
| **Snake** (`snake.yml`) | snake eating the contribution graph, on the `output` branch | every 12h + on push |
| **Metrics** (`metrics.yml`) | 3D calendar, language mix, achievements | every 6h, **only once `METRICS_TOKEN` is set** |

## Files to edit

- `assets/skills.json` – self-rated radar (0–100, 5–8 axes)
- `assets/projects.json` – the four featured repos and their one-line pitches
- `README.md` – layout and words

## Optional: unlock the 3D calendar, achievements and full stat card

1. github.com/settings/tokens → **Generate new token (classic)** → scope `read:user` (add `repo` to count private work)
2. This repo → Settings → Secrets and variables → Actions → **New repository secret** → name `METRICS_TOKEN`
3. Actions tab → Metrics → **Run workflow**, then add the `assets/metrics.*.svg` images to the README

## If something breaks

- Workflow succeeds but nothing updates → Settings → Actions → General → Workflow permissions → **Read and write**
- Snake images 404 → the Snake workflow hasn't finished its first run yet
- Metrics stops working months later → the token expired; make a new one
