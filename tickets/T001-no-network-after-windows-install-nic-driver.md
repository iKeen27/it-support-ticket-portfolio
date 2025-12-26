# Ticket ID: T001
## Title
No network connectivity after Windows installation (Ethernet) — ASRock LAN/NIC driver missing

## Role / Context
Provided local endpoint support after OS installation to restore wired network connectivity.

## Environment
- OS: Windows 10/11
- Connection: Ethernet
- Motherboard: ASRock (model as applicable)
- Scope: Single endpoint (post-install)

## Impact
No network/internet access after OS installation, blocking updates and normal use.

## Symptoms
- Ethernet cable connected but no network access
- Wired connection unavailable / adapter not functioning

## Investigation / Diagnosis
1) Verified physical connectivity (cable/port).
2) Checked Device Manager:
   - LAN/NIC driver was missing or the adapter was not properly recognized post-install.

## Resolution
1) Downloaded the correct LAN/NIC driver from the official ASRock support page (motherboard model-specific).
2) Installed the driver and rebooted (as required).

## Verification
- Ethernet adapter recognized correctly in Device Manager
- Link established and network/internet access restored

## Root Cause (confirmed)
LAN/NIC driver not installed after Windows installation.

## Documentation / Prevention
- Keep motherboard LAN drivers available for post-install deployments
- After OS install, validate Device Manager for missing drivers (Network/Chipset) before handoff
