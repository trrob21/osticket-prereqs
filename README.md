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

!! ATTENTION !! If this appears, choose to “Keep” the file:

<img width="354" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/7d84f212-5137-4a89-8f05-49133887b59b">
</p>
<br />
9. Next, download and install the VC_redist.x86.exe from the installation files. Go through the setup wizard to finish setting up and installing.
</p>
<br />
10. Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) Run the setup wizard: Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration ->
</p>
</p>
<br />
Make a new root password: Password1
</p>
<img width="350" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/56148589-43cc-4e0d-b1ae-bc9d8c6a6c2a">
</p>
<br />
Execute the process.
</p>
<img width="352" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/22e1f723-4277-42ba-a62d-c6b20e99255b">
</p>
<br />
11. After downloading and installing the files search for IIS in the windows search bar and open program as administrator. The program looks like this.
</p>
<img width="355" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/dd42f37c-559f-45b7-b354-a80a62742004">
</p>
<br />
12. Now we have to register PHP within IIS. Click PHP Manager then select "Register new PHP version".
</p>
<img width="353" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/a6559788-0ec2-4751-baa4-31b5ff53b2e1">
</p>
Provide a path to the php executable file (php-cgi.exe). Go to C Drive -> PHP -> click on php-cgi file.
</p>
<img width="385" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/d2d79e51-6aa3-461c-8b88-6ec77f7bd5f0">
</p>
Then restart the IIS server.
</p>
<img width="1130" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/3aaa3ec5-e1ef-4cca-9781-90c6f8f39e4c">
</p>
<br />
13. Install osTicket v1.15.8
</p>
  -Download osTicket from the Installation Files Folder

  -Extract and copy "upload" folder to c:\inetpub\wwwroot
  
  -Within c:\inetpub\root, Rename "upload" to "osTicket"
  </p>
  Reload IIS again
</p>
<br />
14. On IIS go to sites -> Default -> osTicket -On the right, click “Browse *:80”
</p>
<img width="1128" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/340ca697-e553-4746-98d0-a0ec88865c0d">
</p>
You'll notice that some extensions are not enabled on the osTicket browser.
</p>
<img width="614" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/ec7832a3-16cd-4c72-878b-4de5ec2f15a6">
</p>
To enable the extensions Go back to IIS, sites -> Default -> osTicket -Double click PHP manager -Click "Enable or disable an extension".
</p>
<img width="712" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/12b6aa39-c42b-4b0d-ac29-57e079ad7b4a">
</p>
You want to enable three extensions from here.

1.) php_imap.dll

2.) php_intl.dll

3.) php_opcache.dll
</p>
<br />

15. Now we need to rename one of our files in the osTicket folder.Go into the file explorer and search for C;\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename "ost-sampleconfig.php" to "ost-config.php"

Once you have renamed the file right click on it and go to properties. From there click security -> advance -> disable inheritance -> Remove all inherted permissions from this object.

Now add new permissions 

Click Add -> select Principal

Type "Everyone" in the box then click OK.

Make sure all bowes are checked.

<img width="680" alt="image" src="https://github.com/trrob21/osticket-prereqs/assets/150396137/b0e8a82e-62c7-41c7-99ca-a4925a3b451b">















