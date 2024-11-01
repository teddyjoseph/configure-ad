# On-premises-Active-Directory-Deployed-in-the-Cloud-Azure-<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create 2 virtual machines (Client-1 and Domain Controller) on Azure and connect them via remote desktop
- Install Active Directory and promote to a Domain Controller on the server's virtual machine
- Connect the Windows virtual machine to the Domain Controller
- Use Powershell to populate the employee list and attempt to log into client-1 virtual machine with one of the users listed

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/SHHOct8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the image above, Active Directory is being installed and is being promoted to a Domain Controller. To promote as a Domain Controller, you must setup a new forest as mydomain.com (It can be anything, you just have to remember it).
</p>
<br />

<p>
<img src="https://i.imgur.com/j50yNfV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The image above shows when you link both virtual machines. This happens by making the private IP address of the Domain Controller the same as the virtual machine (Client-1).
</p>
<br />

<p>
<img src="https://i.imgur.com/jP4xpdF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally, you run Powershell ISE from the Domain controller. From Powershell, remotely allow domain users to access the computer from the Windows Virtual Machine. This will populate the employee list as shown above.
<br />
