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
Step 1 – Download and Install Oracle VirtualBox<br/><br/>
Navigate to the Oracle VirtualBox website and download the latest version of VirtualBox (v7.2.6). Run the installer and follow the installation wizard to install VirtualBox on your host machine: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%201.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/>
Step 2 – Download Windows Server 2022 ISO<br/><br/>
Go to the Microsoft Evaluation Center and download the Windows Server 2022 ISO (64-bit). Save the ISO file to your system so it can be used to install the server operating system inside the virtual machine: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%20II.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br />
Step 3 – Download Windows 11 Installation Media<br/><br/>
Navigate to the Microsoft Windows 11 download page and download the Windows 11 Installation Media Creation Tool. Use the tool to create a Windows 11 ISO file which will later be used as a client machine in the lab environment: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%203.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br />
Step 4 – Create a New Virtual Machine<br/><br/>
Open Oracle VirtualBox and click “New” to create a new virtual machine. Name the virtual machine Server 2022 and select Microsoft Windows as the operating system type with Windows Server 2022 as the version: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%204.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br />
Step 5 – Allocate System Resources<br/><br/>
Configure the hardware settings for the virtual machine. Assign 8GB of RAM and 2 CPU cores to the virtual machine to ensure the server runs smoothly during installation and future lab exercises: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%205.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br />
Step 6 – Mount the Windows Server 2022 ISO<br/><br/>
Open the virtual machine settings and navigate to the Storage section. Attach the downloaded Windows Server 2022 ISO file to the virtual optical drive so the virtual machine can boot from it during installation: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%206.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br />
Step 7 – Start the Virtual Machine<br/><br/>
Start the virtual machine in VirtualBox. When prompted, select the Windows Server 2022 ISO file and allow the system to boot into the Windows Server installation setup: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%207.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/>
Step 8 – Install Windows Server 2022<br/><br/>
Follow the Windows installation prompts and select Windows Server 2022 (Desktop Experience) to install the version with the graphical user interface. Choose Custom Installation and proceed using the default disk configuration: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%208.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/>
Step 9 – Configure the Administrator Account<br/><br/>
After installation completes, the system will prompt you to set a password for the Administrator account. Enter a secure password and press Ctrl + Alt + Delete to log into the server for the first time: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%209.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/>
Step 10 – Remove the Installation ISO<br/><br/>
Once the installation finishes and the server boots successfully, remove the Windows Server 2022 ISO from the virtual machine’s storage settings to prevent the VM from booting into the installer again: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%2010.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/>
Step 11 – Adjust Time Zone Settings<br/><br/>
Open the system settings and configure the correct time zone for the server environment to ensure system time and logs are accurate: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%2011.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
<br/>
Step 12 – Test Shutdown and Restart Commands<br/><br/>
Opened Command Prompt and tested the system management command shutdown /i looked at other shutdown options using shutdown /?. These commands demonstrate different ways to shut down or restart the server using both the GUI and command line: <br/>
<img src="https://github.com/royalexvo/Helpdesk-Home-Lab-Windows-Server-2022-Installation-Virtual-Environment-Setup/blob/main/Step%2012.png?raw=true" height="80%" width="80%" alt="Lab Steps"/>
</p>
