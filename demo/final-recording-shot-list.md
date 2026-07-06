# Final Demo Recording Shot List

This is the exact capture plan for the final hackathon demo video.

Target length: 2:30 to 3:00.

## Recording setup

Run the connected two-app demo:

```bash
docker compose -f docker-compose.connected.yml up --build
```

Open:

```text
http://localhost:3000
http://localhost:3100
```

Use browser zoom around 90% to 100% so the dashboard, bridge status, receiver acknowledgement, and timeline are visible.

## Shot 1 — Opening / Main app

Time: 0:00 to 0:15

Show:

- Hunter Foreman main page
- ROSE intake area
- dashboard/work state area

Voice line:

```text
Hunter Foreman is an AI operations foreman for small businesses. It turns customer requests into owned work, not just chat replies.
```

## Shot 2 — Customer request into ROSE

Time: 0:15 to 0:45

Paste this request:

```text
We need event booking, digital invitations, guest tickets, QR check-in and a clear approval flow.
```

Click the send/request button.

Show:

- request submitted
- task created
- workflow classification
- confidence/escalation state

Voice line:

```text
ROSE receives the request, Foreman classifies it, chooses the workflow, creates a task, and records the state for the business.
```

## Shot 3 — Dashboard proof

Time: 0:45 to 1:15

Show:

- created task
- status/state ladder
- owner/escalation/notification preview if visible
- classifier/fallback metadata if visible

Voice line:

```text
The dashboard is the proof of ownership. The request now has a workflow, a task record, confidence, escalation state, and visible progress.
```

## Shot 4 — App bridge status

Time: 1:15 to 1:40

Show:

- app bridge section
- connected mode / receiver status
- dispatch or acknowledgement area

Voice line:

```text
The app bridge is versioned, so Foreman can dispatch structured work to another application instead of keeping everything inside one chat window.
```

## Shot 5 — Receiver app acknowledgement

Time: 1:40 to 2:20

Switch to:

```text
http://localhost:3100
```

Show:

- receiver stats
- received task
- event ID / contract version
- timeline
- raw payload/details if visible

Voice line:

```text
The receiver app proves this is a connected workflow. It receives the task event, acknowledges it, and shows the same work state from the external application side.
```

## Shot 6 — Close / proof boundary

Time: 2:20 to 2:55

Return to main app or show final dashboard state.

Voice line:

```text
The public version is intentionally safe. It excludes private systems and secrets, but proves the infrastructure pattern: intake, classification, task creation, app bridge dispatch, acknowledgement, and human-visible state.
```

Final line:

```text
Hunter Foreman turns AI from a response into operational movement.
```

## Screenshot checklist

Capture these still images for the submission page:

1. Main Hunter Foreman screen before request.
2. ROSE request entered.
3. Task created on dashboard.
4. App bridge connected/dispatch state.
5. Receiver app showing received task.
6. Receiver raw payload or timeline.
7. Submission proof or docs README if the platform allows proof screenshots.

## Do not show

- API keys
- private Fireworks dashboard details
- billing pages
- private Hunter internals
- unrelated THETECHGUY private systems
- local folders with sensitive names beyond the public repo names

## If Fireworks support responds before recording

Rerun:

```powershell
cd D:\projects\hunter-foreman
$env:FIREWORKS_MODEL="accounts/fireworks/models/llama4-maverick-instruct-basic"
node scripts/test-fireworks-live.js
```

Only mention live Fireworks verification in the video if the script passes with:

```text
provider=fireworks
fallbackUsed=false
```

Otherwise, do not mention live Fireworks verification in the demo video. The demo should focus on the working product flow.
