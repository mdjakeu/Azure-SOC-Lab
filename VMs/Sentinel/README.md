# Microsoft Sentinel – SIEM Deployment & Threat Detection

Overview
This section documents the deployment and configuration of Microsoft Sentinel as the Security Information and Event Management (SIEM) solution within the Azure SOC Lab.

Microsoft Sentinel was configured to collect logs, create analytic rules, detect suspicious activity, and support incident response aligned with NIST 800-61.

---

Objectives

- Deploy Microsoft Sentinel
- Configure Log Analytics Workspace
- Connect data sources
- Create custom detection rules using KQL
- Generate and investigate security incidents
- Perform incident response workflow

---

## Environment Setup

### 1️⃣ Log Analytics Workspace
- Created a Log Analytics Workspace within the SOC Resource Group
- Configured for centralized log collection

### 2️⃣ Microsoft Sentinel Deployment
- Enabled Sentinel on the Log Analytics Workspace
- Configured SIEM dashboard and monitoring workspace

---

## 🔌 Data Connectors Enabled

The following data connectors were configured:

- Azure Activity Logs
- Security Events (Windows VM)
- Microsoft Defender for Cloud
- Azure AD Sign-in Logs
- Diagnostic Settings for Storage / Key Vault (if applicable)

These connectors allowed centralized ingestion of security logs across the environment.

---

## 🔎 Custom Detection Rules

Custom analytic rules were created to detect suspicious behavior.
Example
SecurityEvent
| order by TimeGenerated
| where EventID == 4625

