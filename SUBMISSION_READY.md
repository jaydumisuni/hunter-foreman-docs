# Submission Readiness Checklist

Final freeze gate for Hunter Foreman before screenshots, demo recording, and final submission.

## Current Status

```text
Status: PRE-FREEZE REVIEW
Freeze state: not frozen yet
Runtime proof: pending
Screenshots: pending
Demo recording: pending
Final submission packaging: pending
```

## Repositories Covered

- [x] `jaydumisuni/hunter-foreman`
- [x] `jaydumisuni/hunter-foreman-demo`
- [x] `jaydumisuni/hunter-foreman-docs`

## Implementation Truth

- [x] Main app exists and is public-safe.
- [x] Receiver app exists and accepts the bridge contract.
- [x] Docs repo contains pitch, submission, demo, architecture, proof, QA, and reviewer material.
- [x] Provider-backed classification path exists.
- [x] Deterministic fallback remains available for local judging.
- [x] Task metadata shows classifier provider and fallback state.
- [x] No private runtime secrets are committed.

## Claim-To-Code Review

- [x] Docs no longer claim verified AMD deployment before proof.
- [x] AI Infra positioning says AMD proof is pending until evidence is captured.
- [x] Final submission draft describes provider/fallback classification truthfully.
- [x] Clean-clone checklist includes provider fallback and provider-backed proof.
- [x] Reviewer principles are saved in `reviewer/engineering-principles.md`.

## Review Status

- [x] `hunter-foreman` provider classifier PR merged.
- [x] `hunter-foreman` CI passed before merge.
- [x] CodeRabbit reported no actionable comments on provider classifier PR.
- [x] Docs AMD/provider alignment PR merged after manual claim-to-code review.
- [ ] CodeRabbit review for docs AMD/provider alignment if the review limit becomes available.
- [ ] Final owner review.

## Proof Still Required

- [ ] Fresh clone of all three repositories.
- [ ] Main app Docker run.
- [ ] Connected demo Docker run.
- [ ] API health checks.
- [ ] Provider fallback proof.
- [ ] Provider-backed proof with runtime credentials configured outside Git.
- [ ] AMD / Fireworks proof evidence or explicit pending note.
- [ ] Receiver failure-mode proof.
- [ ] Public safety check.

## Assets Still Required

- [ ] Main dashboard screenshot.
- [ ] ROSE intake screenshot.
- [ ] Classifier provider/fallback screenshot.
- [ ] Connected receiver acknowledgement screenshot.
- [ ] Failure-mode screenshot.
- [ ] Three-minute demo video.
- [ ] Final AI Infra Summit submission text.
- [ ] Final TechEx submission text.

## Freeze Rule

Do not mark the repositories frozen until:

1. No known claim-to-code mismatches remain.
2. No implementation changes are still planned for submission.
3. Clean-clone proof passes.
4. Provider/AMD wording matches the actual evidence captured.

## Final Sign-Off

```text
Repository freeze: pending
Clean-clone proof: pending
Demo assets: pending
Submission package: pending
Owner sign-off: pending
```

When every required item is checked, stop adding features and submit.
