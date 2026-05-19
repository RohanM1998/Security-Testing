# Credential Dumping and Privilege Escalation in Active Directory Lab

## Overview
In an Active Directory lab environment, after gaining initial access using Metasploit, I executed Mimikatz to extract credentials from memory.

## Techniques Used
- Credential Dumping from LSASS
- Pass-the-Hash for lateral movement
- Privilege escalation

## Tools Used
- Metasploit
- Mimikatz

## MITRE ATT&CK
- Credential Access
- Lateral Movement

## Remediation
Disable WDigest, enforce Credential Guard, restrict admin privileges.
