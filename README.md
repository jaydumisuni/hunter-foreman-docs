# Hunter Foreman Submission Pack

Judge-facing documentation, pitch material, demo scripts, and architecture notes for the Hunter Foreman hackathon submission.

## Repositories

- Core app: `jaydumisuni/hunter-foreman`
- Demo receiver: `jaydumisuni/hunter-foreman-demo`
- Submission pack: `jaydumisuni/hunter-foreman-docs`

See `cross-repo-index.md` for the three-repo map.

## What This Repo Contains

```text
pitch/              Short and long pitch material
submission/         Hackathon submission text and checklist
demo/               Demo script, run flow, and judge walkthrough
architecture/       Product and system diagrams in text form
assets/             Screenshot and video placeholders
qa/                 Judge questions and concise answers
proof/              Clean-clone and judge-readiness proof checklist
roadmap.md          Public roadmap
public-safety.md    Public/private boundary
```

## Core Story

Hunter Foreman is an AI operations foreman for small businesses.

ROSE receives customer requests. Foreman understands the request, creates the task, routes the work, updates the dashboard, dispatches to connected apps, receives acknowledgement, and shows the work state through a live dashboard.

The public hackathon version is intentionally safe. It does not expose private Hunter internals, production credentials, private prompts, client data, or device repair/recovery modules.

## Fast Review Path

1. Read `pitch/one-minute-pitch.md`.
2. Read `architecture/system-overview.md`.
3. Run the demo using `demo/run-guide.md`.
4. Prove the demo using `proof/clean-clone-checklist.md`.
5. Use `submission/checklist.md` before final submission.
6. Use `qa/judge-faq.md` for judge/investor questions.

## Submission Positioning

- AI Infra Summit angle: `submission/ai-infra-summit-positioning.md`
- TechEx business angle: `submission/techex-business-positioning.md`

Same platform, different emphasis.

## Submission Status

The three public repositories are now in proof/review phase before screenshots, demo recording, and final submission packaging.
