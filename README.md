# Azure Security Monitoring & RBAC Lab
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](#)
![Azure](https://img.shields.io/badge/Cloud-Azure-blue)
![Security](https://img.shields.io/badge/Focus-Security%20%26%20RBAC-orange)

A hands-on mini-lab that:
- Applies least-privilege access with **Azure RBAC**
- Simulates an insecure change (**public blob access**)
- Detects it with **Azure Monitor alerts** (email + dashboard)
- Remediates by **disabling anonymous blob access** and verifies the block

## What you’ll see
- RBAC assignments at RG scope (Owner / Contributor / Reader)
- Admin first-login password update flow
- Developer can read blobs; Auditor is blocked from uploads
- Activity Log alert for public access change (12 events fired in test)
- Email notification and remediation proof (public access blocked)

---

## Steps Walkthrough

### Step 1 – Configure RBAC Assignments
Owner, Contributor, and Reader roles applied at the resource group (`rg-minilab`) scope.  
![RBAC role assignments](./screenshots/step1_0.png)

---

### Step 2 – Admin First Login
Admin account prompted to reset password on first sign-in.  
![Admin password reset](./screenshots/step2_0.png)

---

### Step 3 – Developer Access
Developer account (`dev.user`) accessing the blob container and successfully reading blobs.  
![Developer access view](./screenshots/step3_0.png)

---

### Step 4 – Auditor Restrictions
Auditor account (`aud.user`) attempting to upload a blob, blocked due to RBAC Reader role.  
![Auditor denied upload](./screenshots/step4_0.png)

---

### Step 5 – Azure Monitor Alerts Fired
Azure Monitor detects blob access configuration changes and triggers multiple alerts.  
![Azure Monitor alerts list](./screenshots/step5_0.png)

---

### Step 6 – Email Notification
Email received confirming the alert `Detect-Public-Blob-AccessChange` was activated.  
![Email notification](./screenshots/step6_0.png)

---

### Step 7 – Remediation Proof
Attempting to enable public access results in failure – proving that anonymous blob access is blocked.  
![Public access blocked](./screenshots/step7_0.png)

---

## Key Takeaways
- **Least privilege** enforced using RBAC roles.
- **Alert rules** detect sensitive configuration changes in real-time.
- **Email notifications** ensure visibility of incidents.
- **Remediation** (public access disabled) validated and proven.

---
