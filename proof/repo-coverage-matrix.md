# Repository Coverage Matrix

This matrix tracks what each repository must prove before the hackathon submission is considered covered.

## Coverage Status

| Repository | Purpose | Required Proof | Status |
|---|---|---|---|
| `hunter-foreman` | Main app and Foreman core | ROSE intake, routing, task creation, dashboard, app bridge status, local-only fallback, connected dispatch, CI, Fireworks live test script | Covered; live Fireworks proof still requires owner key run if claiming verified live |
| `hunter-foreman-demo` | External receiver app | Receives contract payload, validates task ID, shows live stats, shows received tasks, returns acknowledgement | Covered; latest receiver PR merged |
| `hunter-foreman-docs` | Submission pack | Pitch, architecture, demo script, judge FAQ, public safety, clean-clone proof, final submission draft, dual hackathon positioning | Covered; final proof/status lock in progress |
| `Sergeant` | Supporting reviewer/proof layer | Claim-boundary review, submission proof docs, docs proof tests, CI/Main Review proof | Covered; merged to main as support infrastructure |

## Repo 1 — `hunter-foreman`

Must prove:

- app starts locally
- Docker build works
- ROSE intake form works
- examples work
- task creation works
- dashboard updates
- bridge status is visible
- receiver acknowledgement appears in connected mode
- failure does not crash app
- CI passes
- Fireworks live verification script exists and is safe to run with env-only key

Current proof boundary:

```text
Fireworks provider path is implemented and live verification script is merged.
Verified live Fireworks output requires running scripts/test-fireworks-live.js with a real FIREWORKS_API_KEY outside GitHub.
```

## Repo 2 — `hunter-foreman-demo`

Must prove:

- receiver starts locally
- `/health` returns JSON
- `/foreman/tasks` accepts valid payloads
- invalid payloads are rejected
- receiver stats update
- timeline is visible
- raw payload is inspectable
- CI passes

## Repo 3 — `hunter-foreman-docs`

Must prove:

- judges know what to read first
- demo can be followed without private context
- architecture is clear
- bridge contract is documented
- public/private boundary is explicit
- submission text exists
- screenshot/video checklist exists
- clean-clone proof exists
- AI/AMD/Fireworks claim boundary is explicit

## Supporting Repo — `Sergeant`

Must prove:

- reviewer/proof role is clear
- docs distinguish proven, implemented, and pending proof
- secret/claim-boundary wording remains honest
- CI and Main Review pass
- docs proof tests protect the claim boundary

## Final Rule

A repository is not considered covered just because files exist. It is covered only when a judge can understand its role, run or review its part, and connect it to the full Hunter Foreman story.
