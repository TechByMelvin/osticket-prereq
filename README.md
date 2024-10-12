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
</p>
<br />


<p>
<img src="https://i.imgur.com/hn2GzqE.jpg" />
</p>
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
Configure IIS:
Register PHP (C:\PHP\php-cgi.exe in IIS).
Restart IIS and enable PHP extensions (php_imap.dll, php_intl.dll, php_opcache.dll).
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket:
Unzip osTicket files to c:\inetpub\wwwroot\osTicket.
Rename ost-sampleconfig.php to ost-config.php and set permissions.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Database & Final Setup:
Create osTicket database with HeidiSQL.
Complete the installation via browser using MySQL credentials (root/root).
</p>
<br />
