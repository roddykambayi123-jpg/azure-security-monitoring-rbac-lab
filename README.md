# Azure Security Monitoring & RBAC Lab

This project demonstrates how to configure and test security controls in Microsoft Azure, focusing on Role-Based Access Control (RBAC), storage account security, Azure Monitor alerts, and remediation.

## Objectives
- Configure least-privilege access with Azure RBAC
- Simulate a misconfiguration (public blob access)
- Detect unauthorized changes with Azure Monitor alerts
- Remediate and validate secure storage configuration

## Steps

### Step 1 – Role Assignments
Using Azure CLI to assign Owner (admin.user), Contributor (dev.user), and Reader (aud.user) roles to different users in the resource group.

### Step 2 – User Onboarding
Setting up an admin.user account and forcing a password reset for first login.

### Step 3 – Developer User Access
dev.user logged in successfully and could view blobs in the storage container.

### Step 4 – Auditor Restrictions
aud.user tried to upload a blob but was denied — validating least-privilege RBAC.

### Step 5 – Configuring Alert Rules
Created an Azure Monitor alert for administrative changes to blob access which triggered 12 alerts from the public blob access being changed.

### Step 6 – Email Alert Triggered
Received an email notification when public blob access was attempted — showing that detection worked.

### Step 7 – Remediation Proof
Blob container access remained blocked for anonymous users, ensuring security.

## Screenshots include
- RBAC assignments
- Developer access to view the blobs
- Auditor denied the rights to upload a file
- Password reset from Admin account
- Alert email
- Alerts dashboard
- Remediation proof

## Key Takeaways
- RBAC enforces least-privilege access
- Azure Monitor provides real-time detection
- Misconfigurations can be detected, alerted, and remediated
- Documentation and evidence support portfolio use cases
