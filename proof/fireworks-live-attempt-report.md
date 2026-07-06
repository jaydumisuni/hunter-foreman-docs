# Fireworks Live Attempt Report

This report records the final Fireworks live verification attempt for Hunter Foreman.

## Purpose

The goal was to determine whether the submission could truthfully claim:

```text
Fireworks live integration verified with provider=fireworks and fallbackUsed=false.
```

The result does not support that strongest claim yet because Fireworks serverless inference is blocked by account status.

## Current conclusion

```text
Fireworks provider path: implemented
Live verification script: merged
API key: present and recognized
Endpoint: reachable
Serverless model: valid
Live inference: blocked by Fireworks account status / billing suspension
Fallback behavior: verified working
```

## Tested repository

```text
jaydumisuni/hunter-foreman
```

## Tested script

```powershell
node scripts/test-fireworks-live.js
```

The script reads `FIREWORKS_API_KEY` from the environment, masks the key in output, calls the configured Fireworks OpenAI-compatible endpoint, and expects:

```text
provider=fireworks
fallbackUsed=false
```

## Tested models

Initial model attempts returned model-not-found or inaccessible responses.

The final serverless model tested was Fireworks' own documented serverless sample model:

```text
accounts/fireworks/models/llama4-maverick-instruct-basic
```

The model was set with:

```powershell
$env:FIREWORKS_MODEL="accounts/fireworks/models/llama4-maverick-instruct-basic"
```

## Result

All four live cases reached Fireworks but returned HTTP 412 from the provider.

The provider response indicated that the account is suspended, likely due to billing, spending-limit, free-credit, or payment-status handling.

Because the provider returned HTTP 412, Hunter Foreman correctly fell back to the deterministic rules classifier.

Observed behavior for each case:

- `provider` returned as `rules`
- `fallbackUsed` returned as `true`
- intent remained valid
- confidence remained valid
- summary remained present
- no crash occurred

## Evidence interpretation

This is not evidence that Fireworks live inference is verified.

It is evidence that:

- the API key is configured well enough for the request to reach Fireworks account handling
- the Fireworks endpoint is reachable from the local machine
- the selected serverless model is valid for the serverless path
- Hunter Foreman handles provider failure safely
- the fallback path remains operational and visible

## Support ticket status

A Fireworks support ticket should be filed or has been filed explaining that:

- the account was prompted to add a payment method to receive free credit
- a payment method was added
- free credit did not appear
- account balance remained at zero
- serverless API calls return HTTP 412 account suspended
- the account needs billing/credit activation before live verification can pass

## Submission-safe wording

Use this wording unless a later successful run is captured:

```text
Hunter Foreman includes an implemented Fireworks provider path and a merged live verification script. A real serverless Fireworks call was attempted using the documented serverless model `accounts/fireworks/models/llama4-maverick-instruct-basic`, but live inference was blocked by Fireworks account billing/suspension status. The system correctly fell back to its deterministic classifier, preserving valid intent, confidence, and summary output without crashing.
```

Do not claim:

```text
Fireworks live integration verified.
```

until the script returns:

```text
provider=fireworks
fallbackUsed=false
RESULT: 4/4 cases fully passed
```
