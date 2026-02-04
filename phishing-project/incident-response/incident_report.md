# Incident Report: Phishing Attack Simulation

## Executive Summary
This report documents a simulated phishing incident analyzed from the perspective of a Security Operations Center (SOC) Analyst. The incident involved fraudulent emails impersonating IT Support, resulting in user interaction with a malicious link and subsequent authentication anomalies. The investigation focused on detecting the phishing campaign, correlating activity across multiple log sources, and responding to indicators of potential credential compromise.

## Incident Overview
The phishing campaign targeted multiple users using identical email subjects and a suspicious sender domain. Users who interacted with the phishing email were observed accessing a malicious URL, followed by abnormal authentication behavior originating from an external IP address.

## Scope and Impact
- Users impacted: Multiple employees
- Systems involved: Email gateway, web proxy, authentication service
- Risk level: High (potential credential compromise)

## Evidence Sources
- Email delivery logs
- Web proxy logs
- Authentication logs

## Incident Timeline
(See incident_timeline.md for the detailed chronological breakdown of events.)

## Detection and Analysis
Detection was achieved by identifying a phishing email campaign delivered to multiple users from the same sender domain. Proxy logs confirmed user interaction with the malicious URL. Authentication logs revealed failed login attempts from an external IP address following the phishing interaction, indicating possible credential misuse.

## Response and Mitigation
- Forced password resets for affected users
- Blocked the malicious domain at the email gateway
- Alerted the security team and documented the incident

## Lessons Learned and Recommendations
- Improve phishing awareness training
- Enhance email filtering rules
- Implement conditional access controls

