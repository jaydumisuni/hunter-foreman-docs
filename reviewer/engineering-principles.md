# Reviewer Engineering Principles

These principles define how Hunter Foreman and future THETECHGUY reviewer tools should evaluate code, documentation, and submissions before runtime proof.

## Core Lesson

Runtime proof should confirm engineering confidence, not replace it.

A system should not be run merely to discover whether the design is sound. It should be reviewed until the expected behavior is clear. If execution fails after that, the failure should be surprising and useful.

## 1. Finish, Then Prove

Do not clean-clone or record proof too early.

Correct order:

```text
Finish intended implementation
   ↓
Review claims against code
   ↓
Fix gaps
   ↓
Freeze repositories
   ↓
Run clean-clone proof
   ↓
Capture screenshots and demo video
   ↓
Submit
```

A proof only has value when the thing being proved is not still changing.

## 2. Claims Must Match Implementation

Every public claim must be checked against the code.

Examples:

- If docs say "AI reasoning," reviewer must verify there is an actual reasoning or inference layer.
- If docs say "AMD platform use," reviewer must verify real AMD infrastructure use or clearly mark it as planned.
- If docs say "containerized," reviewer must verify Docker files and run instructions exist.
- If docs say "connected app," reviewer must verify a bridge contract and receiver path exist.

If docs and code disagree, the reviewer must flag the mismatch before runtime testing.

## 3. Evidence Before Conclusions

A reviewer must prefer live evidence over cached summaries.

Evidence hierarchy:

1. Git tree / fresh clone
2. Raw repository files
3. GitHub contents API
4. CI logs
5. Pull request diff
6. Cached search or summaries

If sources conflict, the reviewer must report an evidence conflict instead of choosing the convenient answer.

## 4. Static Review Before Runtime Proof

Runtime proof should not be the first time important issues are found.

Static review should answer:

- What does the code actually do?
- What do the docs claim it does?
- Are those claims true?
- Are fallbacks honest?
- Are security and public/private boundaries clear?
- Are external dependencies real, optional, or planned?

## 5. Fallbacks Must Be Honest

Fallbacks are good engineering when they are clearly named.

Acceptable:

```text
AI_PROVIDER=fireworks uses real inference.
AI_PROVIDER=mock uses deterministic rule-based routing for local demos.
If provider fails, fallback routing keeps the app usable.
```

Not acceptable:

```text
Docs claim AI reasoning while the implementation only uses regex and heuristic scoring.
```

## 6. Bugs After Review Should Become Polish

When the architecture is understood and claims match code, most issues found during proof should be refinements:

- clearer errors
- better empty states
- better instructions
- edge-case handling
- stronger validation

A late issue should not reveal that the team misunderstood the core system.

## 7. Reviewer Must Preserve Trust

The reviewer should be willing to say:

- "I verified this."
- "I cannot verify this."
- "Evidence conflicts."
- "The code does not support this claim."
- "This is planned, not implemented."

Trust is more important than sounding confident.

## 8. Hunter Foreman Specific Lesson

The Foreman decision layer must be reviewed carefully.

If the public submission presents Hunter Foreman as an AI operations layer, reviewer must inspect the actual decision point and confirm whether it is:

- rule-based
- mock-only
- provider-backed inference
- provider-backed with fallback

The submission should describe that state truthfully.

## Final Rule

Run code to prove what thoughtful review already made likely.

If it works, that should be expected.
If it fails, the failure should teach something specific enough to polish the system.
