# Ticket ID: T004
## Title
Legacy laptop performance remediation — migrated HDD to SSD and upgraded DDR3 SODIMM RAM (4GB → 8GB)

## Role / Context
Performed hardware upgrade and post-upgrade validation to restore acceptable performance for daily use.

## Environment
- Device: Legacy laptop (Intel i5)
- OS: Windows 10/11
- Storage: HDD (before) → SSD (after)
- Memory: DDR3 SODIMM 4GB (before) → DDR3 SODIMM 8GB (after)

## Impact
Laptop performance was below acceptable baseline for daily tasks; upgrades restored usability and responsiveness.

## Symptoms
- Very slow boot
- Slow application launches and general system lag

## Investigation / Diagnosis
1) Identified HDD as a primary performance bottleneck (boot time and application load).
2) Confirmed low memory capacity contributed to slowdowns during multitasking.

## Resolution
1) Replaced HDD with SSD.
2) Upgraded system memory from DDR3 SODIMM 4GB to DDR3 SODIMM 8GB.
3) Booted the system and validated performance under common daily workloads.

## Verification
- System boot and application responsiveness improved post-upgrade.
- Validated normal operation and improved multitasking responsiveness after upgrade.
- Device returned to reliable daily-use performance.

## Root Cause (confirmed)
Performance constraints driven by mechanical HDD limitations and insufficient RAM capacity for the workload.

## Documentation / Prevention
- SSD migration is a high-impact upgrade for older systems with HDD storage.
- Ensure DDR3 SODIMM module compatibility (speed/voltage/form factor) before installation.
