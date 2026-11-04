# Incident Report: Internal Port Scan

**Date:** 2026-11-01
**Analyst:** Cheynne
**Severity:** Medium

## Summary
A host from the with the IP 10.0.99.50 performed a brute force attack

## Timeline
| Time | Event |
|------|-------|
| 20:42:32 | Burst of authentication failure alerts for user "buddy" |
| 20:42:38 | Final alert, 16 alerts within 6 seconds |

## Evidence
![pfSense firewall log](../images/bruteforcelogs.png)
![pfSense firewall log](../images/bruteforcelog.png)

## MITRE ATT&CK
- T1046 — Network Service Discovery

## Response / Recommendation
Contact user "buddy" to see if they attempted these logins. Check to see any if any successful logins occurred for this user, and if any alerts were created after a successful login.
