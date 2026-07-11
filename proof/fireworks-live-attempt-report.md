# Fireworks Live Attempt Report — Historical

> **Status:** Superseded by the successful Fireworks proof captured on July 9, 2026.
>
> Current evidence is stored in the core repository at `proof/fireworks-classification-proof.json`. It records successful classifications using `accounts/fireworks/models/gpt-oss-120b` with `provider: fireworks` and `fallbackUsed: false`.

This document is retained as historical evidence of an earlier blocked verification attempt and the system's fallback behavior. It must not be read as the current submission status.

## Purpose of the Earlier Attempt

The earlier test was performed to determine whether the submission could truthfully claim:

```text
Fireworks live integration verified with provider=fireworks and fallbackUsed=false.
```

At that time, Fireworks serverless inference was blocked by account status.

## Earlier Conclusion

```text
Fireworks provider path: implemented
Live verification script: merged
API key: present and recognized
Endpoint: reachable
Serverless model: valid
Live inference: blocked by Fireworks account status / billing suspension
Fallback behavior: verified working
```

## Tested Repository

```text
jaydumisuni/hunter-foreman
```

## Tested Script

```powershell
node scripts/test-fireworks-live.js
```

## Earlier Tested Model

```text
accounts/fireworks/models/llama4-maverick-instruct-basic
```

The earlier calls reached Fireworks but returned HTTP 412. Hunter Foreman correctly fell back to the deterministic classifier without crashing.

Observed earlier fallback behavior:

- `provider` returned as `rules`
- `fallbackUsed` returned as `true`
- intent remained valid
- confidence remained valid
- summary remained present

## Current Successful Proof

A later successful run was captured using:

```text
accounts/fireworks/models/gpt-oss-120b
```

Current verified evidence:

```text
provider=fireworks
fallbackUsed=false
```

Proof location:

```text
jaydumisuni/hunter-foreman/proof/fireworks-classification-proof.json
```

The earlier HTTP 412 attempt remains useful evidence that the fallback path behaves safely, but the final submission may now truthfully state that Fireworks-backed classification was successfully verified.