<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

-Windows Server or Windows 10 (for hosting) 

-Web Server (IIS)

-PHP 7.4 or higher (for running PHP scripts) 

-MySQL Database (for data storage)

-osTicket Installation Files (available from osTicket website)


<h2>Installation Steps</h2>

</p>
<img width="1440" alt="Screenshot 2024-10-12 at 3 05 57 PM" src="https://github.com/user-attachments/assets/32afab57-ad76-410f-b68f-059d13062bf0">
</p>
<p>
Set up a Virtual Machine in Azure
Provision a Windows 10 or Windows Server VM on Microsoft Azure.
Ensure that the VM has at least 2 vCPUs, 4 GB of RAM, and sufficient disk space.

<br />

<p>

<p>
Install IIS (Internet Information Services)
Open Server Manager on Windows, go to Add Roles and Features.
Select Web Server (IIS) and enable necessary features like CGI.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install PHP
Download the latest stable version of PHP (7.4 or higher) for Windows.
Configure PHP with IIS using FastCGI.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Set up MySQL Database

Install MySQL on the same or a separate server.
Create a new database and a user for osTicket.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install PHP
Download the latest stable version of PHP (7.4 or higher) for Windows.
Configure PHP with IIS using FastCGI.
</p>
<br />
