# Ticket ID: T003
## Title
Slow boot and heavy startup — reduced startup load and validated full shutdown behavior

## Role / Context
Provided endpoint performance remediation using a repeatable checklist across multiple Windows devices.

## Environment
- OS: Windows 10/11
- Scope: Multiple endpoints (repeatable approach)

## Impact
Slow startup reduced usability after power-on and increased time-to-productivity.

## Symptoms
- Slow boot/startup
- High background activity after login resulting in sluggish responsiveness

## Investigation / Diagnosis
1) Reviewed Task Manager to identify excessive startup load:
   - Multiple non-essential applications enabled at startup
2) Considered shutdown behavior:
   - Hybrid shutdown/Fast Startup may retain session state between shutdown cycles

## Resolution
1) Disabled non-essential startup applications:
   - Task Manager → Startup apps (kept required driver/security components)
2) Performed a full shutdown when needed to ensure a clean start:
   - Hold Shift while selecting Shut down
3) Rebooted and re-tested.

## Verification
- Boot/startup performance improved after changes
- Observed reduced startup entries enabled and lower background activity after login
- Post-login responsiveness improved

## Root Cause (likely)
Excessive auto-start applications and non-clean shutdown behavior contributing to high post-login background load and slow startup.

## Documentation / Prevention
- Periodically review startup items and remove unnecessary auto-start entries (launchers/updaters/overlays).
- Use a full shutdown when troubleshooting persistent slow startup symptoms.

## Follow-up (if issue persists)
- If storage is HDD-limited, recommend SSD migration and RAM upgrade (see T004).
