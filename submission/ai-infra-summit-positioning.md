# AI Infra Summit Positioning

## Submission Angle

Hunter Foreman is an AI operations infrastructure layer for small businesses.

The project demonstrates how customer requests can move through an AI receptionist, an operations foreman, a workflow engine, a versioned app bridge, and an external receiver application with visible acknowledgement and task state.

## Why It Fits AI Infrastructure

Hunter Foreman is not only a chatbot. It is infrastructure for coordinating AI-assisted work.

Key infrastructure pieces:

- ROSE intake layer
- provider-backed Foreman classification layer
- deterministic local fallback classifier
- task lifecycle layer
- app bridge contract
- external receiver integration
- live acknowledgement
- state ladder
- human escalation
- Docker local deployment
- public-safe repository split
- Sergeant supporting reviewer/proof layer

## AI Provider And Fallback Truth

The public app supports two classifier modes:

```text
AI_PROVIDER=fireworks  -> Fireworks OpenAI-compatible chat completions classification
AI_PROVIDER=mock/rules -> deterministic rule-based classifier for local demos and safe fallback
```

This keeps the demo reproducible without secrets while making the AI decision point real when a provider key is configured.

If the provider is missing, unsupported, or fails, Hunter Foreman keeps working through the deterministic fallback and marks the task with classifier metadata showing that fallback was used.

## Fireworks Proof State

The Fireworks provider path is implemented in the core app and the live verification script has been merged into `hunter-foreman`.

Accurate current claim:

```text
Fireworks provider path implemented; live verification script merged; live provider proof requires running scripts/test-fireworks-live.js with a real FIREWORKS_API_KEY outside GitHub.
```

Strong claim only after evidence:

```text
Fireworks live integration verified with classifier.provider=fireworks and fallbackUsed=false across multiple real requests.
```

Use the strong claim only if that live run output is captured.

## AMD / Fireworks Alignment

The AI Infra Summit judging criteria include meaningful AMD platform use. Hunter Foreman addresses that honestly in two stages:

1. **Implemented now:** the Foreman decision layer has a real provider-backed path through Fireworks-style OpenAI-compatible inference, plus local fallback for safe judging.
2. **Proof step before final submission:** run or document the provider-backed container configuration in an AMD-aligned environment or with the hackathon-supported Fireworks/AMD path, then record the evidence in `proof/clean-clone-checklist.md` and final submission notes.

The project should not claim verified AMD deployment until that proof run has been completed. Until then, the accurate claim is: **containerized app with implemented Fireworks provider path and AMD proof run pending.**

## Demo Story

```text
Customer request
   ↓
ROSE intake
   ↓
Foreman provider/fallback classification
   ↓
Task created
   ↓
App bridge contract
   ↓
Connected receiver app
   ↓
Acknowledgement and state update
   ↓
Dashboard visibility
```

## What Judges Should Notice

- The system is containerized and deployable locally.
- The classifier has a real provider-backed path, not only hardcoded routing.
- The fallback mode is explicit and visible in task metadata.
- The bridge uses a versioned contract.
- The receiver can be swapped for other business applications.
- The dashboard shows operational state, not only chat output.
- Human review is built into the workflow.
- Sergeant supports the proof-before-claim review discipline.
- The public project is scoped safely without private Hunter internals.

## Strongest Line

Hunter Foreman turns AI from a chat response into an operations layer that can move work between real applications.
