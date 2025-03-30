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
1. Navigate to **Entra ID → Users → Select a user → Assigned Roles → Add assignments → Directory Readers → Next → Assign**.
   
Click "Refresh" to ensure the role has been added to the user. The assignment will not be active yet after refreshing because it needs to be set to active. Navigate to "Eligible Assignments" and select "Update" under the Action category. Once activated, an explanation is required before finalizing the activation. Afterward, the assignment will appear under "Active Assignments."

![image](https://github.com/user-attachments/assets/d674c4bc-287a-4f93-9e55-29c2d2ab3ddd)
![image](https://github.com/user-attachments/assets/c3246afc-bb4d-404c-9e7a-1261dfe8bf79)
![image](https://github.com/user-attachments/assets/fc4438b5-2d57-47c8-92c5-ee1f7d193a0a)
![image](https://github.com/user-attachments/assets/cf960905-7996-4dac-b763-5b26cb267f53)
![image](https://github.com/user-attachments/assets/82619357-7105-4610-9c32-d65d56b9f359)
![image](https://github.com/user-attachments/assets/81bba641-834c-4456-b899-7ba6b9f2c82f)
![image](https://github.com/user-attachments/assets/b0161d61-c9d6-4f96-aebe-d6e76101f319)
![image](https://github.com/user-attachments/assets/6bb04aa2-176d-4a03-82f9-57cb4de85779)
![image](https://github.com/user-attachments/assets/ea96b7e9-2843-4588-b503-19a45ac640f2)
![image](https://github.com/user-attachments/assets/41fbb903-bb1c-4d64-b09e-119dea30034e)
![image](https://github.com/user-attachments/assets/e4a83f9f-8f12-40f3-8fee-254eadbb1ae7)
![image](https://github.com/user-attachments/assets/27dca87f-01b0-4042-ad33-b58b596800da)












*Why?* Minimizing unnecessary permissions reduces the risk of **privilege escalation attacks**.

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
