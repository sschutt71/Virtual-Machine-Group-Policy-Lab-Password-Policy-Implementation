<img width="1394" height="865" alt="Password Policy Applied and Users" src="https://github.com/user-attachments/assets/3556a10e-4937-4f95-8937-bf8664366c9a" />
<img width="1381" height="858" alt="new GPO listed under Group Policy Objects" src="https://github.com/user-attachments/assets/ca5603d3-683b-4529-b263-dff491deab6c" />
<img width="1377" height="890" alt="Group Policy Management Screenshot" src="https://github.com/user-attachments/assets/f3e1a072-9df6-4a1a-84f3-2df608b9fec8" />
<img width="1384" height="887" alt="GPO_PasswordPolicy_AccountPolicies" src="https://github.com/user-attachments/assets/92a5beb1-12ed-4dd5-aa13-a100e9f7dfff" />
<img width="1207" height="841" alt="GPO Password Policies" src="https://github.com/user-attachments/assets/329c9c26-df53-45a2-bd09-5fcebebfaa85" />
<img width="1543" height="924" alt="booted the VM and reached the Windows 11 installer screen" src="https://github.com/user-attachments/assets/8ac38e85-2752-4038-9b86-9ef9794db50b" />
<img width="1196" height="915" alt="Active Directory Services Selected" src="https://github.com/user-attachments/assets/f47920b6-9afb-483d-a838-73b41ec6cc34" />
<img width="1401" height="879" alt="3 users added to Group" src="https://github.com/user-attachments/assets/42762bcf-5a5d-4b4d-8cd2-2e9d98e5e188" />
# Virtual-Machine-Group-Policy-Lab-Password-Policy-Implementation
Password Policy Implementation
Virtual Machine Group Policy Lab – Password Policy Implementation

Date: January 13, 2026
Author: Stanley Schutt

Overview

This lab demonstrates the creation and application of a Group Policy Object (GPO) for enforcing password policies on users in a Windows Active Directory environment. The lab was completed in VirtualBox using a domain controller setup.

The goal of this lab is to:

Create multiple users

Configure a password policy via a GPO

Apply the policy to a specific set of users

Test that the policy is enforced

Users Created
Full Name	Username
Kaya Williams	K. Williams
Valerie Pyer	V. Pyer
Sophia Shute	S. Shute

All three users were added to the security filtering of the GPO to ensure the policy applies only to them.

Group Policy Object (GPO)

GPO Name: New User Policy Test Lab

Password Policy Settings Configured:

Minimum Password Length: 8 characters

Password Must Meet Complexity Requirements: Enabled

Maximum Password Age: 60 days

Steps Performed

Create Users

Used Active Directory Users and Computers in VirtualBox.

Created the three users listed above.

Verified users exist in the appropriate Organizational Unit (OU).

Create GPO

Opened Group Policy Management Console.

Created a new GPO named New User Policy Test Lab.

Configure Password Policy

Expanded Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies → Password Policy.

Set the following:

Minimum password length = 8

Password complexity = Enabled

Maximum password age = 60 days

Took a screenshot of the configuration: GPO_PasswordPolicy_Settings.png

Link GPO and Apply to Users

Added the three users to Security Filtering under the GPO scope.

Verified GPO is linked to the OU where the users reside.

Screenshot of linking and users: GPO_LinkedToOU_SecurityFiltering.png

Test Password Policy Enforcement

Logged in as each user to verify enforcement.

Attempted password changes that violate policy (too short or simple).

Observed error messages confirming the policy is active.

Screenshot of enforcement: PasswordPolicy_Enforced_UserTest.png

Screenshots

GPO Password Policy Settings:
GPO_PasswordPolicy_Settings.png

GPO Linked to OU with Security Filtering:
GPO_LinkedToOU_SecurityFiltering.png

User Password Policy Enforcement:
PasswordPolicy_Enforced_UserTest.png
