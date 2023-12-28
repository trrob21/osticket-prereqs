<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro</b> (22H2) x64 Gen 2

<h2>List of Prerequisites</h2>

• PHP Manager

• IIS (Internet Infomation Services)

• MySQL

• Heidi SQL

• Rewrite Module

• osTicket v1.15.8

• VC Redist

• Link to Downloads https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

<p>
1. First your going to want to do is creat a virtual machine using Azure (https://portal.azure.com/). Setup your virtual machine with Windows 10 Pro 22h2 x64 Gen 2 with at least 2 vcpus and 16 Gib memory.
  
<img src="https://github.com/trrob21/osticket-prereqs/assets/150396137/b4acaa20-bebe-4073-8099-a4aab9e769cf">

2. Once your virtual machine is created you will want to take note of the public ip address the vm is setup with so you can connect to it using the Remote Desktop App
</p>
<p>
</p>
<br />

<p>
<img width="1217" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/66f12370-e628-4f8d-bcd5-87af1bc7c6b2">
<img width="310" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/b13053e6-1195-449f-a1e9-bc4dc6de7a8f">


</p>
<p>
3. After connecting to your virtual machine you want to open up your control panel. From there open "Programs" and select "Turn windows features on and off".
</p>
<br />

<p>
<img width="841" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/4c660131-264b-4df6-a636-eba56e0d6f08">
<img width="579" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/44973e60-10ad-442d-9411-ca85da8ce996">



</p>
<p>
4. you want to install and enable IIS in windows with CGI and Common HTTP Features. Make sure all Common HTTP Features are checked.
  <img width="337" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/f445f00e-828b-44cd-bb9e-13598afd7b99">

  To make sure IIS is installed/enabled you can open your browser and type 127.0.0.1 in the search bar and it should look like this.
  <img width="1920" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/1f07d91b-6b89-456f-b597-cf540cc2a93c">

</p>
<br />
5. Now that IIS is installed you want to download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) from the installation files. Go through the install wizard and complete the install.
</p>
6. Next download and install the Rewrite Module (rewrite_amd64_en-US.msi) from the installation files.
</p>
<br />
7. Create a folder in the C drive called PHP.
</p>
<br />
8. From the Installation Files, download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) and unzip the contents into C:\PHP
