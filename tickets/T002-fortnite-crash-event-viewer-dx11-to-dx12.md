# Ticket ID: T002
## Title
Repeated Fortnite application crashes — identified DX11 instability via Event Viewer and mitigated by switching to DX12

## Role / Context
Provided end-user application troubleshooting and stability remediation on a single Windows endpoint.

## Environment
- OS: Windows 10/11
- Application: Fortnite (PC)
- Rendering API: DirectX 11 (before), DirectX 12 (after)
- Scope: Single device

## Impact
Frequent crashes prevented reliable gameplay and required immediate stability remediation.

## Symptoms
- Application crashes repeatedly during a single session over a short period

## Investigation / Diagnosis
1) Reviewed crash entries in Windows Event Viewer (Application logs).
2) Correlated crash timing with Fortnite running under DirectX 11.
3) Confirmed Fortnite rendering mode was set to DirectX 11.

## Resolution
1) Changed Fortnite rendering mode from DirectX 11 to DirectX 12.
2) Retested for stability during a follow-up session.

## Verification
- No crashes observed during the post-change retest session.

## Root Cause (likely)
DirectX 11 instability/compatibility on the endpoint (driver/game configuration).

## Documentation / Prevention
- Maintain GPU drivers using vendor-recommended stable releases.
- If crashes recur: review Event Viewer entries, verify game files, and re-check rendering mode/settings.
