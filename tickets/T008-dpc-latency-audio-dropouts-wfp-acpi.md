# T008 — Intermittent Audio Dropouts (DPC Latency) — WFP Filter Driver + Power Management

## Category
Windows / Audio / Performance

## Priority
P2 — Real-time audio dropouts (clicks/cutting) and intermittent stutter affecting latency-sensitive usage.

## Environment (sanitized)
- **OS:** Windows 11
- **Connectivity:** Wi‑Fi/Ethernet present (sanitized)
- **Tools:** DPC Latency Checker (initial indicator), **LatencyMon** (driver attribution + metrics)
- **Notes:** User reported no intentional changes prior to onset.

## Reported Symptoms
- Sudden onset of audio clicks/dropouts (“sound cutting”).
- Issue persisted during normal usage.

## Impact / Scope
- **User impact:** Reduced audio reliability; degraded experience for real-time workloads (voice/media/gaming).
- **Scope:** Single endpoint.

## Investigation / Troubleshooting

### 1) Confirm the issue
- Initial measurement showed extreme latency spikes (tens of ms), consistent with DPC/ISR contention.
- Switched to **LatencyMon** to identify specific driver contributors.

### 2) Isolation tests
- Temporarily disabled network adapters and disconnected non-essential USB devices to reduce variables.
- Results indicated a system/driver-level cause rather than application-only.

### 3) Primary driver identified
- LatencyMon highlighted **`nfextlag.sys`** as the highest DPC contributor.
- `nfextlag.sys` is associated with third-party **NetFilter SDK / Windows Filtering Platform (WFP)** filtering, commonly installed by VPN/firewall/traffic-filtering products.

### 4) Remediation — disable the driver (immediate fix)
Executed in elevated Command Prompt:
```bat
sc query nfextlag
sc stop nfextlag
sc config nfextlag start= disabled
```
- Rebooted to ensure the driver does not reload.

### 5) Secondary contributor discovered
- Post-remediation monitoring still showed elevated activity attributed to **`ACPI.sys`** (power/firmware interaction).
- Applied OS power configuration changes to stabilize low-latency behavior.

## Root Cause
1) **Primary:** Third-party WFP network filter driver (`nfextlag.sys`) causing excessive DPC latency and audio dropouts.  
2) **Contributing:** Aggressive power management transitions contributing via `ACPI.sys`.

## Resolution
- Disabled the problematic WFP filter driver and prevented auto-start.
- Tuned Windows power settings for low-latency stability:
  - High Performance power plan
  - Processor minimum state: 100%
  - PCIe Link State Power Management: Off
  - USB selective suspend: Disabled
  - Disabled Fast Startup  
  *(Optional BIOS power-state tuning tested; details omitted/sanitized.)*

## Verification
- Ran LatencyMon for an extended session (~50+ minutes).
- Confirmed meaningful reduction in ISR/DPC latency and **no audio dropouts** during verification window.

## Prevention / Recommendations
- Avoid unnecessary “network accelerators” or kernel-level traffic filters on latency-sensitive systems.
- Prefer minimal-filter VPN/firewall solutions; validate latency impact post-install.
- Keep chipset drivers and BIOS on stable releases.
- Standardize power settings on endpoints intended for real-time workloads.

## Sanitization Notes
- Do not upload screenshots containing usernames, hostnames, serial numbers, internal IPs, or unique IDs.
