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

![Resource Group](<img width="1370" height="784" alt="image" src="https://github.com/user-attachments/assets/ef5b1361-c287-46c0-8cca-2bedefa0406a" />
)

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

![VNet](images/02-vnet.png)

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

![Virtual Machine](images/03-vm.png)

---

### 4. Log Analytics Workspace

A Log Analytics Workspace was created as the centralized log repository.

**Function:**
- Stores security telemetry
- Enables KQL querying
- Backend requirement for Sentinel

![Log Analytics](images/04-log-analytics.png)

---

### 5. Microsoft Sentinel Enablement

Microsoft Sentinel was enabled on top of the Log Analytics Workspace.

**Capabilities Activated:**
- SIEM functionality
- Log correlation
- Incident generation
- Investigation tools

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

![Data Connectors](images/06-data-connectors.png)

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

![KQL Query](images/07-kql.png)

---

### 8. Custom Analytics Rule Creation

Custom analytics rules were created to detect brute-force login patterns.

**Detection Logic:**
- Threshold-based rule
- Multiple failed logins within a time window
- Automatic incident generation

![Analytics Rule](images/08-analytics-rule.png)

---

### 9. Incident Investigation

Generated incidents were analyzed using Sentinel’s investigation tools.

**Investigation Process:**
- Entity mapping review (IP, host, account)
- Timeline correlation
- Suspicious behavior validation

![Incident Investigation](images/09-incident.png)

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

It reflects core Security Engineer responsibilities in a modern cloud environment.
