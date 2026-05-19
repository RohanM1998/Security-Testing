# Detecting Phishing Activity using Splunk SIEM

## Overview
During SOC simulation, I analyzed firewall and email logs in Splunk and identified suspicious communication to a malicious domain after a phishing email interaction.

## Investigation
Correlated logs showed:
- Outbound traffic to suspicious domain
- Suspicious PowerShell activity

## Splunk Query
index=firewall_logs suspicious_domain

## MITRE ATT&CK
- Initial Access (Phishing)
- Command and Control

## Remediation
Blocked domain, isolated host, reset credentials.
