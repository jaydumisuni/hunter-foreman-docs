# Judge Score Map

This page maps Hunter Foreman directly to the scoring areas judges are likely to care about during the AMD AI Developer Hackathon: Act II.

## Track positioning

Primary track:

```text
Track 3: Unicorn Track
```

Reason:

Hunter Foreman is a full AI application and product concept, not only a narrow model benchmark or captioning workflow. It uses AI infrastructure to turn customer requests into operational work across connected applications.

Secondary relevance:

```text
Track 1: Hybrid Token-Efficient Routing Agent
```

Reason:

Hunter Foreman includes provider/fallback routing and is architected around deciding when provider-backed inference is useful and when deterministic local routing is enough for safe, low-cost operation.

## Score mapping

| Judging area | Hunter Foreman answer | Evidence |
| --- | --- | --- |
| Creativity / Originality | AI operations foreman, not another chatbot. It moves requests into owned work. | ROSE -> Foreman -> Task -> Dashboard -> App Bridge -> Receiver |
| Completeness | Main app, receiver app, docs, proof workflows, Docker path, demo guide, final platform paste text. | `hunter-foreman`, `hunter-foreman-demo`, `hunter-foreman-docs` |
| Technical execution | Versioned app bridge, connected receiver acknowledgement, deterministic fallback, CI, Docker proof, public/private split. | Submission Proof workflow, Docker proof, app bridge contract, receiver demo |
| Use of AI / AI infrastructure | Fireworks-compatible provider path, deterministic fallback, live verification script, explicit account-status proof boundary. | `scripts/test-fireworks-live.js`, Fireworks attempt report, fallback proof |
| AMD / Fireworks platform use | Hackathon credits are available according to kickoff email; Fireworks provider path is implemented; live proof is pending account credit activation. | Fireworks attempt report; support ticket; no live-verified claim until rerun passes |
| Product / market potential | Small businesses need requests routed, owned, tracked, and escalated across channels and apps. | Dashboard, task lifecycle, app bridge, receiver app, public roadmap |
| Demo clarity | 3-minute flow from request to receiver acknowledgement. | `demo/final-recording-shot-list.md`, `demo/three-minute-demo-script.md` |
| Reproducibility | Public repos, safe docs, clean proof workflow, no secrets committed. | README, proof matrix, clean-clone checklist, Submission Proof |
| Safety / responsibility | Public version excludes private internals, credentials, private prompts, client data, payment secrets, and sensitive modules. | `public-safety.md`, final submission draft |
| Review maturity | Sergeant supports claim-boundary discipline and proof-before-claim review. | `jaydumisuni/Sergeant` |

## Judge-facing one-liner

```text
Hunter Foreman turns AI from a response into operational movement: intake, classification, task creation, dashboard state, app bridge dispatch, receiver acknowledgement, and human-visible ownership.
```

## What to emphasize in live judging

1. It is an operations layer, not a chatbot.
2. The connected receiver proves the workflow leaves the main app.
3. The fallback path proves resilience when provider inference is unavailable.
4. The public/private boundary proves responsible demo scoping.
5. The docs and proof workflows make the project reproducible.

## What not to overclaim

Do not claim live Fireworks verification yet.

Correct wording:

```text
Fireworks-compatible provider path implemented; live verification attempted; Fireworks account activation/credits blocked inference; fallback verified.
```

Upgrade only after a rerun shows:

```text
provider=fireworks
fallbackUsed=false
```

## Questions to listen for during kickoff

- How exactly do participants activate the $50 Fireworks AI API credits?
- How exactly do participants activate the $100 AMD Developer Cloud credits?
- Is Unicorn Track scored differently from Track 1 on AMD platform usage?
- Are proof links, CI output, or demo videos preferred in the final submission?
- Is fallback behavior acceptable evidence of production-minded reliability when provider access is unavailable?
