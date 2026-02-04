[README.md](https://github.com/user-attachments/files/25060683/README.md)
# Phishing Detection & Incident Response (SOC Case Study)

## Project Overview 

This project is performed by a Security Operations Center Analyst to simulate a real-world phishing attack. The attack involves fraudulent emails sent to the employees posing as IT Support to decieve clicking on the malicious link.

The SOC Analyst’s objective is to investigate the phishing activity in order to detect the attack, analyze related events, and respond appropriately to mitigate the threat.


## Tools and Skills Demonstrated

Phishing detection and analysis 
Log analysis (e-mail, proxy, authentication)
Splunk SPL for data correlation
IOC identification
Incident timeline documentation
Incident response documentation

## Project Structure

The project is organized to reflect a SOC investigation workflow, separating raw log data, detection logic, SIEM queries, and incident documentation.

phishing-detection-project/
├── data/
│   ├── auth_logs.csv
│   ├── email_logs.csv
│   └── proxy_logs.csv
├── detections/
│   ├── phishing_detection_logic.txt
│   └── splunk_queries.txt
├── incident-response/
|   ├── incident_report.md
|   ├── incident_timeline.md
└── README.md


### Directory Breakdown

- **data/**  
  Contains simulated raw log data used during the investigation, including email delivery logs, web proxy activity, and authentication events.

- **detections/**  
  Documents the detection method used by the SOC Analyst. This includes phishing detection logic and SIEM-style queries written in Splunk SPL to identify suspicious activity.

- **incident_timeline.md**  
  Provides a chronological reconstruction of the phishing incident, showing how events unfolded from initial email delivery to detection and response.

- **README.md**  
  Serves as the primary documentation for the project, explaining the investigation scope, detection approach, and outcomes.


## Detection & Analysis Summary
The phishing attack was initially detected by identifying multiple emails delivered from the same external sender domain with identical subject lines, indicating a potential phishing campaign. Email logs were analyzed to determine the scope of users targeted by the attack.

Following email delivery, web proxy logs were reviewed to identify users who interacted with the phishing email by clicking the embedded URL. This activity was correlated with authentication logs to detect abnormal login behavior occurring shortly after the phishing interaction.

Authentication logs revealed failed login attempts from an external IP address associated with users who clicked the phishing link. In one case, a successful login occurred after multiple failed attempts, suggesting a potential credential compromise.

## Response Actions & Mitigation
Upon detection of the phishing activity and associated authentication anomalies, immediate containment actions were initiated. Affected user accounts were identified and forced password resets were performed to prevent further unauthorized access.

The malicious domain associated with the phishing campaign was blocked at the email gateway to prevent additional phishing emails from reaching users. The phishing URL was also flagged to prevent further access attempts.

The incident was documented and escalated to the security team for visibility and tracking. Impacted users were notified and advised on phishing awareness and credential safety best practices.

These actions successfully mitigated the phishing attack, prevented further credential misuse, and reduced the likelihood of additional user compromise.
