# Entra ID Identity & Access Management (IAM)

## Definition: Entra ID Identity & Access Management (IAM)
Microsoft Entra ID Identity & Access Management (IAM) is a cloud-based identity solution that enables organizations to securely manage user access to applications, devices, and data. It provides authentication, authorization, and governance capabilities, ensuring that only authorized users can access critical resources while maintaining compliance with security policies.

### Who:
This lab is designed for **cybersecurity professionals, cloud administrators, and IT security analysts** looking to gain hands-on experience in securing identities in **Entra ID (formerly Azure AD)**.

### What:
This lab will guide through configuring **RBAC (Role-Based Access Control)** to enhance security and enforce least privilege access.

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

**Click on the images below to view the full-size version**
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


## Conclusion

In this lab, the key principles of **Entra ID IAM** were explored. Azure Active Directory, Role-Based Access Control (RBAC), and Conditional Access policies were configured to manage and secure user access to Azure resources. These practices are essential for maintaining a secure cloud environment and ensuring that only authorized individuals can access sensitive resources.

