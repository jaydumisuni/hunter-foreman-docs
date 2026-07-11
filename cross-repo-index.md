# Cross-Repository Index

Hunter Foreman is presented through three public-safe implementation and documentation repositories, with Sergeant as the supporting engineering reviewer.

## 1. Core App

Repository: [jaydumisuni/hunter-foreman](https://github.com/jaydumisuni/hunter-foreman)

Purpose:

- ROSE intake
- Fireworks AI classification with explicit fallback
- task creation and ownership
- operations dashboard
- App Bridge dispatch
- Docker startup
- CI checks
- public API and bridge contract documentation
- screenshots and reproducible proof artifacts

Use this repository to run and inspect the main demo.

## 2. Demo Receiver App

Repository: [jaydumisuni/hunter-foreman-demo](https://github.com/jaydumisuni/hunter-foreman-demo)

Purpose:

- accepts Foreman task events
- validates the versioned bridge contract
- displays received tasks
- displays the ROSE → Foreman → App Bridge timeline
- proves that the main application can dispatch work to another application

Use this repository to inspect the connected receiver and App Bridge boundary.

## 3. Submission Pack

Repository: [jaydumisuni/hunter-foreman-docs](https://github.com/jaydumisuni/hunter-foreman-docs)

Purpose:

- pitch material
- demo script
- judge FAQ
- final submission record
- architecture notes
- roadmap
- public safety boundary
- repository and proof checklists

Use this repository for the complete judge-facing explanation and cross-repository map.

## Supporting Review Layer

Repository: [jaydumisuni/Sergeant](https://github.com/jaydumisuni/Sergeant)

Sergeant is the independent implementation reviewer shaped and validated through Hunter Foreman. It supports claim-boundary discipline, evidence-based review, and proof-before-release engineering.

## Public Entry Points

- Main repository: https://github.com/jaydumisuni/hunter-foreman
- Public demo: https://hunter-foreman.thetechguyds.com
- Local/Docker application: http://localhost:3000

## Completion Status

The repositories have reached the submitted hackathon state. Review them together as one project: the core application, connected receiver, judge-facing documentation, and supporting review layer.