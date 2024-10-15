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
<img src="https://imgur.com/HeaeMzX.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1.Set Up the Azure Virtual Machine
Provision a new Windows 10 VM on Azure with the following configuration:

-VM Name: osticket-vm 

-vCPUs: 4 

-RAM: 8 GB (recommended)


</p>
<br />


<p>
<img src="https://imgur.com/wsMfxHw.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2.Access the VM via Remote Desktop.
  
 1.Download and install a Remote Desktop client (e.g., Windows Remote Desktop).

 2.Log into the VM using the credentials above.

</p>
<br />


<p>
<img src="https://imgur.com/EdmY5zD.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3.Install and Configure IIS (Web Server).
  
 1.Open Server Manager > Add Roles and Features.

 2.Select Web Server (IIS) and ensure that the CGI feature is enabled under Application Development Features.

 3.Confirm the installation and restart IIS once completed.

</p>
<br />


<p>
<img src="https://imgur.com/lLqxgrW.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4.Install PHP for IIS:
  
 1.From the osTicket-Installation-Files folder (download from osTicket’s official site), install PHP Manager for IIS 
 (PHPManagerForIIS_V1.5.0.msi).

 2.Install Rewrite Module (rewrite_amd64_en-US.msi) from the same folder.

 3.Create the directory C:\PHP, then unzip PHP 7.3.8 into this folder.

 4.Register PHP in IIS:

 5.Open IIS > PHP Manager > Register new PHP version.
 Point to C:\PHP\php-cgi.exe.

 6.Restart IIS to apply changes.

</p>
<br />


<p>
<img src="https://imgur.com/ySdKXfc.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5.Install MySQL and Configure Database:
  
 1.From the osTicket-Installation-Files, install MySQL 5.5.62 (mysql-5.5.62-win32.msi) with these settings:
    Typical Setup.
    Username: root.
    Password: root.

 2.After installation, launch the MySQL configuration wizard and complete the setup.

</p>
<br />


<p>
<img src="https://imgur.com/JkJaLCp.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
6.Install osTicket:
  
 1.Unzip osTicket v1.15.8 from the installation files and copy the upload folder to C:\inetpub\wwwroot.
  
 2.Rename the upload folder to osTicket.

 3.Restart IIS and browse to http://localhost/osTicket to launch the osTicket installation wizard.

</p>
<br />


<p>
<img src="https://imgur.com/hX8fdD4.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
7.Enable Required PHP Extensions:
  
 1.In IIS, go to PHP Manager > Enable or disable an extension.

 2.Enable the following extensions:

   php_imap.dll

  php_intl.dll

  php_opcache.dll

 3.Restart IIS and refresh the osTicket page in the browser.

</p>
<br />


<p>
<img src="https://imgur.com/55TzKqm.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
8.Configure osTicket:
  
 1.Rename the file C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to ost-config.php.

 2.Set the correct file permissions:

   1.Right-click ost-config.php > Properties > Security.

   2.Disable inheritance and remove all permissions.

   3.Assign Full Control to Everyone.

3.In your browser, continue the osTicket installation wizard:

   Helpdesk Name: Your preferred name (e.g., "IT Support Desk").

   Default Email: An email address for receiving customer tickets.

</p>
<br />


<p>
<img src="https://imgur.com/RhmcHy0.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9.Set Up the MySQL Database for osTicket:
  
  1.Install HeidiSQL (from the osTicket-Installation-Files folder).

  2.Connect to MySQL with root/root credentials.

 3.Create a new database named osTicket.

 4.In the osTicket setup wizard, provide the following database details:

   -MySQL Database: osTicket

   -MySQL Username: root

   -MySQL Password: root

 5.Click Install Now to complete the osTicket installation.

</p>
<br />


<p>
<img src="https://imgur.com/VCPz9Nd.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
10.Final Steps and Cleanup:
  

   1.Set C:\inetpub\wwwroot\osTicket\include\ost-config.php to Read-only for security.

   2.Verify that osTicket is accessible via the following URLs:

   Admin Panel: http://localhost/osTicket/scp/login.php

   End-User Portal: http://localhost/osTicket/

</p>
<br />


