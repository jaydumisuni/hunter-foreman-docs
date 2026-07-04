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
- no token values or private secrets are exposed

## Step 5 — Failure Checks

Stop the receiver and submit another request from the main app.

Pass criteria:

- main app does not crash
- dashboard shows dispatch failure or local/receiver issue clearly
- app remains usable

## Step 6 — Public Safety Check

Confirm the public repositories do not contain:

- production credentials
- private Hunter prompts
- client data
- device repair/recovery logic
- payment secrets
- private THETECHGUY internals

## Result

If every pass criterion is met, the three repositories are ready for CodeRabbit review, final owner review, screenshots, and demo recording.
