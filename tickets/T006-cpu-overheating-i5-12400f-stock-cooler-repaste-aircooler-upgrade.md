# Ticket ID: T006
## Title
CPU overheating under load (Intel i5-12400F) — identified inadequate stock cooling and degraded thermal paste; resolved with cooler upgrade and repaste

## Role / Context
Performed local hardware diagnostics and thermal remediation on a personal Windows desktop to restore safe operating temperatures under sustained load.

## Environment
- OS: Windows 11 Pro
- CPU: Intel Core i5-12400F
- Cooling (initial): Intel stock cooler
- Monitoring: Hardware monitoring tools (Core Temp, MSI Afterburner)
- Workload: High CPU load (gaming/rendering)

## Impact
CPU temperatures reached critical levels under load, risking thermal throttling, instability, and reduced component lifespan.

## Symptoms
- CPU temperature spikes to ~95°C under heavy workload
- Idle temperature ~60°C
- Light workload (web browsing) temperature ~70°C
- Other components appeared within normal ranges

## Investigation / Diagnosis
1) Verified temperature behavior using hardware monitoring tools.
2) Isolated the issue to CPU thermals (other components normal).
3) Performed physical inspection:
   - Thermal paste found degraded/hardened
   - Stock cooler assessed as insufficient for sustained high-load usage

## Mitigation (temporary)
1) Applied a temporary CPU undervolt within safe limits to reduce peak temperatures until a permanent cooling fix was implemented.
2) Reduced peak temperature to ~85°C as a short-term stability measure.

## Resolution
1) Replaced the stock CPU cooler with a higher-performance air cooler.
2) Cleaned old thermal compound and applied fresh thermal paste.
3) Cleaned dust and improved overall airflow.
4) Restored CPU voltage/settings to normal after the thermal fix.

## Verification
- CPU temperatures decreased significantly under load after cooler upgrade and repaste.
- Completed an extended CPU rendering stress test with stable temperatures and no thermal shutdowns.

## Root Cause (confirmed)
Inadequate cooling capacity (stock cooler) combined with degraded thermal paste causing elevated CPU temperatures under load.

## Documentation / Prevention
- Periodically inspect/replace thermal paste if temperatures drift upward over time.
- Use adequate cooling for sustained workloads and maintain case airflow (regular dust cleaning).
- Treat undervolting as a temporary mitigation; address cooling hardware for permanent resolution.
