# PurpleTeamSOCLab
A VirtualBox lab simulation of an attack (Kali Linux) on an isolated network, with detection using a SIEM (Wazuh) and firewall (pfSense).

OVERVIEW
This lab simulates an office network monitored by a SIEM, an attempted an SSH brute force attack on the SIEM server, the building of the log pipeline, and the collection of the logs.

ARCHITECTURE
Host      Role                           Network Segment        IP                         Telemetry to SIEM   
----------------------------------------------------------------------------------------------------------------------------------------
pfSense   firewall/router                LAN, OPT1         10.0.10.1/24, 10.0.99.1/24      syslog (514)
DC01      domain controller (Windows)    LAN (Office)        10.0.10.10                    agent (1514)
WIN01     workstation (Windows 11)       LAN (Office)        DHCP                          agent (1514)
WAZUH     SIEM (Ubuntu Server)           LAN (Office)        10.0.10.20
KALI      attacker                       OPT1                10.0.99.50
