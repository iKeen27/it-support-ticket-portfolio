# Ticket Index (T001–T007)

Quick navigation to all documented cases.

## Connectivity / Drivers
- **T001 — No network after Windows install (Ethernet)**
  - Restore wired connectivity by installing the correct ASRock LAN/NIC driver and validating adapter status.
  - File: `tickets/T001-no-network-after-windows-install-nic-driver.md`

## Application Stability (Crash Triage)
- **T002 — Frequent Fortnite crashes (Event Viewer)**
  - Event Viewer triage to isolate DX11 instability; switched to DX12 and verified stability.
  - File: `tickets/T002-fortnite-crash-event-viewer-dx11-to-dx12.md`

## Boot / Startup Performance
- **T003 — Slow boot & heavy startup**
  - Reduced startup load by disabling non-essential startup apps and applying full shutdown when needed.
  - File: `tickets/T003-slow-boot-startup-apps-fast-startup-full-shutdown.md`

## Hardware Upgrade (Performance Remediation)
- **T004 — Legacy laptop performance upgrade (HDD → SSD + DDR3 SODIMM RAM)**
  - Identified storage/RAM bottlenecks and upgraded to SSD + increased DDR3 SODIMM memory for daily usability.
  - File: `tickets/T004-legacy-laptop-hdd-to-ssd-ddr3-sodimm-ram-upgrade.md`

## Endpoint Standardization / Performance Tuning
- **T005 — Endpoint standardization & performance tuning (remote)**
  - Standardized endpoint configuration and improved performance using built-in Windows settings (no third-party tools).
  - File: `tickets/T005-endpoint-standardization-performance-tuning-remote.md`

## Thermals (CPU)
- **T006 — CPU overheating under load (i5-12400F)**
  - Diagnosed sustained high temps; replaced stock cooler/thermal paste, cleaned system, and confirmed improvement under stress test.
  - File: `tickets/T006-cpu-overheating-i5-12400f-stock-cooler-repaste-and-aircooler-upgrade.md`

## Fan Noise (UEFI/BIOS)
- **T007 — MSI UEFI chassis fan curve tuning (guided remote)**
  - Guided users through UEFI fan-curve correction to reduce excessive chassis fan noise under load while maintaining safe thermals.
  - File: `tickets/T007-msi-uefi-chassis-fan-curve-guided-remote.md`
