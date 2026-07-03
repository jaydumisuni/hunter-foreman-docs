# Demo Run Guide

## Repositories

Place the two app repositories beside each other:

```text
workspace/
  hunter-foreman/
  hunter-foreman-demo/
```

## Option 1 — Main App Only

From `hunter-foreman`:

```bash
docker compose up --build
```

Open:

```text
http://localhost:3000
```

This mode demonstrates local ROSE intake, Foreman routing, task creation, dashboard updates, and notification previews.

## Option 2 — Connected Two-App Demo

From `hunter-foreman`:

```bash
docker compose -f docker-compose.connected.yml up --build
```

Open both apps:

```text
http://localhost:3000
http://localhost:3100
```

Submit a request in the main app. The receiver app should display the task with contract version, event type, and timeline.

## Demo Request

```text
We need event booking, digital invitations, guest tickets, QR check-in and a clear approval flow.
```

## What To Show Judges

1. ROSE receives the request.
2. Foreman routes it to a workflow.
3. A task is created.
4. The app bridge status shows connected mode.
5. The receiver app displays the bridged task.
6. The timeline shows ROSE → Foreman → AppBridge.

## Reset

Stop the containers and start again. The demo stores tasks in memory only for this public phase.
