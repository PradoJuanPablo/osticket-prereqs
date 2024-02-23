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

<ol>
  <li>Set up an Azure Virtual Machine (VM) environment (Windows 10 4 vCPUs Recommended)</li>
  <li><a href = "https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">osTicket Installation Files</a> (Download these files on your Azure Virtual Machine) </li>
  <li>Enable IIS in I.S.S.</li>
  <li>Install Web Platform Installer</li>
  <li>Install MySQL and set up username and password</li>
    <ul>
    <li>For this tutorial, we will set up our username and password as such:</li>
      <ul>
      <li>username: Labuser</li>
      <li>password: Password1234</li>
      </ul>
    </ul>
  <li>Install C++ Redistributable</li>
  <li>Configure permissions and install osTicket</li>
</ol>

<h2>Installation Steps</h2>

<p>

<img width="919" alt="image" src="https://github.com/PradoJuanPablo/osticket-prereqs/assets/160810181/9145b766-c8ba-4a27-9eda-6a7995cf80a4">
"/>
</p>
<p>
First, we will create a Resource Group (RG) in Azure. A resource group is like a folder. We will name this resouce group "RG-osTicket". I used US East as the region to create my RG. Just keep in mind which region you created your RG in because we will be using it with future deployments. 
</p>
<br />

<p>
<img width="829" alt="image" src="https://github.com/PradoJuanPablo/osticket-prereqs/assets/160810181/799972dc-ac8d-4b59-a2c6-cca9b937945b">

</p>
<p>
Next, we will create our Virtual Machine (VM). A VM is essentially a computer within a computer. I named this VM "VM-osTicket" and set the region as US East as I did with my Resource Group. We will use Windows 10 with 2vCPUs in this instance.

Create a username and password for your VM, we will be using it to log in so take note of your credentials. I set my username to be "Labuser" and my password to "Password1234". This is in no way best practice in the real world, but for demonstration purposes it's fine. 

Now that our VM is created, we will be logging in using Remote Desktop Connection. To do that we need to grab out VM's public IP address
</p>
<br />

<p>
<img width="600" alt="image" src="https://github.com/PradoJuanPablo/osticket-prereqs/assets/160810181/093194ae-d92b-4fb2-b4b1-ee70896afb5d">

<img width="450" alt="image" src="https://github.com/PradoJuanPablo/osticket-prereqs/assets/160810181/335594e8-c008-4942-8cd2-47d181bec0cb">

</p>
<p>
Now that we have our IP, open Remote Desktop Connestion and connect using that IP and your login credentials
</p>
<br />

<p>
<img width="719" alt="image" src="https://github.com/PradoJuanPablo/osticket-prereqs/assets/160810181/29b1ccab-4a34-4c70-99f9-0598663df4c4">

</p>
<p>
Now that we have logged into our machine, we must enable Internet Information Services (IIS). IIS is software that runs on servers and helps host websites and applications on the internet.
To get there we go to the Control Panel > Programs > Turn Windows Features On or Off > Check the box next to Internet Information Services > Expand and go to World Wide Web Services > Expand again and go to Application Development Features and click the box next to CGI

After all the boxes are checked, click "Ok" and it will begin to install IIS.

  <img width="719" alt="image" src="https://github.com/PradoJuanPablo/osticket-prereqs/assets/160810181/a6922dfe-c26f-4e4f-b7f5-de6de9729f85">

</p>
<p>
To test that it worked, go to you web browser and type "127.0.0.1" and it should return a page that says "Internet Information Services" 

</p>
<br />

<p>
<img width="721" alt="image" src="https://github.com/PradoJuanPablo/osticket-prereqs/assets/160810181/c9ba45e2-630a-4ae9-953f-defc9c5ea598">

</p>
<p
  
Now we have this installed, lets [download](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) the installations files needed for osTicket and HeidiSQL.

- From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

