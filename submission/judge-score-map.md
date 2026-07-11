# Judge Score Map

This page maps Hunter Foreman directly to the scoring areas for the AMD Developer Hackathon: Act II.

## Track Positioning

Primary track:

```text
Track 3: Unicorn Track
```

Hunter Foreman is a full AI application and product concept, not a narrow benchmark or captioning workflow. It uses AI infrastructure to turn customer requests into operational work across connected applications.

## Score Mapping

| Judging area | Hunter Foreman answer | Evidence |
| --- | --- | --- |
| Creativity / Originality | AI operations foreman, not another chatbot. It moves requests into owned work. | ROSE → Foreman → Task → Dashboard → App Bridge → Receiver |
| Completeness | Main application, receiver application, docs, proof workflows, Docker path, public demo, screenshots, video, and final submission package. | `hunter-foreman`, `hunter-foreman-demo`, `hunter-foreman-docs` |
| Technical execution | Versioned App Bridge, connected receiver acknowledgement, deterministic fallback, CI, Docker proof, and public/private split. | Submission proof, Docker proof, App Bridge contract, receiver demo |
| Use of AI / AI infrastructure | Verified Fireworks classification, explicit fallback, confidence and escalation metadata, and observable provider state. | `proof/fireworks-classification-proof.json`, `scripts/test-fireworks-live.js` |
| AMD / Fireworks platform use | Fireworks-backed inference was successfully verified using `accounts/fireworks/models/gpt-oss-120b`. | Proof records `provider: fireworks` and `fallbackUsed: false` |
| Product / market potential | Small businesses need requests routed, owned, tracked, and escalated across channels and applications. | Dashboard, task lifecycle, App Bridge, receiver application, public roadmap |
| Demo clarity | Public judge-facing demo plus a complete request-to-receiver walkthrough. | `https://hunter-foreman.thetechguyds.com`, demo video, screenshots, scripts |
| Reproducibility | Public repositories, safe documentation, Docker support, proof package, and no committed secrets. | README, proof matrix, clean-clone checklist, submission proof |
| Safety / responsibility | Public version excludes private internals, credentials, private prompts, client data, payment secrets, and sensitive modules. | `public-safety.md`, final submission record |
| Review maturity | Sergeant supports claim-boundary discipline and proof-before-release review. | `jaydumisuni/Sergeant` |

## Judge-Facing One-Liner

```text
Hunter Foreman turns AI from a response into operational movement: intake, classification, task creation, dashboard state, App Bridge dispatch, receiver acknowledgement, and human-visible ownership.
```

## What to Emphasize

1. It is an operations layer, not a chatbot.
2. Fireworks AI performs verified semantic classification before Foreman creates owned work.
3. The connected receiver proves the workflow leaves the main application.
4. The fallback path proves resilience when provider inference is unavailable.
5. The public/private boundary proves responsible demo scoping.
6. The documentation and proof workflows make the project reproducible.

## Verified Claim Boundary

Safe current wording:

```text
Hunter Foreman includes a verified Fireworks-backed classification path using accounts/fireworks/models/gpt-oss-120b. The captured proof records provider=fireworks and fallbackUsed=false, while the deterministic fallback remains available for reproducible local and Docker demonstrations.
```

Do not overstate planned integrations such as production WhatsApp automation, payments, event management, invitations, QR access, multi-business deployment, or additional production receivers. Those remain explicitly identified as planned or not connected.

## Submission State

- Track: `Track 3 — Unicorn Track`
- Main repository: `https://github.com/jaydumisuni/hunter-foreman`
- Public demo: `https://hunter-foreman.thetechguyds.com`
- Submission: completed
