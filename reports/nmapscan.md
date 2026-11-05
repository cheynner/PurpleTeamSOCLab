# Incident Report: Brute force attack

**Date:** 2026-11-01\
**Analyst:** Cheynne\
**Severity:** Medium

## Summary
A host operating from the untrusted network segment 10.0.99.0/24 with the IP 10.0.99.50, performed a brute force attack against the user "buddy", which is the Wazuh SIEM server located on the office network segment 10.0.10.0/24. No successful logins were detected from this IP. The account was not compromised, there were no successful logins recorded.

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

