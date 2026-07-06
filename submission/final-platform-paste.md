# Final Platform Paste Text

Use this as the base text for the hackathon submission platform. Adjust only for platform word limits.

## Project title

Hunter Foreman

## Tagline

AI operations infrastructure for small businesses — from customer request to owned work.

## Short description

Hunter Foreman turns customer requests into structured work. ROSE receives the request, Foreman classifies it through a provider-backed classifier or safe deterministic fallback, chooses the workflow, creates a task, updates the dashboard, dispatches the task through a versioned app bridge, and receives acknowledgement from a connected application.

## Problem

Small businesses receive customer requests through websites, WhatsApp, email, phone calls, social media, and staff conversations. The problem is not only answering the customer. The deeper problem is ownership: who captured the request, who understands it, who routes it, who follows up, and where the business can see the work state.

Most chatbot demos stop at the reply. A real business needs the work to move.

## Solution

Hunter Foreman is an AI operations layer for small businesses. It demonstrates a full operational lifecycle:

1. ROSE receives a customer request.
2. Foreman classifies the request through a provider-backed path or deterministic fallback.
3. The system selects the workflow and creates a task.
4. The dashboard shows confidence, ownership, escalation state, and notification previews.
5. A versioned app bridge dispatches the task to a connected receiver app.
6. The receiver acknowledges the event and shows the bridged task state.

This proves the pattern: AI does not only answer. It helps move work into systems the business can track.

## What we built

The submission is split across public repositories:

- `jaydumisuni/hunter-foreman` — main public demo app
- `jaydumisuni/hunter-foreman-demo` — connected receiver app
- `jaydumisuni/hunter-foreman-docs` — submission pack, proof, demo guides, and judge documentation
- `jaydumisuni/Sergeant` — supporting reviewer/proof layer used to protect claim boundaries and review readiness

The main app includes:

- ROSE request intake
- Foreman classifier path
- deterministic fallback
- task creation
- dashboard state
- app bridge dispatch
- receiver acknowledgement
- Docker support
- public-safe repository split
- Fireworks-compatible provider path
- live verification script
- explicit proof boundary for external provider/account status

## AI infrastructure angle

Hunter Foreman is not just a chatbot. It is infrastructure for coordinating AI-assisted work.

It includes:

- intake layer
- provider-backed classification layer
- deterministic fallback layer
- task lifecycle layer
- dashboard state layer
- versioned app bridge
- connected receiver app
- human escalation path
- containerized local demo path

The Fireworks-compatible provider path is implemented and a live verification script is merged. A real Fireworks serverless call was attempted using a documented serverless model, but live inference was blocked by Fireworks account billing/suspension status. The system correctly fell back to its deterministic classifier without crashing. We do not claim live Fireworks verification unless a later successful provider run is captured.

## Public safety boundary

The public hackathon version intentionally excludes private Hunter internals, production credentials, private prompts, client data, payment secrets, device repair/recovery logic, and sensitive THETECHGUY business internals.

The public repositories demonstrate the architecture safely without exposing private production systems.

## Demo flow

Customer request → ROSE intake → Foreman classification → Task created → Dashboard updated → App bridge dispatch → Receiver acknowledgement → Visible state ladder and timeline.

## Why it matters

Hunter Foreman reframes AI from a conversation tool into an operations layer. Small businesses should not need a large software team to capture requests, connect apps, route work, and understand what is happening. This project shows how AI-assisted operations can make work visible, trackable, and owned.

## Final line

Hunter Foreman turns AI from a response into operational movement.

## Repository links

- Main app: https://github.com/jaydumisuni/hunter-foreman
- Receiver app: https://github.com/jaydumisuni/hunter-foreman-demo
- Submission docs: https://github.com/jaydumisuni/hunter-foreman-docs
- Supporting reviewer/proof layer: https://github.com/jaydumisuni/Sergeant
