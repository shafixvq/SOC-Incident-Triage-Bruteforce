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

| Tactic        | Technique ID | Technique Name        | Description |
|--------------|--------------|-----------------------|-------------|
| Credential Access | T1110 | Brute Force | Repeated attempts to gain access to an account using multiple passwords |

MITRE ATT&CK was used to classify the observed behavior and align the incident with known adversary techniques.


## Findings
- Multiple failed login attempts were observed within a short timeframe
- The activity originated from a single external IP address
- The login pattern was consistent with brute force behavior
- No successful login was detected during the observation period

  
## Evidence
Screenshots in this repository demonstrate:
- Active endpoint monitored by SIEM
- Detection of failed authentication attempts
- Alert details including timestamps and event IDs


## Conclusion & Escalation
Based on the investigation, this incident was classified as a **True Positive**.
The alert met escalation criteria due to repeated unauthorized access attempts and was escalated to Level 2 SOC for further containment actions.


## Lessons Learned
- Importance of log correlation
- Early detection reduces impact
