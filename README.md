# DemoX Demo Library

A self-hosted, searchable library of DemoX HTML demos. Add a demo folder, push to GitHub, and it's live automatically.

## How it works

1. Every demo lives in `demos/<demo-id>/`
2. Each folder needs `index.html` (the demo) and `demo.yaml` (the metadata)
3. If the demo was built with Claude Code or Blueprint MCP, include a `claude.md` so it can be regenerated or extended later
4. When you push to `main`, GitHub automatically rebuilds `demos.json` and publishes everything to GitHub Pages

## Adding a demo

```
demos/
  my-new-demo/
    index.html    ← your demo file
    demo.yaml     ← required metadata
    claude.md     ← optional, include if built with AI tooling
```

### demo.yaml fields

```yaml
title: "Short descriptive title"
description: >
  One or two sentences on what the demo shows.
vertical: Logistics          # Logistics | Financial services | Healthcare | CPG | Insurance
product:
  - Blueprint                # Blueprint | CDH | Pega Platform | Cosmos
type: Scenario               # Scenario | Walkthrough | Concept | Interactive
region: AMS                  # AMS | EMEA | APJ
persona: Business stakeholder
duration_minutes: 8
status: active               # active | draft | archived
event: null                  # or e.g. "Pega World 2025"
iframe_safe: true            # false if the demo has CSP/X-Frame issues
owner: DemoX AMS
source_tool: Claude Code     # Claude Code | Cursor | Bolt | Blueprint MCP | Manual
tags:
  - recall
  - cpg
```

### claude.md

Include this file if the demo was built with an AI tool. It should capture:
- What the demo is for and who the audience is
- The scenario and narrative beats
- Design decisions and tone guidelines
- Any constraints (e.g. iframe restrictions, screen size targets)
- How to regenerate or extend it

This is the demo's memory. Anyone on the team — or Claude Code — can pick it up and continue the work.

## One-time GitHub setup

1. Create a new GitHub repo and push this folder to it
2. Go to **Settings → Pages → Source** and set it to **GitHub Actions**
3. That's it — the workflow in `.github/workflows/publish.yml` handles everything from there

Your library will be live at `https://<your-org>.github.io/<repo-name>/`

## Running locally

```bash
python3 scripts/build-index.py   # generates demos.json
python3 -m http.server 8000       # serves the site at localhost:8000
```
