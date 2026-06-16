# Helpdesk Home Lab - Active Directory Account Troubleshooting & GPO (Windows Server 2022)


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
Open Active Directory Users and Computers on the Windows Server 2022 VM, locate the user account, and disable the account:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/1.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 2 – Test User Login</b><br/><br/>
Attempt to log in to the Windows 11 workstation using the disabled domain account and verify access is denied. Make sure to sign out before testing to ensure that the test is valid:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/2.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 3 – Sign in as Local Administrator</b><br/><br/>
Log in using a local administrator account to perform troubleshooting tasks on the workstation:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/3.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 4 – Remove the User Profile</b><br/><br/>
Open System Properties, navigate to User Profiles, and delete the user's profile from the workstation. This simulates the same problem as a disabled user account:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/4.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 5 – Verify Account Restrictions</b><br/><br/>
Attempt to sign in again with the deleted account and confirm the account cannot authenticate:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/5.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 6 – Configure Login Hours</b><br/><br/>
Re-enable the user account and modify the user's Logon Hours settings and test login restrictions during unauthorized times:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/6.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 7 – Configure Account Expiration</b><br/><br/>
Set an expiration date for the user account and verify the account expiration error message:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/7.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 8 – Open Group Policy Management</b><br/><br/>
Launch Group Policy Management and open the Default Domain Policy for editing:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/8.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 9 – Configure Password Policies</b><br/><br/>
Set password expiration requirements, minimum password age, and password history settings:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/9.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 10 – Configure Account Lockout Policies</b><br/><br/>
Set the account lockout threshold, lockout duration, and reset counter values:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/10.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 11 – Enforce Group Policy</b><br/><br/>
Apply and enforce the updated Group Policy settings for the domain:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/11.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 12 – Verify Domain Policies</b><br/><br/>
Use the NET USER and GPRESULT commands to verify password and account policies:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/12.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 13 – Test Account Lockout</b><br/><br/>
Enter incorrect credentials multiple times to trigger an account lockout:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/13.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 14 – Unlock the User Account</b><br/><br/>
Open Active Directory Users and Computers and unlock the affected user account:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/14.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/><br/>
<b>Step 15 – Confirm User Access</b><br/><br/>
Verify the user can successfully log in after the account has been unlocked:<br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Active-Directory-Account-Troubleshooting-GPO-Windows-Server-2022-/blob/main/15.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
</p>


