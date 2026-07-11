# Cross-Repository Index

Hunter Foreman is presented through three public-safe implementation and documentation repositories, with Sergeant as the supporting engineering reviewer.

## Operating Business Context

Hunter Foreman was built inside **THETECHGUY DIGITAL SOLUTIONS**, an operating business with real clients and production-facing business and Events platforms.

- Main business platform: https://thetechguyds.com
- Events platform: https://events.thetechguyds.com
- Public Hunter Foreman demo: https://hunter-foreman.thetechguyds.com

The hackathon implementation also served as a completion and verification path for capabilities intended for the main business. Work completed and proven in the public demo is considered implemented for the wider business architecture. What remains is rollout, private configuration, and safe connection to existing production systems.

The broader ecosystem already supports Events operations, invitations, QR access, payments, referrals, commissions, and private WhatsApp workflows. Those systems are not exposed through the public repositories or runtime.

## 1. Core App

Repository: [jaydumisuni/hunter-foreman](https://github.com/jaydumisuni/hunter-foreman)

Purpose:

- ROSE intake
- Fireworks AI classification with explicit fallback
- task creation and ownership
- operations dashboard
- analytics and system health
- App Bridge dispatch
- Docker startup
- CI checks
- public API and bridge contract documentation
- screenshots and reproducible proof artifacts
- verified implementation surface for wider business rollout

Use this repository to run and inspect the main demo and the completed public-safe Foreman implementation.

## 2. Demo Receiver App

Repository: [jaydumisuni/hunter-foreman-demo](https://github.com/jaydumisuni/hunter-foreman-demo)

Purpose:

- accepts Foreman task events
- validates the versioned bridge contract
- displays received tasks
- displays the ROSE → Foreman → App Bridge timeline
- proves that the main application can dispatch work to another application
- validates the receiver pattern intended for later private business rollout

Use this repository to inspect the connected receiver and App Bridge boundary.

## 3. Submission Pack

Repository: [jaydumisuni/hunter-foreman-docs](https://github.com/jaydumisuni/hunter-foreman-docs)

Purpose:

- pitch material
- demo script
- judge FAQ
- final submission record
- architecture notes
- roadmap and business-rollout boundary
- public safety boundary
- repository and proof checklists

Use this repository for the complete judge-facing explanation and cross-repository map.

## Supporting Review Layer

Repository: [jaydumisuni/Sergeant](https://github.com/jaydumisuni/Sergeant)

Sergeant is the independent implementation reviewer shaped and validated through Hunter Foreman. It supports claim-boundary discipline, evidence-based review, and proof-before-release engineering.

## Public Entry Points

- Main repository: https://github.com/jaydumisuni/hunter-foreman
- Public demo: https://hunter-foreman.thetechguyds.com
- Main business platform: https://thetechguyds.com
- Events platform: https://events.thetechguyds.com
- Local/Docker application: http://localhost:3000

## Completion Status

The public repositories have reached the submitted hackathon state. The core Foreman capabilities demonstrated and verified here are completed for the wider business architecture. Existing production systems remain private, while business rollout and approved connection work continue outside the public runtime.

Review the repositories together as one project: the core application, connected receiver, judge-facing documentation, and supporting review layer.