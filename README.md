# Entra ID (formerly Azure Active Directory) Identity & Access Management (IAM) Lab

## Overview

### Who:
This lab is designed for **cybersecurity professionals, cloud administrators, and IT security analysts** looking to gain hands-on experience in securing identities in **Entra ID (formerly Azure AD)**.

### What:
This lab will guide through configuring **RBAC (Role-Based Access Control)**, **Conditional Access Policies**, **Privileged Identity Management (PIM)**, and **Identity Protection** in **Entra ID** to enhance security and enforce least privilege access.

### When:
Implementing IAM best practices is crucial **before granting users access to cloud resources** to prevent **unauthorized access, account compromise, and privilege escalation attacks**.

### Where:
This lab will be performed within the **Microsoft Entra Portal**, using **Entra ID, Conditional Access, and Security Center** for identity governance and protection.

### Why:
Effective **Identity & Access Management (IAM)** is the **first line of defense** against cyber threats. **80% of breaches** are linked to weak or compromised credentials. This lab helps to:
- Secure user identities and enforce least privilege.
- Prevent unauthorized access using Conditional Access & MFA.
- Protect privileged accounts with just-in-time access.

---

## Lab Requirements
- **Microsoft Entra Subscription** (Free Trial or existing tenant).
- **Global Administrator** or **Security Administrator** role in Entra ID.
- A **test user account** to apply security policies.

---

## Lab Setup & Steps

### 1. Configure Role-Based Access Control (RBAC) for Least Privilege
#### Objective:
Restrict access using **Entra ID RBAC** to ensure users only have permissions needed for their job.

#### Steps:
1. Navigate to **Entra ID → Roles & Administrators**.
2. Assign the **"Reader"** role to a test user to allow read-only access.
3. Remove unnecessary **"Contributor" or "Owner"** roles from users who don’t need them.
4. Verify permissions using **Access Reviews** under **Identity Governance**.

📌 *Why?* Minimizing unnecessary permissions reduces the risk of **privilege escalation attacks**.

---

### 2. Implement Conditional Access & Multi-Factor Authentication (MFA)
#### Objective:
Enforce security policies like **blocking risky sign-ins and requiring MFA** for sensitive accounts.

#### Steps:
1. Go to **Entra ID → Security → Conditional Access**.
2. Create a **New Policy** → Name it **"Require MFA for Admins"**.
3. Select **Users → Assign to "Directory Roles" → Select "Global Administrators"**.
4. Set **Conditions → Locations → Block access from "Untrusted Countries"**.
5. In **Grant Controls**, select **Require Multi-Factor Authentication (MFA)**.
6. **Enable policy** and test it with the admin test account.

📌 *Why?* Conditional Access + MFA blocks **99.9% of identity-based attacks**.

---

### 3. Configure Privileged Identity Management (PIM) for Just-in-Time Access
#### Objective:
Protect **high-risk Entra ID roles** by requiring **time-based, on-demand access approvals**.

#### Steps:
1. Navigate to **Entra ID → Privileged Identity Management (PIM)**.
2. Click on **"Entra ID Roles" → Select "Global Administrator"**.
3. Set **"Require approval"** for Global Admin role activation.
4. Configure **"Time-bound access"** (e.g., allow access for 1 hour max).
5. Test by assigning **PIM-protected admin** role to a test user.

📌 *Why?* Attackers can’t exploit **always-on admin accounts** if privileged access is **time-restricted**.

---

### 4. Enable Identity Protection to Detect Compromised Accounts
#### Objective:
Use **Entra ID Identity Protection** to automatically detect and respond to **suspicious sign-ins**.

#### Steps:
1. Go to **Entra ID → Security → Identity Protection**.
2. Under **Risk Detection**, enable **"Risky Sign-ins" & "Leaked Credentials"**.
3. Create a policy:
   - **Assign to "All Users"**.
   - **Block access for High-Risk Users**.
   - **Require password change for Medium-Risk Users**.
4. Simulate a risky sign-in (e.g., log in from a different country).

📌 *Why?* Automatically detecting and blocking **compromised accounts** stops breaches before they escalate.

---

### 5. Secure Service Principals & Entra ID App Registrations
#### Objective:
Protect **Entra ID App Registrations & Service Principals** from abuse.

#### Steps:
1. Go to **Entra ID → App Registrations**.
2. Review **API Permissions** and remove unnecessary permissions.
3. Enable **"Admin Consent Required"** for third-party apps.
4. Block legacy authentication methods in **Entra ID → Security → Authentication Methods**.

📌 *Why?* Attackers often exploit **unmonitored service accounts** with excessive permissions.

---

## Testing & Validation
- **RBAC Test:** Try logging in with the test user and verify they only have **"Reader"** access.
- **Conditional Access Test:** Attempt to log in from an untrusted location and verify access is **blocked**.
- **PIM Test:** Try to activate **Global Admin** role and verify it requires **approval**.
- **Identity Protection Test:** Simulate a risky sign-in and confirm alerts are generated.

---

## Conclusion
### What Was Learned:
✔ Implement **Entra ID RBAC** for least privilege access.  
✔ Enforce **MFA & Conditional Access** to stop unauthorized logins.  
✔ Protect privileged roles using **PIM** for just-in-time access.  
✔ Detect and respond to **compromised accounts** with Identity Protection.  
✔ Secure **Entra ID App Registrations & Service Principals** from exploitation.

### Why This Lab Makes One Stand Out:
✅ Shows **real-world identity security expertise** (high-demand skill).  
✅ Demonstrates hands-on experience **securing Entra ID** (critical for cybersecurity jobs).  
✅ Prepares for **AZ-500 (Azure Security Engineer) & SC-300 (Identity & Access Administrator) exams**.

---

## Next Steps
🚀 **Advance IAM skills:**  
- Set up **Entra B2B & B2C** for external identity management.  
- Automate identity governance using **Entra ID Lifecycle Policies**.  
- Configure **SIEM integration** (Azure Sentinel) for **identity-related attack detection**.
