# Cloud SOC Lab – Microsoft Sentinel Implementation in Azure

## Project Overview

This project demonstrates the deployment of a cloud-native Security Operations Center (SOC) using Microsoft Sentinel in Microsoft Azure.

The lab simulates a real-world security monitoring environment, including infrastructure deployment, log ingestion, detection engineering, and incident investigation.

---

## Architecture Components

- Azure Resource Group
- Virtual Network (VNet)
- Virtual Machine (Attack Simulation Target)
- Log Analytics Workspace
- Microsoft Sentinel (SIEM)
- Data Connectors
- Custom Analytics Rules
- Incident Investigation Workflow

---

## Implementation Steps

### 1. Resource Group Creation

A dedicated Resource Group was created to logically isolate all SOC-related components.

**Purpose:**
- Governance boundary
- Lifecycle management
- RBAC scoping
- Cost tracking

<img width="1370" height="784" alt="image" src="https://github.com/user-attachments/assets/8dedcbca-cefa-439e-b9dc-8dbbc2f6c6c4" />


---

### 2. Virtual Network Deployment

A Virtual Network (VNet) was deployed to simulate a production-like enterprise environment.

**Configuration:**
- Custom address space defined
- Subnet configuration prepared
- Designed to host monitored assets

**Security Relevance:**
- Enables controlled communication
- Supports traffic visibility
- Simulates realistic attack surface

<img width="735" height="355" alt="image" src="https://github.com/user-attachments/assets/f34f21ce-4f71-41d3-ad47-d88d0f38f2e0" />

---

### 3. Virtual Machine Deployment

A Virtual Machine was deployed inside the VNet to act as a monitored endpoint.

**Configuration:**
- Public IP assigned (for attack simulation)
- Security logging enabled
- Network interface attached to VNet

**Security Objective:**
The VM was intentionally exposed to generate:
- Failed login attempts
- Brute-force patterns
- Security event telemetry

<img width="468" height="321" alt="image" src="https://github.com/user-attachments/assets/fb01e431-cd4b-42d2-879e-739684ac8a94" />

---

### 4. Log Analytics Workspace

A Log Analytics Workspace was created as the centralized log repository.

**Function:**
- Stores security telemetry
- Enables KQL querying
- Backend requirement for Sentinel

<img width="468" height="388" alt="image" src="https://github.com/user-attachments/assets/57318c45-1455-468f-a28f-4ae52e47eb40" />

---

### 5. Microsoft Sentinel Enablement

Microsoft Sentinel was enabled on top of the Log Analytics Workspace.

**Capabilities Activated:**
- SIEM functionality
- Log correlation
- Incident generation
- Investigation tools

<img width="468" height="245" alt="image" src="https://github.com/user-attachments/assets/ebea8ab4-e8af-4b13-aca5-a6f3a7e74ef6" />


![Sentinel](images/05-sentinel.png)

---

### 6. Data Connectors Configuration

Data connectors were enabled to ingest telemetry into Sentinel.

**Integrated Sources:**
- Azure Activity Logs
- Security Events from the VM
- Infrastructure logs

**Impact:**
Provides full visibility across:
- Control plane
- Endpoint level events

<img width="468" height="245" alt="image" src="https://github.com/user-attachments/assets/a5405e73-42dd-4b2e-8d06-1f89dbb84a77" />

<img width="468" height="317" alt="image" src="https://github.com/user-attachments/assets/c050f2c6-e53b-44df-9ac9-619a3804e4b9" />

---

### 7. Log Analysis Using KQL

KQL queries were executed to validate ingestion and analyze suspicious activity.

**Analysis Performed:**
- Failed login attempts
- Source IP identification
- Event time correlation

**Value:**
- Verified ingestion pipeline integrity
- Confirmed detection feasibility

<img width="468" height="231" alt="image" src="https://github.com/user-attachments/assets/8b8bdee7-e6b9-4d05-a43a-059e6c34393d" />

<img width="468" height="254" alt="image" src="https://github.com/user-attachments/assets/f91c6068-6aaa-43d3-93a7-64e0aa18a770" />



---

### 8. Custom Analytics Rule Creation

Custom analytics rules were created to detect brute-force login patterns.

**Detection Logic:**
- Threshold-based rule
- Multiple failed logins within a time window
- Automatic incident generation

<img width="468" height="269" alt="image" src="https://github.com/user-attachments/assets/5c4ce0ec-c7ef-4d89-ab2e-c7f4ee1a4c2c" />



---

### 9. Incident Investigation

Generated incidents were analyzed using Sentinel’s investigation tools.

**Investigation Process:**
- Entity mapping review (IP, host, account)
- Timeline correlation
- Suspicious behavior validation

<img width="468" height="91" alt="image" src="https://github.com/user-attachments/assets/dc0af4e5-9e5f-4a92-9133-50d206eadf06" />
<img width="468" height="108" alt="image" src="https://github.com/user-attachments/assets/c7aeb884-b9c4-4c71-a01a-d3f402500dce" />


---

## Skills Demonstrated

- Azure Infrastructure Deployment
- Cloud Security Architecture
- SIEM Implementation
- Log Ingestion & Validation
- KQL Querying
- Detection Engineering
- Incident Investigation
- Threat Pattern Analysis


---

## Conclusion

This lab demonstrates the practical implementation of a cloud-native SOC using Microsoft Sentinel, covering infrastructure deployment, telemetry ingestion, detection logic creation, and incident investigation workflow.
<img width="468" height="264" alt="image" src="https://github.com/user-attachments/assets/f4ce5ac5-d90e-4e7e-8d0e-470bf570e02d" />


It reflects core Security Engineer responsibilities in a modern cloud environment.
