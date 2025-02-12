# SOC Automation Project

## Overview
This project focuses on automating endpoint monitoring for a Security Operations Center (SOC). The goal is to streamline threat detection and response by integrating various security tools. 

## Project Workflow
1. **Endpoint Monitoring**: Installed **Sysmon** on my laptop to collect detailed telemetry data.
2. **Log Forwarding**: Configured **Wazuh** to receive and analyze the logs from the endpoint.
3. **Alert Management**: Set up **TheHive** to manage security alerts and incidents.
4. **Automation**: Used **Shuffle** to automate the delivery of alerts from Wazuh to TheHive and send email notifications to users if an alert is triggered.

The following diagram illustrates the architecture and workflow:

![SOC Automation Diagram](image.png)

## Technologies Used
- **Sysmon** – Endpoint telemetry collection
- **Wazuh** – Security monitoring and log analysis
- **TheHive** – Security Incident Response Platform (SIRP)
- **Shuffle** – Security automation and orchestration tool

## How It Works
1. **Sysmon** collects logs from the laptop and sends them to **Wazuh**.
2. **Wazuh** analyzes logs and detects anomalies.
3. If a security alert is triggered, Wazuh forwards it to **Shuffle**.
4. **Shuffle** processes the alert, delivers it to **TheHive**, and sends an email notification to the user.
5. **TheHive** allows SOC analysts to investigate and manage incidents efficiently.

## Installation & Setup
### Prerequisites
- A laptop or endpoint with **Sysmon** installed
- A configured **Wazuh Manager**
- **TheHive** for incident management
- **Shuffle** for automation

### Steps
1. **Install Sysmon** on your endpoint and configure its rules.
2. **Set up Wazuh** to collect Sysmon logs and create alert rules.
3. **Deploy TheHive** to manage security alerts.
4. **Integrate Shuffle** to automate alert forwarding and email notifications.
5. **Test the setup** by generating logs and verifying the automation workflow.

## Future Improvements
- Enhancing detection rules for better threat intelligence.
- Integrating additional threat enrichment sources.
- Automating remediation actions for certain alerts.

## Author
Muhammad Shine
