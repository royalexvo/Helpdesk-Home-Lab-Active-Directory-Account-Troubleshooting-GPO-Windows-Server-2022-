# Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-


<h2>Description</h2>
This lab demonstrates common help desk tasks performed in an Active Directory environment. The goal of this lab is to practice user account troubleshooting, account lockout management, password policy configuration, and Group Policy administration within a Windows Server domain environment.

<br />In this setup, the following tasks were completed:

- <b>Opened Active Directory Users and Computers</b>
- <b>Disabled a domain user account</b>
- <b>Verified login failure for a disabled account</b>
- <b>Logged into a local administrator account</b>
- <b>Removed a user profile from a Windows 11 workstation</b>
- <b>Tested login restrictions for a disabled account</b>
- <b>Configured user login hour restrictions</b>
- <b>Tested account expiration settings</b>
- <b>Enabled and disabled user accounts</b>
- <b>Opened and modified the Default Domain Policy</b>
- <b>Configured password age requirements</b>
- <b>Configured account lockout policies</b>
- <b>Enforced Group Policy settings</b>
- <b>Verified password policies using Command Prompt</b>
- <b>Generated Group Policy results using GPRESULT</b>
- <b>Locked and unlocked a domain user account</b>
- <b>Tested account lockout behavior from a Windows 11 client</b>

<h2>Languages and Utilities Used</h2>

- <b>Active Directory Users and Computers (ADUC)</b>
- <b>Group Policy Management</b>
- <b>Command Prompt (CMD)</b>
- <b>GPRESULT</b>
- <b>NET USER</b>
- <b>Windows Server 2022</b>
- <b>Windows 11</b>

<h2>Environments Used </h2>

- <b>Domain Controller: Windows Server 2022</b>
- <b>Client Machine: Windows 11</b>
- <b>Active Directory Domain Environment</b>
- <b>Oracle VirtualBox</b>

<h2>Program walk-through:</h2>

<p align="center">
<b>Step 1 – Disable a Domain User Account</b><br/><br/>
Open Active Directory Users and Computers, locate the user account, and disable the account: <br/>
<img src="INSERT_STEP_1_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 2 – Test User Login</b><br/><br/>
Attempt to log in to the Windows 11 workstation using the disabled domain account and verify access is denied: <br/>
<img src="INSERT_STEP_2_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 3 – Sign in as Local Administrator</b><br/><br/>
Log in using a local administrator account to perform troubleshooting tasks on the workstation: <br/>
<img src="INSERT_STEP_3_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 4 – Remove the User Profile</b><br/><br/>
Open System Properties, navigate to User Profiles, and delete the user's profile from the workstation: <br/>
<img src="INSERT_STEP_4_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 5 – Verify Account Restrictions</b><br/><br/>
Attempt to sign in again with the disabled account and confirm the account cannot authenticate: <br/>
<img src="INSERT_STEP_5_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 6 – Configure Login Hours</b><br/><br/>
Modify the user's Logon Hours settings and test login restrictions during unauthorized times: <br/>
<img src="INSERT_STEP_6_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 7 – Configure Account Expiration</b><br/><br/>
Set an expiration date for the user account and verify the account expiration error message: <br/>
<img src="INSERT_STEP_7_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 8 – Open Group Policy Management</b><br/><br/>
Launch Group Policy Management and open the Default Domain Policy for editing: <br/>
<img src="INSERT_STEP_8_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 9 – Configure Password Policies</b><br/><br/>
Set password expiration requirements, minimum password age, and password history settings: <br/>
<img src="INSERT_STEP_9_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 10 – Configure Account Lockout Policies</b><br/><br/>
Set the account lockout threshold, lockout duration, and reset counter values: <br/>
<img src="INSERT_STEP_10_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 11 – Enforce Group Policy</b><br/><br/>
Apply and enforce the updated Group Policy settings for the domain: <br/>
<img src="INSERT_STEP_11_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 12 – Verify Domain Policies</b><br/><br/>
Use the NET USER and GPRESULT commands to verify password and account policies: <br/>
<img src="INSERT_STEP_12_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 13 – Test Account Lockout</b><br/><br/>
Enter incorrect credentials multiple times to trigger an account lockout: <br/>
<img src="INSERT_STEP_13_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 14 – Unlock the User Account</b><br/><br/>
Open Active Directory Users and Computers and unlock the affected user account: <br/>
<img src="INSERT_STEP_14_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>

<b>Step 15 – Confirm User Access</b><br/><br/>
Verify the user can successfully log in after the account has been unlocked: <br/>
<img src="INSERT_STEP_15_IMAGE_HERE" height="80%" width="80%" alt="Lab Steps"/>
<br/>
</p>
