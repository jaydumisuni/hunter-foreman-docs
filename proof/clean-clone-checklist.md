# Clean Clone Proof Checklist

Use this checklist to prove the three public repositories are judge-ready before final submission.

## Goal

A judge should be able to clone the project, follow the docs, run the connected demo, and understand the value without private context.

## Repositories

```text
hunter-foreman
hunter-foreman-demo
hunter-foreman-docs
```

## Fresh Workspace Layout

```text
workspace/
  hunter-foreman/
  hunter-foreman-demo/
  hunter-foreman-docs/
```

## Step 1 — Clone

```bash
git clone https://github.com/jaydumisuni/hunter-foreman.git
git clone https://github.com/jaydumisuni/hunter-foreman-demo.git
git clone https://github.com/jaydumisuni/hunter-foreman-docs.git
```

Pass criteria:

- all repositories clone successfully
- no private files are required
- no credentials are required for local demo mode

## Step 2 — Run Main App Only

From `hunter-foreman`:

```bash
docker compose up --build
```

Open:

```text
http://localhost:3000
```

Pass criteria:

- ROSE intake loads
- example buttons work
- task creation works
- dashboard updates
- local-only bridge status is clear
- classifier status shows `AI_PROVIDER=mock` or fallback mode when no provider key is configured

## Step 3 — Run Connected Demo

From `hunter-foreman`:

```bash
docker compose -f docker-compose.connected.yml up --build
```

Open:

```text
http://localhost:3000
http://localhost:3100
```

Pass criteria:

- main app shows connected bridge mode
- receiver app shows live stats
- submitting a ROSE request creates a task
- receiver app receives the task
- main app shows receiver acknowledgement
- main app shows state ladder and timeline
- receiver app displays contract payload under details

## Step 4 — API Checks

```bash
curl http://localhost:3000/health
curl http://localhost:3000/api/app-bridge/status
curl http://localhost:3100/health
curl http://localhost:3100/api/tasks
```

Pass criteria:

- all endpoints return JSON
- health checks return ok
- `/health` includes the active AI provider
- `/api/app-bridge/status` shows whether Fireworks credentials are configured
- no token values or private secrets are exposed

## Step 5 — Provider Fallback Check

Run without any provider key.

Pass criteria:

- tasks are still created
- classifier metadata shows fallback/rules mode
- workflow selection is still understandable
- no provider secret is required for local proof

## Step 6 — Provider-Backed Check

When a valid provider key is available, run with:

```bash
AI_PROVIDER=fireworks
FIREWORKS_API_KEY=<configured outside git>
```

Pass criteria:

- task creation still works
- classifier metadata shows provider mode instead of fallback mode
- provider failure still falls back safely
- no key value appears in UI, logs, API responses, commits, screenshots, or demo recording

## Step 7 — AMD / AI Infra Proof Check

Before final AI Infra Summit packaging, complete one of these evidence paths:

```text
A. Run the containerized demo in the hackathon-supported AMD/Fireworks path.
B. Run the provider-backed classifier with the official hackathon-supported Fireworks/AMD configuration.
C. If verified AMD runtime is not available, explicitly mark AMD deployment as pending and do not claim verified AMD use.
```

Pass criteria:

- the submission wording matches the actual proof
- any AMD/Fireworks claim is supported by visible evidence
- if the proof is pending, docs say pending rather than implemented

## Step 8 — Failure Checks

Stop the receiver and submit another request from the main app.

Pass criteria:

- main app does not crash
- dashboard shows dispatch failure or local/receiver issue clearly
- app remains usable

## Step 9 — Public Safety Check

Confirm the public repositories do not contain:

- production credentials
- private Hunter prompts
- client data
- device repair/recovery logic
- payment secrets
- private THETECHGUY internals

## Result

If every pass criterion is met, the three repositories are ready for CodeRabbit review, final owner review, screenshots, and demo recording.