# Three-Minute Demo Script

## 0:00 — Opening

Hunter Foreman is an AI operations foreman for small businesses. This demo shows a customer request moving from intake to routed work, then into a connected external application.

## 0:15 — Show the Main App

Open the main app:

```text
http://localhost:3000
```

Explain:

ROSE is the intake layer. Foreman is the operations layer. The dashboard is where the business sees work instead of only chat messages.

## 0:35 — Submit a Request

Use the automation example or type:

```text
We need an AI receptionist and dashboard that can receive customer requests, route them to the right person, and send WhatsApp/email updates.
```

Click:

```text
Send to Hunter Foreman
```

Explain:

The request is classified, converted into a task, assigned a workflow, and displayed with confidence, owner, escalation status, and notification previews.

## 1:10 — Show App Bridge Status

Point to the bridge section.

Explain:

If no receiver is configured, Foreman stays in local-only demo mode. In connected mode, it dispatches the task to an external application.

## 1:30 — Start Connected Demo

Open the connected receiver app:

```text
http://localhost:3100
```

Explain:

This second app proves Foreman is not just rendering a dashboard. It can send structured work to another application using a versioned contract.

## 1:55 — Submit Another Request

Return to the main app and submit another request.

Show:

- receiver acknowledgement
- receiver event ID
- live state ladder
- detailed timeline

## 2:25 — Show Receiver App

Return to the receiver app.

Show:

- live receiver stats
- received task
- timeline
- raw contract payload under details

Explain:

The receiver app accepts the task event, stores it in memory for the demo, and shows that the app bridge contract works.

## 2:50 — Closing

Hunter Foreman turns AI from a response into operational movement. The public version is safe and intentionally limited, but the architecture can later connect Events, Sales, Support, Payments, and other business systems.

## Final Line

This is not just a chatbot. It is an AI operations layer that helps a business receive, route, track, and own work.
