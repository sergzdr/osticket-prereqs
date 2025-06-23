<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: Lab 3.1. osTicket Setup | Microsoft Azure | IT Tutorial Speedrun Walkthru](https://youtu.be/t7shFAn6G8Q)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket installation files
- Heidi SQL

<h2>Installation Steps (13 Steps)</h2>

<p>
</p>
<p>
Peace be upon you and welcome to my first in-depth IT tutorial!
  
1.) I shall begin by creating a remote computer---AKA a virtual machine (VM)---using the Microsoft Azure portal (portal.azure.com). The use of a VM will protect our physical machine in the event of any unforeseen malfunctions or mishaps. Plus, any created VM will act as a clean slate computer fit for continual replication of the lab (i.e., good practice). Next, create a resource group titled "osTicket". Then, create a VM with 2-4 vCPUs. In this example I will be using 3 vCPUs.
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/256d4d5c-fce6-49ca-a4cc-1a865ec48b8f" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
2.) Next, we will connect our newly created VM using Remote Desktop Connection (RDP). We can do so by copying and pasting our public IPv4 address. If you are a Mac user you will have to download Micosoft Remote Desktop. 
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/8873d88a-baf4-4155-9655-eebc94a583ed"/>
<p>
<br />
  
<p>
</p>
<p>
3.) Enable Internet Information Services (IIS). First, access the Control Panel -> Uninstall a program -> Turn Windows features on or off -> Observe the list and enable IIS.
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/490990a7-9471-48e7-b7fd-a6ba6bfe5906" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
4.) Now that IIS is enabled we can now install Web Platform Installer, which you can find here: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 - This link contains the necessary downloadable material for osTicket. Simply click the link and install the Web Platform Installer.
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/0eda6fe3-d447-4183-ad23-7b308f6b5d16" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
5.) Next, we will extract all of our recently downloaded material onto the desktop.
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/cabc17e2-371e-47e6-a92c-a4ac35372066" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
6.) Then, we will install the various files within the osTicket-Installation-Files folder.
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/caa421eb-671e-4bd0-ba95-16e339cd1878" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
7.) Within the Windows (C:) folder, create a folder named "PHP" and extract all files from the compressed zip folder into the recently made PHP folder.
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/f274ab11-b8c8-4042-a862-000c45b4b86e" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
8.) Register new PHP.
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/40d7c9fd-b489-4ebc-98a4-e70cafd92dcb" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
9.) Drag and drop "upload" folder, rename "upload" folder to "osTicket".
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/0d81b638-389e-47e8-9376-84aa8ebfb5ab" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
10.) Within IIS -> Sites -> osTicket -> browse. 
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/81e2f9cd-cce5-4dfc-8c4e-6e66189279c9" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
11.) Enable three extensions then refresh the osTicket browser.
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/060d0b62-44d6-4672-a432-68c9b3f84ecf" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
12.) Rename "ost-sampleconfig.php" to "ost-config.php" and enable full control for everyone. 
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/aaa65441-802d-4291-b844-d9ba4e3029b1" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
13.) Enjoy using osTicket ticketing system! بارك الله فيكم
<p>
</p>
<p>

<img src="https://github.com/user-attachments/assets/43af42ff-dd1c-47b5-bf1e-7dc0d052d611" alt="Disk Sanitization Steps"/>
<p>
<br />
  
<p>
</p>
<p>
