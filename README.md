# Hunter Foreman Submission Pack

Judge-facing documentation, pitch material, demo scripts, proof material, and architecture notes for the Hunter Foreman hackathon submission.

## Repositories

- Core app: `jaydumisuni/hunter-foreman`
- Demo receiver: `jaydumisuni/hunter-foreman-demo`
- Submission pack: `jaydumisuni/hunter-foreman-docs`

See `cross-repo-index.md` and `proof/repo-coverage-matrix.md` for the three-repo map and coverage status.

## What This Repo Contains

```text
pitch/              Short and long pitch material
submission/         Hackathon submission text, judge walkthrough, and checklist
demo/               Demo script, run flow, and judge walkthrough
architecture/       Product, system, and app-bridge contract notes
assets/             Screenshot and video placeholders
qa/                 Judge questions and concise answers
proof/              Clean-clone, repo coverage, and judge-readiness proof
roadmap.md          Public roadmap
public-safety.md    Public/private boundary
```

## Core Story

Hunter Foreman is an AI operations foreman for small businesses.

ROSE receives customer requests. Foreman understands the request, creates the task, routes the work, updates the dashboard, dispatches to connected apps, receives acknowledgement, and shows the work state through a live dashboard.

The public hackathon version is intentionally safe. It does not expose private Hunter internals, production credentials, private prompts, client data, or device repair/recovery modules.

## Fast Review Path

1. Read `pitch/one-minute-pitch.md`.
2. Read `submission/final-submission-draft.md`.
3. Read `architecture/system-overview.md`.
4. Read `architecture/app-bridge-contract.md`.
5. Run the demo using `demo/run-guide.md`.
6. Present the demo using `demo/three-minute-demo-script.md`.
7. Prove all repos using `proof/repo-coverage-matrix.md` and `proof/clean-clone-checklist.md`.
8. Use `submission/judge-walkthrough.md`, `submission/checklist.md`, and `qa/judge-faq.md` before final submission.

## Submission Positioning

- AI Infra Summit angle: `submission/ai-infra-summit-positioning.md`
- TechEx business angle: `submission/techex-business-positioning.md`

Same platform, different emphasis.

## Submission Status

The three public repositories are now in proof/review phase before screenshots, demo recording, and final submission packaging.
