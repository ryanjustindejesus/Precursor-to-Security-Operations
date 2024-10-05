<h1>Precursor to Security Operations</h1>
<b>This tutorial outlines the installation of another Windows virtual machine and using it to generate failed login attempts from both Windows and Linux virtual machines</b>

<h2>Environments and Technologies Used</h2>

- <b>Microsoft Azure</b> 
- <b>Remote Desktop</b>
- <b>PowerShell</b>

<h2>Operating Systems</h2>

- <b>Windows 10</b>


<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/d47c2b24-baf6-457e-bbb9-83131b645ad3)
- <b>Create another Windows virtual machine in a region outside of the US and name it "attack-vm"</b>
- <b>Name the Resource Group: RG-Cyber-Lab Attacker</b>
- <b>Name the VNet: Lab-VNet-Attacker</b>

![image](https://github.com/user-attachments/assets/0f3509df-8ac6-4224-848a-add810dbbbc9)
- <b>Log into the attack-vm</b>
- <b>Open Remote Desktop Connection</b>
- <b>Use the IP address of the windows-vm</b>
- <b>Perform 3 failed login attempts to generate some failed Remote Desktop Connection logs against the windows-vm</b>

![image](https://github.com/user-attachments/assets/d4a33559-3389-40a7-9107-430b1b4b2296)
- <b>Download SQL Server Management Studio on the attack-vm</b>
- <b>Use the IP address of the windows-vm</b>
- <b>Perform 3 failed login attempts to generate some failed MS SQL Auth logs against the windows-vm</b>

![image](https://github.com/user-attachments/assets/8453203d-b20a-4340-8e93-75901186d719)
- <b>Open Windows PowerShell in the attacker-vm</b>
- <b>Use the IP address of the windows-vm</b>
- <b>Perform 3 failed login attempts using SSH to generate some failed logs against the linux-vm</b>

![image](https://github.com/user-attachments/assets/446f1b83-930b-4b59-8d9a-147989daa88c)
- <b>Log into your windows-vm</b>
- <b>Open Event Viewer</b>
- <b>Inspect the failures and successes in the security logs</b>

![image](https://github.com/user-attachments/assets/4dceeabf-f38e-47bc-818b-fc969d81e9c4)
- <b>Open PowerShell and login to the linux-vm</b>
- <b>Change directory to /var/log: cd /var/log</b>
- <b>List the contents of the logs directory: ls</b>
- <b>Display and filter the auth.log related to the user ryan: cat auth.log | grep ryan</b>
