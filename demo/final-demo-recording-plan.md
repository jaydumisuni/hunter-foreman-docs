# Final Demo Recording Plan

Target length: **2 to 3 minutes**.

Goal: show that Hunter Foreman moves a customer request into owned, visible work across an app boundary.

## Recording flow

### Scene 1 — Problem / product identity

Duration: 10 to 15 seconds.

Show:

- Hunter Foreman main screen.
- One sentence voiceover or caption.

Suggested line:

```text
Small businesses do not only need chatbot replies. They need customer requests to become owned work.
```

### Scene 2 — ROSE receives request

Duration: 20 to 25 seconds.

Show:

- ROSE intake form/chat.
- Submit a realistic request.

Suggested request:

```text
We need wedding invitations, tickets, and QR check-in support for a conference.
```

Suggested line:

```text
ROSE captures the customer request and passes it to Foreman.
```

### Scene 3 — Foreman creates work

Duration: 25 to 35 seconds.

Show:

- Created task.
- Intent/confidence/escalation state if visible.
- Dashboard update.

Suggested line:

```text
Foreman classifies the request, selects the workflow, creates a task, and makes the work visible.
```

### Scene 4 — App bridge dispatch

Duration: 25 to 35 seconds.

Show:

- Bridge status or dispatch event.
- App bridge contract if needed.

Suggested line:

```text
The app bridge sends the structured task to a connected receiver using a versioned contract.
```

### Scene 5 — Receiver acknowledgement

Duration: 25 to 35 seconds.

Show:

- `hunter-foreman-demo` receiver page.
- Received task.
- Acknowledgement/stat update.

Suggested line:

```text
The external receiver accepts the task and acknowledges it back into the workflow.
```

### Scene 6 — Proof and safety

Duration: 25 to 35 seconds.

Show:

- Submission Proof success or repo proof matrix.
- Fireworks attempt report if useful.
- Public safety boundary if useful.

Suggested line:

```text
The public version is containerized, reproducible, and scoped safely without private credentials or internal Hunter systems.
```

### Scene 7 — Closing

Duration: 10 to 15 seconds.

Show:

- Dashboard or final state.

Suggested line:

```text
Hunter Foreman turns AI from a chat response into an operations layer that moves work between real applications.
```

## What not to show

- API keys.
- Fireworks key screen.
- Private accounts.
- Payment methods.
- Private Hunter internals.
- Device repair/recovery modules.
- Long terminal troubleshooting.

## If Fireworks account is still blocked

Do not mention the billing issue in the main demo unless asked.

Use this wording only in docs or Q&A:

```text
The Fireworks provider path is implemented and the live verification script is merged. A live serverless run was attempted but blocked by Fireworks account status, so the demo uses the verified deterministic fallback path.
```

## Final demo success criteria

A judge should understand these points without extra explanation:

- The project is not only a chatbot.
- A request becomes structured work.
- Work appears in a dashboard.
- A connected app receives and acknowledges the task.
- The system has a safe fallback.
- The public repo is reproducible and scoped safely.
