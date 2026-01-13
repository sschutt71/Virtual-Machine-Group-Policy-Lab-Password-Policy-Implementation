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
