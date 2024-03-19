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

- Virtual Machine in Azure
- [PHP Manager for IIS](https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link)
- [Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link)
- [PHP 7.3.8](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link)
- [VC_redist.x86.exe](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)
- [MySQL 5.5.62](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link)
- [HeidiSQL](https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit)

<h2>Installation Steps</h2>

![Screenshot 2024-03-12 at 7 19 44 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/c50a886d-8a69-43de-9c59-965966fda1f8)
<h3>Create an Azure Virtual Machine Windows 10, 4 vCPUs</h3>

Create an Azure Virtual Machine Windows 10, 4 vCPUs
- Name: Vm-osticket
- Username: labuser (for example/whatever you chose)
- Password: osTicketPassword1! (for example/whatever you chose)
<p>
	To create a Windows 10 Azure Virtual Machine (VM) with 4 virtual CPUs (vCPUs), start by logging into the Azure Portal. Once logged in, navigate to the "Virtual Machines" section and select "Create" or "+ Add" to initiate a new VM setup. In the creation wizard, choose your subscription and a resource group, or create a new one if necessary. When specifying the VM details, select a region and then choose a size that offers 4 vCPUs—Azure provides different VM sizes, so select one like the "D-Series" that meets the requirement. For the image, search for and select a Windows 10 option available in the marketplace. Proceed to configure the administrator account with a username and password, and set up inbound port rules, allowing RDP (Remote Desktop Protocol) to enable remote access. Review the remaining settings, adjusting them as needed for network, management, and additional features. Finally, review the summary and hit "Create" to deploy your Windows 10 VM with 4 vCPUs. After the VM is deployed, you can connect to it using RDP to start using your Windows 10 environment on Azure.
</p>
<br/>


![Screenshot 2024-03-12 at 9 29 36 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/e0b2759b-1aeb-4d98-9d6d-66392418d367)
<h3>Install / Enable IIS in Windows WITH CGI and Common HTTP Features and IIS Management Console</h3>

- World Wide Web Services -> Application Development Features ->
  [X] CGI
  [X] Common HTTP Features
- Internet Information Services -> Web Management Tools -> IIS Management Console
	[X] IIS Management Console
<p>
	To install and enable Internet Information Services (IIS) with CGI, common HTTP features, and the IIS Management Console on a Windows 10 Virtual Machine, begin by opening the Control Panel and navigating to "Programs and Features." From there, select "Turn Windows features on or off" to open the Windows Features dialog. In this dialog, locate and expand the "Internet Information Services" node. Make sure to check the boxes for "IIS Management Console" under "Web Management Tools," and under "World Wide Web Services," expand "Application Development Features" to enable "CGI." Additionally, under "Common HTTP Features," select the desired features such as Static Content, Default Document, and Directory Browsing. Click "OK" to initiate the installation process. Windows will then install the selected components, and you might need to restart the VM to complete the installation. 
</p>
<br/>


![Screenshot 2024-03-12 at 10 39 39 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/43282b45-8e4e-4603-b1db-90997a837aae)
<h3>Download and install PHP Manager for IIS & the Rewrite Module</h3>


![Screenshot 2024-03-12 at 10 40 51 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/79d97d80-89e5-47d7-9d4b-8e9894f0bb81)
<h3>Create the directory C:\PHP</h3>
<p>
	Open File Explorer by pressing the Windows key + E, navigate to the C: drive, and right-click in an empty space within the drive's window. From the context menu that appears, select "New" and then "Folder." Name this new folder "PHP" and press Enter. Your directory C:\PHP will now be created and ready for use, serving as a designated location for PHP-related files or installations, should you choose to use it for such purposes. 
</p>
<br/>


![Screenshot 2024-03-12 at 11 08 24 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/b6a8262a-9c6c-4bcf-9dfb-990d416cff96)
<h3>Download and install PHP 7.3.8 and unzip the contents into C:\PHP</h3>


