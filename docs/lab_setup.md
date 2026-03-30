  Lab Setup

  Overview
This lab simulates a brute force attack in a small enterprise environment and demonstrates how it can be detected using Splunk.

Machines

  - Kali Linux (Attacker)
  - Used to perform brute force attacks using Hydra

  - Windows 10 (Target)
  - Victim machine where login attempts occur
  - Generates EventCode 4625 (failed logins)

  - Windows Server (Optional)
  - Simulates a corporate server environment

  - Ubuntu Server (Splunk SIEM)
  - Centralized log collection and analysis
  - Receives logs from endpoints

Tools Used

- Splunk (SIEM)
- Sysmon (Windows logging)
- Hydra (Brute force tool)
- Kali Linux

 Network Configuration

- Kali Linux: NAT (external attacker simulation)
- Windows machines: Internal Network
- Splunk Server: Internal Network

Data Flow

1. Attacker (Kali) performs brute force attack on Windows 10  
2. Windows generates security logs (EventCode 4625)  
3. Logs are forwarded to Splunk  
4. Splunk analyzes and detects suspicious activity  

Objective

- Simulate a real-world attack scenario  
- Detect brute force attempts using Splunk  
- Visualize and alert based on log data  
