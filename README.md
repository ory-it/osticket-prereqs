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
- PHP Manager for IIS
- Rewrite Module
- PHP 7.3.8
- VC_redist.x86.exe
- MySQL 5.5.62
- HeidiSQL

<h2>Installation Steps</h2>

![Screenshot 2024-03-12 at 7 19 44 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/c50a886d-8a69-43de-9c59-965966fda1f8)
<h3>Create an Azure Virtual Machine Windows 10, 4 vCPUs</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-12 at 9 29 36 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/e0b2759b-1aeb-4d98-9d6d-66392418d367)
<h3>Install / Enable IIS in Windows WITH CGI and Common HTTP Features and IIS Management Console</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-12 at 10 39 39 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/43282b45-8e4e-4603-b1db-90997a837aae)
<h3>Download and install PHP Manager for IIS & the Rewrite Module</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-12 at 10 40 51 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/79d97d80-89e5-47d7-9d4b-8e9894f0bb81)
<h3>Create the directory C:\PHP</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-12 at 11 08 24 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/b6a8262a-9c6c-4bcf-9dfb-990d416cff96)
<h3>Download and install PHP 7.3.8 and unzip the contents into C:\PHP</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-12 at 11 12 14 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/3dd889c8-87bc-40ad-8bc7-65dbf3b5185c)
<h3>Download and install VC_redist.x86.exe</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-12 at 11 20 06 PM](https://github.com/ory-it/osticket-prereqs/assets/67742620/fa32ad0d-4afe-4431-a225-c494c9d05aec)
<h3>Download and install MySQL 5.5.62</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-13 at 7 58 58 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/f1d1cd6b-2e4c-4f45-950c-39257a433084)
<h3>Open IIS as an Admin, Register PHP from within IIS, & Reload IIS</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-13 at 8 03 40 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/07f8d193-182f-4836-a28f-3e75a1a29c57)
<h3>Install osTicket v1.15.8, Reload IIS, & Go to sites -> Default -> osTicket</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-13 at 8 13 10 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/bfeddc51-83e9-479c-b5f4-542a3f4756e6)
<h3>Note that some extensions are not enabled</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-13 at 8 20 14 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/a1f2fe02-f23c-4b6b-90e4-c623996d7c4a)
<h3>Rename: ost-config.php, Assign Permissions: ost-config.php, & Continue Setting up osTicket in the browser</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-13 at 8 26 26 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/ba3502b6-bfac-41aa-ab90-e5c5c4a7b45b)
<h3>Download and install HeidiSQL</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


![Screenshot 2024-03-13 at 8 37 00 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/2cc90d51-9882-420a-8e80-554c7f21c6da)
<h3>Congratulations, hopefully it is installed with no errors!</h3>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

![Screenshot 2024-03-13 at 8 31 20 AM](https://github.com/ory-it/osticket-prereqs/assets/67742620/cffe61c8-f247-48a1-a562-cebeb5faad0c)
<h3>Clean up</h3>
<p>
- Delete: C:\inetpub\wwwroot\osTicket\setup
</p>
</p>
- Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />
