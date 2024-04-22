# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h2>osTicket - Prerequisites and Installation</h2>
This project: <br/>
- Defines the proper prerequistes in order to install OS Ticket.<br/>
- Step-by-step instructions installing OS Ticket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)
- Database Server (MySQL)
- PHP version that meets OS Ticket System requirements

<h2>Operating Systems Used </h2>

- Windows 10</b> (4 vCPUs)

<h2>List of Prerequisites</h2>

<br>In this project, the following files were used for installing OS Ticket:</br> <a href="https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Installation Files </a>
<br>
<img src="https://i.imgur.com/BcXJDxB.png"/>
<br>
<h2> Step-by-Step Guide for Installation of OS Ticket</h2>
<b>1. Install and Enable IIS in Windows 10 WITH
CGI and Common HTTP Features </b>
<br>
  -  Navigate to World Wide Web Services -> Application Development Features ->

  -  Check the following below:
      -  [X] CGI
      -  [X] Common HTTP Features<br>

  -  Navigate to IIS -> Web Management Tools -> IIS Management Console

  -  Check the following below:
      -  [X] IIS Management Console

<b>2. From the installation files (<a href="https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Installation Files </a>)  download and install the following:</b>

  -  PHP Manager for IIS
  -  Rewrite_amd64


<b>3. Create New PHP Folder on Computer's C Drive</b>

  -  Navigate to File Explorer -> My Computer/This PC -> Local Disk (C:)
  -  Right click to create new folder, named PHP

<b>4. From the installation files (<a href="https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Installation Files </a>)  download and install the following:<b/>

  -  PHP 7.3.8 and unzip contents into C:\PHP
       
<img src="https://i.imgur.com/rg2rh9C.png"/>
       
        
<b>7.  Download and Install VC_redist.x86.exe<b/>


<b>6. Downlowad and Install MySQL 5.5.62 using the following:</b>

  - Typical Setup ->
  - Launch Configuration Wizard (after install) ->
  - Standard Configuration ->
  - Username: root
  - Example Password: Password1

<b>8. Open IIS as an Admin</b>

<b>9. Register PHP from within IIS</b>

  -  Navigate to IIS -> PHP Manager -> Register New PHP Version

<img src= "https://i.imgur.com/ujfPruW.png"/>

<b>10. Reload IIS (Open IIS, Stop and Start the server)</b>

<b>11. Download and install OSTicket<b/>
   - Extract and copy the “upload” folder to c:\inetpub\wwwroot
   - Within c:\inetpub\wwwroot, Rename the “upload” folder to “osTicket”
<img src= "https://i.imgur.com/lfqRLxb.png"/>

<b>12. Reload IIS (Open IIS, Stop and Start the server)</b>

 - Open IIS
 - Stop and Restart 

<b>13. Go to sites -> Default -> osTicket</b>
   - Click "Browse *.80" on the right

<b>14. Enable extensions</b>
   - Go to IIS-> sites -> Default -> osTicket
   - Double-click PHP Manager
   - Click “Enable or disable an extension”
   - Enable: php_imap.dll
   - Enable: php_intl.dll
   - Enable: php_opcache.dll
   - Refresh the OS Ticket site

<img src="https://i.imgur.com/l6RaZNQ.png"/>

<b>15. Rename: ostsample-config.php to ost-config.php</b>
   - From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
   - To: C:\inetpub\wwwroot\osTicket\include\ost-config.php


<b>16. Assign Permissions: ost-config.php</b>

   - Right click ost-config.php
   - Click security -> Advanced settings
   - Disable inheritance -> Remove All
   - Click Select a principal
   - New Permissions -> Everyone -> All
   - Apply -> Ok

<img src ="https://i.imgur.com/eK1Spdm.png"/>

<b>17. Download and install HeidiSQ from <a href="https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Installation Files </a></b>
<br>

<b>18. Open Heidi SQL<b/>
- Create a new session with the following:
    - Username:  root
    - Password: Password1
- Connect to the session
- Right click and create a database called “osTicket”

<b>18. Continue Setting up osTicket in the browser (click Continue)</b>
- Example Name: Helpdesk
- Default email (receives email from customers)


<b>19. Continue Setting up osticket in the browser(Click Continue) </b>
   - MySQL Database: osTicket
   - MySQL Username: root
   - MySQL Ex. Password: Password1
   - Click “Install Now!”


<b>20. Congratulations! osTicket should be installed without any errors.</b>

<img src= "https://i.imgur.com/H3tDxR9.png"/>
  - Browse to your help desk login page: http://localhost/osTicket/scp/login.php </a>
  - End Users osTicket URL: http://localhost/osTicket/


<b>21. Clean up</b>
   - Delete: C:\inetpub\wwwroot\osTicket\setup
   - Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<p>

</p>
<br />
