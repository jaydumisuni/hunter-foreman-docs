# Final Submission Draft

## Project Name

Hunter Foreman

## Tagline

AI operations infrastructure for small businesses — from customer request to owned work.

## Short Description

Hunter Foreman turns customer requests into structured work. ROSE receives the request, Foreman classifies it through a provider-backed classifier or safe deterministic fallback, chooses the workflow, creates a task, updates the dashboard, dispatches the task through a versioned app bridge, and receives acknowledgement from a connected application.

## Problem

Small businesses often receive requests through websites, WhatsApp, email, phone calls, social media, and staff conversations. The problem is not only answering the customer. The deeper problem is ownership: who captured the request, who understands it, who routes it, who follows up, and where the business can see the work state.

Most chatbot demos stop at the reply. A real business needs the work to move.

## Solution

Hunter Foreman is a public-safe proof of an AI operations layer.

It demonstrates:

- AI receptionist intake through ROSE
- provider-backed Foreman classification with explicit fallback
- workflow selection
- task creation with confidence and escalation state
- live dashboard visibility
- notification previews
- versioned external app bridge contract
- connected receiver app acknowledgement
- public/private boundary for safe demonstration

## What Was Built

The submission is split across three public repositories:

1. `hunter-foreman` — main public demo app
2. `hunter-foreman-demo` — connected external receiver app
3. `hunter-foreman-docs` — submission pack, pitch material, proof checklist, and judge documentation

The main app now supports:

```text
AI_PROVIDER=fireworks  -> provider-backed classification through Fireworks-compatible chat completions
AI_PROVIDER=mock/rules -> deterministic local fallback for judge-safe demos
```

No API keys or private credentials are committed. If the provider is not configured, the app still runs and marks fallback usage in the task classifier metadata.

## Demo Flow

```text
Customer request
   ↓
ROSE intake
   ↓
Foreman provider/fallback classification
   ↓
Task created
   ↓
Dashboard updated
   ↓
App bridge dispatch
   ↓
Connected receiver app
   ↓
Receiver acknowledgement
   ↓
Visible state ladder and timeline
```

## AI Infra / AMD Positioning

Hunter Foreman is containerized and includes a real provider-backed classifier path. For AI Infra Summit submission, the honest current position is:

- implemented: Dockerized public app and receiver demo
- implemented: Fireworks-compatible provider classifier path
- implemented: deterministic fallback for reproducible local judging
- pending proof: AMD-aligned provider/container run evidence before final packaging

The project should only claim verified AMD platform use after the provider-backed run is performed and documented in the proof checklist.

## Why It Matters

This project reframes AI from a conversation tool into an operations layer. A small business should not need a large software team to organize work, connect apps, and see what is happening. Hunter Foreman shows how an AI-assisted system can receive, route, track, and escalate work while keeping humans in control.

## Public Safety Boundary

This public version intentionally excludes:

- private Hunter internals
- production credentials
- private prompts
- client data
- payment secrets
- device repair/recovery logic
- sensitive THETECHGUY business internals

The public repositories demonstrate the architecture, not private production systems.

## Judging Notes

Judges should evaluate the project as infrastructure, not as a single chatbot. The important part is that a request moves through a full operational lifecycle and can be dispatched to another application through a versioned contract.

## Future Direction

The same architecture can later support Events, Sales, Support, Payments, Field Work, Device Service, and internal business automation. Hunter Foreman is the operating layer that coordinates those systems.