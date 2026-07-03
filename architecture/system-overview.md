# System Overview

```text
Customer
   |
   v
ROSE
AI Receptionist
   |
   v
Hunter Foreman
AI Operations Foreman
   |
   +--> Intent + confidence
   +--> Workflow selection
   +--> Task creation
   +--> Human escalation
   |
   v
Foreman Dashboard
   |
   v
App Bridge Contract
foreman.app.task.v1
   |
   v
Connected Receiver App
```

## Public Repositories

### `hunter-foreman`

Main public demo app. It contains ROSE intake, Foreman routing, task creation, dashboard, notification previews, app bridge dispatch, Docker support, and CI.

### `hunter-foreman-demo`

External receiver app. It accepts the versioned bridge contract, displays received tasks, and shows the timeline.

### `hunter-foreman-docs`

Judge-facing submission pack. It contains pitch material, demo scripts, architecture notes, and judge questions.

## Public / Private Boundary

The public demo includes only safe routing, task, bridge, and presentation logic.

The private Hunter ecosystem remains separate. Private prompts, production credentials, client data, device repair/recovery modules, and internal business logic are not included.
