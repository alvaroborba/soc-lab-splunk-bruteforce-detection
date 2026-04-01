SOC Lab Splunk Brute Force Detection
Overview

This repository demonstrates a SOC lab using Windows Event Logs and Sysmon in Splunk. It includes simulated attacks, log ingestion, and detections for suspicious activity and potential account compromise. All activities were performed in a controlled lab environment for educational purposes.

Detection Scenarios
Brute Force Simulation: Multiple failed login attempts on SMB services using Hydra to generate authentication events.
SMB Share Enumeration: Listing SMB shares using smbclient to generate access logs.
Failed Login Detection: Identify repeated failed login attempts (EventCode 4625) to detect possible brute force attacks.
Successful Login Detection: Monitor successful logins (EventCode 4624) for correlation with failed attempts.
Process Monitoring via Sysmon: Track process creation events (EventCode 1) including user, executable, and command line.
Brute Force Followed by Successful Login: Detect multiple failed attempts followed by a successful login, indicating possible account compromise.
Evidence

Includes screenshots of queries executed in Splunk, showing results and patterns for analysis.

Notes

All simulations were done in a controlled lab. Queries demonstrate practical SOC detection techniques, including aggregation, thresholding, and process monitoring.

  - [**Architecture**](./Architecture) – Network and infrastructure diagrams.  
  - [**Attacks**](./Attacks) – Screenshots of simulated attacks and detected events.  
  - [**Dashboards**](./Dashboards) – Screenshots of Splunk dashboards.  
  - [**Alerts**](./Alerts) – Screenshots of configured alerts.  

All projects are for learning and portfolio purposes only. No sensitive data is included.
