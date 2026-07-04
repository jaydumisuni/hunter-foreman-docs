# App Bridge Contract

## Purpose

The app bridge contract is the public-safe boundary between Hunter Foreman and any connected business application.

It proves that Foreman can move work out of the AI intake dashboard and into another app without exposing private Hunter internals.

## Contract Version

```text
foreman.app.task.v1
```

## Direction

```text
Hunter Foreman
   ↓ POST /foreman/tasks
Connected Receiver App
   ↓ acknowledgement
Hunter Foreman Dashboard
```

## Core Envelope

```json
{
  "contract": "foreman.app.task.v1",
  "eventId": "HF-DEMO-1-1234567890",
  "eventType": "task.created",
  "source": "hunter-foreman",
  "createdAt": "2026-07-04T00:00:00.000Z",
  "task": {
    "id": "HF-DEMO-1",
    "customerName": "Demo Customer",
    "channel": "website",
    "message": "Customer request text",
    "workflow": {
      "label": "Business Automation Workflow",
      "owner": "Automation Team"
    },
    "status": "ready_to_assign"
  },
  "timeline": [
    {
      "actor": "ROSE",
      "action": "request_received"
    },
    {
      "actor": "Foreman",
      "action": "task_created"
    },
    {
      "actor": "AppBridge",
      "action": "dispatch_requested"
    }
  ]
}
```

## Receiver Response

```json
{
  "ok": true,
  "received": {
    "contract": "foreman.app.task.v1",
    "eventId": "HF-DEMO-1-1234567890",
    "eventType": "task.created",
    "source": "hunter-foreman",
    "receivedAt": "2026-07-04T00:00:01.000Z",
    "receiverState": "accepted",
    "task": {
      "id": "HF-DEMO-1"
    }
  }
}
```

## Why Versioning Matters

The version lets future receiver apps know which payload shape they are accepting. That means Events, Support, Sales, Payments, or other business apps can integrate without depending on private implementation details.

## Current Demo Guarantees

- The receiver can reject missing task IDs.
- The receiver can report unsupported contract versions.
- The main app can show local-only mode when no receiver is configured.
- The main app can show receiver acknowledgement when connected.
- The dashboard can show dispatch failure without crashing.

## Future Contract Growth

Future versions can add:

- staff assignment
- SLA timers
- customer update status
- payment state
- event booking metadata
- signed payload verification
- retry and idempotency fields
