# Ticket ID: T007
## Title
Excessive case fan noise under load — corrected MSI UEFI chassis fan curve via guided remote session

## Role / Context
Provided guided remote support (screen sharing) to assist users in adjusting MSI UEFI/BIOS fan control settings. Users accessed BIOS locally while I supervised and directed the changes step-by-step.

## Environment
- OS: Windows 10/11
- Motherboard/UEFI: MSI
- Scope: 3 endpoints
- Fans: Chassis/case fans

## Impact
Excessive fan noise during normal high-load usage impacted user experience and indicated suboptimal fan control configuration.

## Symptoms
- Chassis fans ramped to high RPM/noise during heavy workloads
- Fan behavior appeared overly aggressive relative to normal operating temperatures (user reported)

## Investigation / Diagnosis
1) Confirmed the issue was specific to chassis/case fans (not CPU/GPU fans).
2) Reviewed MSI UEFI hardware monitor / fan control configuration via shared screen guidance.
3) Identified an overly aggressive/misconfigured fan curve driving unnecessary high RPM under load.

## Resolution
1) Guided users to MSI UEFI fan control (Hardware Monitor / Fan Control).
2) Adjusted the chassis fan curve to more appropriate temperature-to-RPM points.
3) Verified correct control mode per fan type where applicable (PWM/DC).
4) Saved configuration and rebooted.

## Verification
- Fan noise reduced significantly during high-load usage.
- Normal operating temperatures maintained after reboot and during subsequent use.
- No recurring complaints reported over an extended period.

## Root Cause (confirmed)
Misconfigured MSI UEFI/BIOS chassis fan curve causing unnecessary high fan RPM under load.

## Documentation / Prevention
- Recommended documenting baseline fan curve settings for rollback.
- Re-check fan curves after BIOS updates or hardware changes.
- Ensure correct PWM/DC mode selection based on installed fan hardware.