![Screenshot 2024-03-12 at 11 12 14 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/3dd889c8-87bc-40ad-8bc7-65dbf3b5185c)
<h3>Download and install VC_redist.x86.exe</h3>


![Screenshot 2024-03-12 at 11 20 06 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/fa32ad0d-4afe-4431-a225-c494c9d05aec)
<h3>Download and install MySQL 5.5.62</h3>

- Typical Setup ->
- Launch Configuration Wizard (after install) ->
- Standard Configuration ->
- Password1


![Screenshot 2024-03-13 at 7 58 58 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/f1d1cd6b-2e4c-4f45-950c-39257a433084)
<h3>Open IIS as an Admin, Register PHP from within IIS, & Reload IIS</h3>
<p>
	On a Windows 10 system, to open Internet Information Services (IIS) Manager with administrative privileges, type "IIS" into the search bar, right-click on the "Internet Information Services (IIS) Manager" result, and select "Run as administrator." To register PHP, in the IIS Manager, select your server's name in the left-hand connections pane, then double-click "Handler Mappings" in the main panel. Click "Add Module Mapping" in the right-hand actions pane, entering "*.php" in the "Request path," selecting "FastCgiModule" for the "Module," and specifying the path to your "php-cgi.exe" file (e.g., "C:\PHP\php-cgi.exe") in the "Executable" field. Name the handler "PHP via FastCGI" or a similar descriptive name, then click "OK" to register it. To reload IIS and apply the changes, open Command Prompt as an administrator by typing "cmd" in the search bar, right-clicking on "Command Prompt," and choosing "Run as administrator." In the Command Prompt, type "iisreset" and press Enter, which will stop and then restart all IIS services, ensuring your PHP registration takes effect.
</p>
<br/>


![Screenshot 2024-03-13 at 8 03 40 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/07f8d193-182f-4836-a28f-3e75a1a29c57)
<h3>Install osTicket v1.15.8, Reload IIS, & Go to sites -> Default -> osTicket</h3>

Install osTicket v1.15.8
- Download osTicket from the Installation Files Folder
- Extract and copy “upload” folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

Go to sites -> Default -> osTicket
- On the right, click “Browse *:80”


![Screenshot 2024-03-13 at 8 13 10 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/bfeddc51-83e9-479c-b5f4-542a3f4756e6)
<h3>Note that some extensions are not enabled</h3>

- Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
  - Enable: php_imap.dll
  - Enable: php_intl.dll
  - Enable: php_opcache.dll
- Refresh the osTicket site in your browse, observe the changes


![Screenshot 2024-03-13 at 8 20 14 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/a1f2fe02-f23c-4b6b-90e4-c623996d7c4a)
<h3>Rename: ost-config.php, Assign Permissions: ost-config.php, & Continue Setting up osTicket in the browser</h3>

Rename: ost-config.php
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php
- Disable inheritance -> Remove All
- New Permissions -> Everyone -> All

Continue Setting up osTicket in the browser (click Continue)
- Name Helpdesk
- Default email (receives email from customers)


![Screenshot 2024-03-13 at 8 26 26 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/ba3502b6-bfac-41aa-ab90-e5c5c4a7b45b)
<h3>Download and install HeidiSQL</h3>

- Open Heidi SQL
- Create a new session, root/Password1
- Connect to the session
- Create a database called “osTicket”


![Screenshot 2024-03-13 at 8 37 00 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/2cc90d51-9882-420a-8e80-554c7f21c6da)
<h3>Congratulations, hopefully it is installed with no errors!</h3>

Browse to your help desk login page:[](http://localhost/osTicket/scp/login.php)


![Screenshot 2024-03-13 at 8 31 20 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/cffe61c8-f247-48a1-a562-cebeb5faad0c)
<h3>Clean up</h3>

- Delete: C:\inetpub\wwwroot\osTicket\setup
- Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

