# Judge Walkthrough

## What To Review First

Start with the repositories in this order:

1. `hunter-foreman-docs`
2. `hunter-foreman`
3. `hunter-foreman-demo`

The docs repo explains the story. The core repo runs the main app. The demo repo proves the external app bridge.

## Fast Path

Read:

```text
README.md
pitch/one-minute-pitch.md
architecture/system-overview.md
architecture/app-bridge-contract.md
demo/three-minute-demo-script.md
proof/clean-clone-checklist.md
submission/final-submission-draft.md
```

Then run the connected demo.

## What The Demo Proves

The demo proves that Hunter Foreman can:

- receive a business request
- classify it into a workflow
- create a task
- show the task in a dashboard
- prepare customer updates
- dispatch the work to a connected app
- receive acknowledgement
- show state progression
- keep the public/private boundary clean

## What It Does Not Claim

This public version does not claim to be the full private Hunter ecosystem.

It does not include:

- production integrations
- payment provider secrets
- WhatsApp production credentials
- private Hunter prompts
- client data
- device service modules
- internal THETECHGUY automation

## Suggested Judge Test

1. Clone all three repos.
2. Run the main app only.
3. Submit a ROSE request.
4. Confirm local-only bridge state.
5. Run the connected demo.
6. Submit another request.
7. Confirm receiver acknowledgement.
8. Stop the receiver.
9. Submit another request.
10. Confirm the main app does not crash.

## Evaluation Frame

Evaluate Hunter Foreman as a business operations infrastructure layer.

The value is not only the UI. The value is the lifecycle:

```text
Request → routed work → visible dashboard → connected app → acknowledgement
```

## Strongest Point

The project shows that AI can be used as a coordinator of business work, not only as a conversational interface.
