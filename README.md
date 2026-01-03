# IT Support Ticket Portfolio (Windows Endpoints)

Sanitized, ticket-style case notes documenting real Windows 10/11 endpoint incidents and repeatable fixes.  
No client-identifiable information is included.

## What this repository demonstrates
- Structured incident documentation (symptoms → impact → scope)
- Evidence-driven troubleshooting (tools + measurable findings)
- Root cause analysis (primary + contributing factors)
- Remediation with verification and prevention steps
- Practical Windows support workflows (drivers, performance, stability, thermals, UEFI/BIOS)

## Coverage
- Post-OS install driver remediation (chipset / NIC / GPU)
- Performance and stability improvements (startup load, responsiveness)
- Crash triage using Event Viewer and corrective actions
- Thermal remediation (repaste, cooler upgrade) + validation under load
- Guided UEFI/BIOS changes (e.g., fan curve correction)

## Repository structure
- `INDEX.md` — ticket directory (quick navigation)
- `tickets/` — incident tickets (T001+)
- `templates/` — reusable ticket template (optional but recommended)

## Ticket format (standard)
Each ticket follows:  
**Impact → Environment → Symptoms → Investigation → Resolution → Verification → Root Cause → Prevention**

## Privacy & sanitization
Before publishing any ticket updates:
- Remove usernames, hostnames, emails, and account identifiers
- Remove serial numbers, unique IDs, and internal/private IPs
- Crop/redact screenshots and logs
- Avoid pasting full `C:\Users\<name>\...` paths (use generic paths)

## Quick start
1) Open `INDEX.md`
2) Pick a ticket and review the investigation + resolution + verification

## How to add a new ticket
1) Copy `templates/ticket-template.md` into `tickets/`
2) Name it `T###-short-title.md` (e.g., `T008-dpc-latency-audio-dropouts.md`)
3) Add one row to `INDEX.md`

## Notes
- Third-party tools are intentionally minimized; preference is built-in Windows tools and vendor-supported methods.
- Verification is required for every ticket (duration, metric, or reproduction test).

## Links
Repo:
https://github.com/iKeen27/it-support-ticket-portfolio

LinkedIn:
https://www.linkedin.com/in/mohammedalamoudi-it/
