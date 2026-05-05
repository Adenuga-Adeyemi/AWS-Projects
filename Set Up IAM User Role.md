# Setting Up IAM Users and Admin Access in AWS (Essential Security Step)
<img width="867" height="441" alt="image" src="https://github.com/user-attachments/assets/17ef6521-c670-46c5-8eb6-4048b56188cf" />


A detailed guide on how to create IAM users, assign permissions, enable Multi-Factor Authentication (MFA), and secure your AWS account using Identity and Access Management (IAM).

---

## Author

Adeyemi Adenuga

Medium Article:
https://medium.com/@adeyemi.da/setting-up-iam-users-and-admin-access-in-aws-essential-security-step-3d39c848f19b

LinkedIn:
https://www.linkedin.com/in/pearladeyemi

---

## Overview

Security is one of the most important aspects of working with Amazon Web Services (AWS). After creating an AWS account, the next critical step is to properly configure Identity and Access Management (IAM).

This guide explains how to:

- Understand AWS root user and IAM users  
- Create IAM users  
- Assign permissions using policies and groups  
- Enable Multi-Factor Authentication (MFA)  
- Secure account access  
- Set up billing alerts  

---

## Key Terminologies

### AWS (Amazon Web Services)
AWS is a cloud computing platform that provides computing power, storage, databases, networking, and other services on demand.

### Root User
The root user is the original account owner created during AWS sign-up. It has full administrative access to all resources and should only be used for critical tasks.

### IAM User
An IAM user is an identity created within AWS to grant access to specific people or applications. IAM users have controlled permissions.

### IAM Policy
An IAM policy is a JSON document that defines permissions. It specifies what actions a user or group can perform on AWS resources.

---

## Why IAM Users Are Important

Using the root user for daily tasks is a major security risk.

### Risks of Using Root User
- Full unrestricted access to all AWS services  
- High risk if credentials are compromised  
- Potential for unauthorized billing charges  
- No access control or restrictions  

### Benefits of IAM Users
- Follows the principle of least privilege  
- Allows role-based access control  
- Enables secure collaboration in teams  
- Improves accountability using AWS logs (CloudTrail)  
- Allows easy permission management and revocation  

---

## Methods of Assigning IAM Permissions

### 1. Add User to Group (Recommended)

This is the best practice for managing multiple users.

Steps:
- Create an IAM group (e.g., Administrators, Developers)  
- Attach policies to the group  
- Add users to the group  

Advantages:
- Easier permission management  
- Scalable for teams  
- Centralized control  

---

### 2. Attach Policies Directly to User

Permissions are assigned directly to a single user.

Advantages:
- Quick setup  
- Suitable for individual users  

Disadvantages:
- Harder to manage at scale  
- Less organized than groups  

---

## Step-by-Step: Creating an IAM User

### Step 1: Sign in to AWS Console

- Log in using your AWS account  
- Access the AWS Management Console dashboard  

---

### Step 2: Open IAM Service

- Search for IAM in the AWS services search bar  
- Open the IAM dashboard  

---

### Step 3: Enable Multi-Factor Authentication (MFA) for Root User

- Go to IAM dashboard  
- Click Security Recommendations  
- Select Add MFA  
<img width="828" height="369" alt="image" src="https://github.com/user-attachments/assets/40d19165-b2a2-4347-a3aa-c09930783ebe" />

<img width="828" height="433" alt="image" src="https://github.com/user-attachments/assets/0c327033-403e-434d-ab54-1e547fab4189" />

### MFA Setup Process:
- Enter device name  
- Select Authenticator App  
- Install Google Authenticator on your phone  
- Scan QR code  
- Enter two consecutive verification codes  

MFA adds an extra layer of security to your account.

---

### Step 4: Create IAM User

- Go to Users in IAM dashboard  
- Click Add Users  
- Enter username  
<img width="828" height="309" alt="image" src="https://github.com/user-attachments/assets/3740adb7-532d-4502-9b96-4dcbfbfd9ab9" />

Choose access type:
- AWS Management Console access  
<img width="828" height="398" alt="image" src="https://github.com/user-attachments/assets/d3394bb4-7d00-48e6-b097-17f1e6ac9612" />

Assign permissions:
- Add user to group (recommended), OR  
- Attach policies directly  


For admin access:
- Select AdministratorAccess policy  
<img width="828" height="355" alt="image" src="https://github.com/user-attachments/assets/e62a71ac-729f-47b0-aa3e-ce428faf7ad2" />
Create user and save credentials securely.

---

### Step 5: Configure IAM User Login

- Enable console access  
- Set a custom password  
- Optionally require password reset at first login  
- Download credentials securely  
<img width="828" height="517" alt="image" src="https://github.com/user-attachments/assets/15a19337-d83c-4bda-a0a3-c68aa4d64978" />

---

### Step 6: Set Account Alias

- Go to IAM dashboard  
- Create an account alias  
- This allows login using a custom name instead of Account ID  

---

### Step 7: Enable MFA for IAM User

- Select IAM user  
- Go to Security Credentials  
- Assign MFA device  
- Configure using authenticator app  

---

## Billing Alerts Setup

To avoid unexpected charges:

### Enable Billing Notifications

- Open Billing Dashboard  
- Go to Billing Preferences  
- Enable:
  - PDF invoices by email  
  - Free Tier usage alerts  
  - Billing alerts  
<img width="828" height="566" alt="image" src="https://github.com/user-attachments/assets/02334fae-d926-49ed-a3b7-9982ff27329f" />

- Add your email for notifications  

This helps monitor AWS usage and costs.

---

## Switching from Root User to IAM User

After setup:

- Sign out of root account  
- Sign in using IAM username  
- Use account alias instead of Account ID  
- Log in with IAM credentials  
<img width="828" height="473" alt="image" src="https://github.com/user-attachments/assets/ed8b5e30-e7d5-49b3-bb59-f7a5633560ff" />

---

## Best Practices for AWS Security

- Never use root user for daily operations  
- Always enable MFA  
- Use IAM roles and groups instead of individual permissions  
- Apply least privilege principle  
- Monitor activity using AWS CloudTrail  
- Set up billing alerts  

---

## Conclusion

Setting up IAM users is a critical step in securing your AWS environment. It ensures better access control, reduces risk, and follows industry best practices for cloud security.

By implementing IAM correctly, you build a strong foundation for safe and scalable cloud computing.

---

## Contact

For questions or support:

LinkedIn: https://www.linkedin.com/in/pearladeyemi  
Medium: https://medium.com/@adeyemi.da  

---
