# SOC Incident Triage – Brute Force Login Attack

## Overview
This project demonstrates Level 1 SOC alert triage and investigation of a brute force login attack using SIEM logs.

## Objective
- Identify suspicious login activity
- Investigate alert details
- Determine incident severity
- Decide escalation to L2 SOC

## Tools Used
- SIEM (Wazuh / Splunk)
- Windows Event Logs
- MITRE ATT&CK Framework

## Incident Description
Multiple failed login attempts were detected against a user account within a short time window, indicating a potential brute force attack.

## Investigation Steps
1. Reviewed authentication logs
2. Identified source IP and target user
3. Correlated event timestamps
4. Checked frequency and patterns

## MITRE ATT&CK Mapping
- T1110: Brute Force

## Findings
The activity showed repeated failed authentication attempts from a single external IP address.

## Conclusion & Escalation
This alert was classified as a **True Positive** and escalated to L2 SOC for further action.

## Lessons Learned
- Importance of log correlation
- Early detection reduces impact
