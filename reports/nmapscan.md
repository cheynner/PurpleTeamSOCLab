# Incident Report: Internal Port Scan

**Date:** 2026-11-03
**Analyst:** Cheynne
**Severity:** Low

## Summary
A host from the with the IP (10.0.99.50) performed a full TCP port
scan against the domain controller (10.0.10.10).

## Timeline
| Time | Event |
|------|-------|
| 20:01:12 | Burst of 6 blocked connections |

## Evidence
![pfSense firewall log](../images/nmap-firewall-log.png)

## MITRE ATT&CK
- T1046 — Network Service Discovery

## Response / Recommendation
Alert on one source contacting many ports in a short window;
consider a network IDS (Suricata) for scan detection.
