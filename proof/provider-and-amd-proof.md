# Provider And AMD Proof Note

This note prevents the submission from overstating what has been verified.

## Current Implemented State

Hunter Foreman now has a real provider-backed classifier path in the public app.

```text
AI_PROVIDER=fireworks  -> provider-backed classification through Fireworks-compatible chat completions
AI_PROVIDER=mock/rules -> deterministic rule-based fallback for local demos
```

The app remains usable without secrets. When a provider key is missing or the provider fails, the classifier falls back to deterministic rules and records fallback metadata on the task.

## What Is Not Yet Claimed

Do not claim verified AMD infrastructure deployment until the proof run has actually been completed.

Accurate current wording:

```text
Hunter Foreman is containerized, includes a Fireworks-compatible provider path, and is ready for AMD-aligned provider proof.
```

Do not write:

```text
Hunter Foreman has already been deployed on AMD Developer Cloud.
Hunter Foreman already runs on ROCm.
Hunter Foreman already uses AMD infrastructure in production.
```

unless that proof has been captured.

## Proof Evidence To Capture

Before final AI Infra Summit submission, capture one of these:

1. Provider-backed classification run using the hackathon-supported Fireworks/AMD path.
2. Container run in an AMD-backed environment.
3. Clear note that AMD deployment is planned/pending if no verified runtime evidence is available.

## Evidence Checklist

- command used
- environment variables used, with keys redacted
- `/health` output showing provider mode
- `/api/app-bridge/status` output showing provider configured without exposing secrets
- screenshot of task classifier metadata
- short note explaining whether AMD use is verified or pending

## Reviewer Rule

The submission must describe the implementation truthfully.

If evidence is missing, mark the claim as pending. Do not convert planned infrastructure into completed infrastructure just because it sounds better.