<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: Lab 3.1. osTicket Setup | Microsoft Azure | IT Tutorial Speedrun Walkthru](https://youtu.be/NNOhNYb7XHE)
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket installation files
- Heidi SQL

<h2>Installation Steps (15 Steps)</h2>

<p>
</p>
<p>
Peace be upon you and welcome to my first in-depth IT tutorial!

1.) First, visit Microsoft Azure Portal (portal.azure.com), and create a Virtual Machine (VM).

  - A VM is a remote computer AKA a "clean slate" computer.
    - It protects our Personal Computer (PC) from any mishaps and/or malfunctions.
    - It allows for continuous replication of the lab to ensure maximum efficiency.

  - Details of VM   
    - Subscription
      - Resource group: osTicket
  
    - Instance details
      - Virtual machine name: osticket-vm
      - Region: (US) East US 2
      - Image: Windows 10 Pro, version 22H2 - x64 Gen2
      - Size: Standard_D2s_v3 - 2 vcpus, 8 GiB memory

    - Administrator account
      - Username: labuser
      - Password: osTicketPassword1!

<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/256d4d5c-fce6-49ca-a4cc-1a865ec48b8f" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
2.) Next, connect the newly created VM using Remote Desktop Connection (RDP). 

  - We can do so by copying and pasting our public IPv4 address.

    - Note: If you are a Mac user you will have to download Micosoft Remote Desktop. 
  
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/8873d88a-baf4-4155-9655-eebc94a583ed" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<p>
<br />
  
<p>
</p>
<p>
3.) Enable Internet Information Services (IIS). 
  
  - First, access the Control Panel -> Uninstall a program -> Turn Windows features on or off -> Observe the list and enable IIS.
    
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/490990a7-9471-48e7-b7fd-a6ba6bfe5906" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
4.) Now that IIS is enabled we can now install Web Platform Installer, which you can find here: 

  - https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

  - The link above contains the necessary downloadable material for osTicket. Simply click the link and install the Web Platform Installer.
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/0eda6fe3-d447-4183-ad23-7b308f6b5d16" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
5.) Next, we will extract all of our recently downloaded material onto the desktop.
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/cabc17e2-371e-47e6-a92c-a4ac35372066" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
6.) Then, install these two files within the "osTicket-Installation-Files" folder.

  - PHPManagerForIIS_V1.5.0
  - rewrite_amd64_en-US
        
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/caa421eb-671e-4bd0-ba95-16e339cd1878" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
7.) Within the Windows (C:) folder, create a folder named "PHP" and then extract all files from "php-7.3.8-nts-Win32-VC15-x86" into the PHP folder.

  - Then, install the remaining files:
    - VC_redist_x86
    - mysql-5.5.62-win32
      - Setup Type: Typical
      - Server Instance Configuration: Standard Configuration
        - Password: root
       
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/f274ab11-b8c8-4042-a862-000c45b4b86e" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
8.) Next, open IIS as an admin -> PHP Manager -> Register new PHP version -> "PHP" -> "php_cgi"
  
  - Then, stop and start the server (refresh).
  
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/40d7c9fd-b489-4ebc-98a4-e70cafd92dcb" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
9.) Within the zip file "osTicket-v1.15.8", drag and drop the "upload" folder into "wwwroot", and then rename "upload" folder to "osTicket".
  
  (Then, stop & start the server.)
  
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/0d81b638-389e-47e8-9376-84aa8ebfb5ab" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
10.) Within IIS Manager -> Sites -> Default Web Site -> osTicket -> Browse *:80 (http)
  
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/81e2f9cd-cce5-4dfc-8c4e-6e66189279c9" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
11.) In IIS Manager -> Default Web Site (x2) -> PHP Manager -> Enable or disable an extension -> enable three particular extensions: 
  
  - "php_imap.dll"
  - "php_intl.dll"
  - "php_opcache.dll"

(Then, refresh the osTicket browser.)

<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/060d0b62-44d6-4672-a432-68c9b3f84ecf" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
12.) Proceed to Windows (C:) -> inetpub -> wwwroot -> osTicket -> include -> Scroll down fully & rename "ost-sampleconfig.php" to "ost-config.php" - next, right click "ost-config.php" -> Properties -> Security -> Advanced -> Add -> Select a principal -> Type: "everyone" -> Check Names -> OK -> Check box titled "Full control" -> OK -> Apply
  
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/aaa65441-802d-4291-b844-d9ba4e3029b1" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
13.) Back in the web browser, continue into osTicket Installer and enter your information.

  - System Settings
    - Note: "Default Email" is the one which receives Emails from customers.
    - Note: "Email Address" must be different from "Default Email".

  - Admin User
    - Username: adminuser
    - Password: Password1
  
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/43af42ff-dd1c-47b5-bf1e-7dc0d052d611" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
14.) In our "osTIcket-Installation-Files" folder -> open "HeidiSQL_12.3.0.6589_Setup" -> Accept the agreement -> Next (x4) -> Install
  
  - In HeidiSQL, click +New -> enter Username & Password

    - Username: root
    - Password: root
    
  Note: The use of "root" for the username & password is solely for lab purposes---this is not a good idea to do in the real world! God Bless <3
   
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/3d79e54d-ed82-47de-a871-9588970f49f2" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
15.) Enjoy using osTicket Support Ticket System! - بارك الله فيكم

  - Database Settings
    - MySQL Username: root
    - MySQL Password: root

  - Admin login: http://localhost/osTicket/scp/login.php
   
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/4f30a1a1-447a-443b-8e0b-955df3958b3b" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
