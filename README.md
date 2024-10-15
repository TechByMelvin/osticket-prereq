<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


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
Set Up the Azure Virtual Machine
Provision a new Windows 10 VM on Azure with the following configuration:

-VM Name: osticket-vm 

-vCPUs: 4 

-RAM: 8 GB (recommended)


</p>
<br />


<p>
<img src="https://i.imgur.com/hn2GzqE.jpg" />
</p>
<p>
Access the VM via Remote Desktop.
  
-Download and install a Remote Desktop client (e.g., Windows Remote Desktop).

-Log into the VM using the credentials above.

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Install and Configure IIS (Web Server).
  
-Open Server Manager > Add Roles and Features.

-Select Web Server (IIS) and ensure that the CGI feature is enabled under Application Development Features.

-Confirm the installation and restart IIS once completed.

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install PHP for IIS:
  
-From the osTicket-Installation-Files folder (download from osTicket’s official site), install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi).

-Install Rewrite Module (rewrite_amd64_en-US.msi) from the same folder.

-Create the directory C:\PHP, then unzip PHP 7.3.8 into this folder.

-Register PHP in IIS:

-Open IIS > PHP Manager > Register new PHP version.
Point to C:\PHP\php-cgi.exe.

-Restart IIS to apply changes.

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install MySQL and Configure Database:
  
-From the osTicket-Installation-Files, install MySQL 5.5.62 (mysql-5.5.62-win32.msi) with these settings:
   Typical Setup.
   Username: root.
   Password: root.

-After installation, launch the MySQL configuration wizard and complete the setup.

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket:
-Unzip osTicket v1.15.8 from the installation files and copy the upload folder to C:\inetpub\wwwroot.
  
-Rename the upload folder to osTicket.

-Restart IIS and browse to http://localhost/osTicket to launch the osTicket installation wizard.

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable Required PHP Extensions:
  
-In IIS, go to PHP Manager > Enable or disable an extension.

-Enable the following extensions:

   php_imap.dll

   php_intl.dll

   php_opcache.dll

-Restart IIS and refresh the osTicket page in the browser.

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure osTicket:
  
-Rename the file C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to ost-config.php.

-Set the correct file permissions:

   Right-click ost-config.php > Properties > Security.

   Disable inheritance and remove all permissions.

   Assign Full Control to Everyone.

-In your browser, continue the osTicket installation wizard:

   Helpdesk Name: Your preferred name (e.g., "IT Support Desk").

   Default Email: An email address for receiving customer tickets.

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Set Up the MySQL Database for osTicket:
  
-Install HeidiSQL (from the osTicket-Installation-Files folder).

-Connect to MySQL with root/root credentials.

-Create a new database named osTicket.

-In the osTicket setup wizard, provide the following database details:

   MySQL Database: osTicket

   MySQL Username: root

   MySQL Password: root

-Click Install Now to complete the osTicket installation.

</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Final Steps and Cleanup:
  
-Delete the folder C:\inetpub\wwwroot\osTicket\setup.

-Set C:\inetpub\wwwroot\osTicket\include\ost-config.php to Read-only for security.

-Verify that osTicket is accessible via the following URLs:

   Admin Panel: http://localhost/osTicket/scp/login.php

   End-User Portal: http://localhost/osTicket/

</p>
<br />


