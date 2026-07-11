# Final Submission Record

## Project Name

Hunter Foreman

## Tagline

AI operations infrastructure for small businesses — from customer request to owned work.

## Short Description

Hunter Foreman turns customer requests into structured work. ROSE receives the request, Foreman classifies it through Fireworks AI or a safe deterministic fallback, chooses the workflow, creates a task, updates the dashboard, dispatches the task through a versioned App Bridge, and receives acknowledgement from a connected application.

## Problem

Small businesses often receive requests through websites, WhatsApp, email, phone calls, social media, and staff conversations. The problem is not only answering the customer. The deeper problem is ownership: who captured the request, who understands it, who routes it, who follows up, and where the business can see the work state.

Most chatbot demos stop at the reply. A real business needs the work to move.

## Solution

Hunter Foreman is a public-safe proof of an AI operations layer.

It demonstrates:

- AI receptionist intake through ROSE
- verified Fireworks AI classification with explicit fallback
- workflow selection
- task creation with confidence and escalation state
- live dashboard visibility
- versioned external App Bridge contract
- connected receiver acknowledgement
- public/private boundary for safe demonstration

## Public Submission Entry Points

- Main public repository: https://github.com/jaydumisuni/hunter-foreman
- Public demo application: https://hunter-foreman.thetechguyds.com
- Local/Docker application: http://localhost:3000

## Presentation Voice and Ecosystem Reuse

The official presentation video is narrated using **Hunter’s internal voice system**. This demonstrates practical reuse of the broader THETECHGUY AI ecosystem for product communication and future voice-enabled interfaces.

The voice narration is a presentation-layer integration, separate from the Hunter Foreman runtime capabilities described in this submission.

Submission-form technology note:

```text
Hunter internal voice system — official presentation narration and ecosystem reuse.
```

Recommended Additional Information wording:

```text
The official Hunter Foreman presentation is narrated using Hunter’s internal voice system, demonstrating that the project was developed and presented within a broader reusable AI ecosystem. The voice layer supports the presentation and is not claimed as a Hunter Foreman runtime feature in this public release.
```

## Repository Map

The implementation is split across three public repositories:

1. [hunter-foreman](https://github.com/jaydumisuni/hunter-foreman) — main public application, Docker setup, and proof package
2. [hunter-foreman-demo](https://github.com/jaydumisuni/hunter-foreman-demo) — connected external receiver application
3. [hunter-foreman-docs](https://github.com/jaydumisuni/hunter-foreman-docs) — submission pack, pitch material, architecture, and judge documentation

[Sergeant](https://github.com/jaydumisuni/Sergeant) is the supporting implementation reviewer/proof layer shaped through Hunter Foreman.

The main app supports:

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
Foreman Fireworks/fallback classification
   ↓
Task created
   ↓
Dashboard updated
   ↓
App Bridge dispatch
   ↓
Connected receiver app
   ↓
Receiver acknowledgement
   ↓
Visible state ladder and timeline
```

## AI Infrastructure / AMD Positioning

Hunter Foreman is containerized and includes a verified Fireworks-backed classifier path.

Current evidence:

- implemented: Dockerized public application and receiver demo
- implemented: Fireworks-compatible provider classifier path
- verified: successful Fireworks classifications using `accounts/fireworks/models/gpt-oss-120b`
- verified: proof records `provider: fireworks` and `fallbackUsed: false`
- implemented and verified: deterministic fallback for reproducible judging when provider credentials are unavailable

The successful provider evidence is stored in the core repository at:

```text
proof/fireworks-classification-proof.json
```

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

Judges should evaluate the project as infrastructure, not as a single chatbot. The important part is that a request moves through a complete operational lifecycle and can be dispatched to another application through a versioned contract.

The Hunter voice narration should be considered supporting ecosystem integration and evidence of reusable internal AI infrastructure, not a claim that voice interaction is part of the current Foreman runtime.

## Future Direction

The same architecture can later support Events, Sales, Support, Payments, Field Work, Device Service, and internal business automation. Hunter Foreman is the operating layer that coordinates those systems.

## Submission Status

Submitted to **Track 3 — Unicorn Track**. The main repository field points to `jaydumisuni/hunter-foreman`, while the main README maps the related public repositories as required.