# Incident Report: Internal Port Scan

**Date:** 2026-11-01
**Analyst:** Cheynne
**Severity:** Medium

## Summary
A host from the with the IP 10.0.99.50 performed a brute force attack

## Timeline
| Time | Event |
|------|-------|
| 20:01:11 | Burst of 16 blocked connections alerts |
| 20:01:50 | Final alert

## Evidence
![pfSense firewall log](../images/nmapscanlogs.png)
![pfSense firewall log](../images/nmapscanlog.png)

## MITRE ATT&CK
- T1046 — Network Service Discovery

## Response / Recommendation
Alert on one source contacting many ports in a short window;
consider a network IDS (Suricata) for scan detection.
