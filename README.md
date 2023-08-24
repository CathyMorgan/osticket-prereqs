<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

  

  <h2> Files You Need to Download</h2>

- ### [Download Now](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 📁




  
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

  <h2> Prerequisites </h2>

- Create a Virtual Machine in Azure
- Install osTicket v1.15.8
- Install HeidiSQL
- Install MySQL
- Install PHP
- install Microsoft Visual C++ Redistributable
  <h2>Steps</h2>
<h3 align="center">Create a Virtual Machine in Azure</h3>
<br />
<p>

<h2>Installation Steps</h2>

1. The first step is to create a resource group within Azure.

![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/587c74d8-1878-44d3-bab0-45eaac109e47)

<br />

![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/f49bec6a-59ae-4ebc-9850-7ac67c356c7c)

<br />

2. Create a Windows 10 Virtual Machine (VM), commonly with 2-4 Virtual CPUs. Enter a Username and password this can be whatever you choose, we will use this information to remote in from our main computer. Allow Azure to construct a new virtual Network (Vnet) while creating the Virtual Machine (VM):<p>

<img width="1323" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/2c0747bb-fe5d-40a6-8717-74231002b952">

![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/27846ccc-cfec-4ccd-a02d-ef94f25348a7) 

<br />

3. Open the remote desktop app on your computer and connect to your virtual machine within Azure using its ip address.

Remote desktop example on a Macbook computer.
   
<img width="1415" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/16505d70-4379-40fc-872b-fe5a4702e787">

</p>

Remote Desktop example on a Microsoft computer.

![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/080a8d31-7ee1-4b22-98dc-074110971e38)

<br />


<p>
4. We must now install and enable IIS in Windows. Enter "Control Panel" into your Search Bar > "Programmes" > "Turn Windows features on or off" > "OK" Scroll down until you reach "Internet Information Services (IIS)."


<img width="1042" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/6aca310c-daf5-4d72-ad94-674a1d1f93d1">



5. Click on "Internet Information Services" to expand it. Expand the "World Wide Web" tab. Next, expand the "Application Developer" tab. Check the "CGI*" button and press Ok.

<img width="1131" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/928733f5-6602-47c6-b7d5-2eb90d1b588d">

Enabling CGI is necessary to download the PHP Manager, which is a back-end web programming language that allows osTicket to function smoothly on a web browser.





<h3 align="center">Install PHP Manager</h3>
<br />
<p>
  
  <br />

To install the PHP Manager and download the required files, follow these steps:

- Begin by downloading the PHP Manager file.
- During the installation process, make sure to agree with all the terms and conditions.
- Once the installation is finished, you will have successfully downloaded the PHP Manager into your operating system.

<img width="1375" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/9d12451f-309c-4cc1-8e4e-252608ed3d33">

<h3 align="center">Install Rewrite Module</h3>
<br />
<p>

- Obtain the Rewrite Module file from a reliable source or the official website.
- Double-click on the downloaded file to begin the installation process.
- Follow the on-screen prompts and agree to the terms and conditions.
- Once the installation is complete, the Rewrite Module will be installed on your computer.

    
 ![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/cc7ca959-244c-4c3d-a153-3c83105dfe23)

<h3 align="center">Create Directory C:\PHP</h3>
<br />
<p>
  
- Open File Explorer.
- Type "C:\" in the search bar and press Enter.
- Right-click on an empty area within the "C:\" drive and select "New" > "Folder".
- Name the folder "PH".
- Download the file "php-7.3.8-nts-Win32-VC15-x86.zip" from the specified source.
- Locate the downloaded file.
- Right-click on the "php-7.3.8-nts-Win32-VC15-x86.zip" file.
- From the context menu, select "Extract All".
- In the "Extract Compressed (Zipped) Folders" window, ensure that the "Destination" field shows the path "C:\PH".
- Click the "Extract" button to extract the PHP files to the "C:\PH" folder.

These steps should allow you to create the "C:\PH" directory and extract the PHP file successfully.


![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/8ee398fa-e2b9-44dd-9d80-9da37dc9ca20)


<img width="583" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/1a6003cd-57c4-46da-9bde-739b23aac0ff">

<img width="1431" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/4b2285be-9ceb-4b58-8e1a-54f3c9acb0c5">


<h3 align="center">VC Redist Download</h3>

- Visit the Microsoft Download Center website.
- Search for "Visual C++ Redistributable Packages for Visual Studio".
- Choose the appropriate version (32-bit or 64-bit) and language. (Please also note I have attached all downloadable files for this project at the top of the page)
  
- Download the file.
- Locate and run the installer.
- Follow the on-screen instructions to install.
- Accept the terms and agreements if you agree.
- Complete the installation by following any remaining prompts.


![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/9d08a9a9-b860-47e2-909b-22fc95c58a1e)





  <h3 align="center">VC Download MySQL</h3>

Download and install MySQL and agree to all permissions. You will then create a username and password for the platform you will use to store the information used in osTicket.  

![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/c3a003ae-23e7-49f9-ba6c-11ffde076158)

<img width="853" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/46d87612-40a2-4002-ad1f-d185166c9900">
  

  <h3 align="center">Install osTicket v1.15.8

<img width="768" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/e9dc50cb-94af-427e-8f08-18f3349fd69e">
 
<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/3d83f436-f339-4cd1-a45c-d184734f4a05">

<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/63dea9ea-d4e4-44b3-85d4-372dac3dc87c">

<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/6184d9a5-e396-47e0-9239-f3d8379330fa">

  <h3 align="center">Reload IIS (Open IIS, Stop and Start the server)

<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/52320c96-489e-490e-a5ee-c1a16e2881e0">

<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/13872d1f-6112-470c-bf14-3ef34f0f945e">
  
  <h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled

<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/64ba8d71-9fd2-437b-b420-987a520c26a0">

Go to IIS> Sights> Default> osTicket and double-click PHP Manager:


![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/fede5169-a9fc-477e-b6ad-5ac7e660964c)



Click "Enable or disable relevant extensions".



Please enable the following PHP extensions:

 
(php_imap.dll)
(php_intl.dll)
(php_opcache.dll)


  <h3 align="center">Refesh osTicket (notice changes).


<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/2b88feed-4ad9-45aa-9ee0-ff111e9af3b1">


<h3 align="center"> Rename 



From C:\inetpub\wwwroot\Ticket\include\ost-sampleconfig.php.

To: C\inetpub\wwwroot\osTicket\include\ost-config.php:

 <img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/d5f6f3b7-aed9-48f9-9137-139d158409c0">

 
<h3 align="center">Assign Relevant Permissions: ost- config.php

<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/e7d6c792-c9f7-4739-9a1f-93cbc89f4bdd">

Everyone given permission (New Permissions> Everyone> All).



![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/3cfc8186-1e07-4f27-ac22-1eae2d2818e2)



<h3 align="center">Continue Setting up osTicket 

<img width="505" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/052cf289-c567-4ab6-ac47-897410460edb">



<h3 align="center">Download and Install HeidiSQL

  <img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/45a51baa-8ec5-4b82-a36e-2ed0b3ec14e4">

Create a new session and input root/Password then connect:

<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/3e178a65-5424-4c9e-8bf5-db749307787b">

Create a database called osTicket:

<img width="688" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/ea956916-c5df-4c0c-88f7-be7e61313977">


<h3 align="center"> Finish setting up osTicket in the browser

MySQL Database (osTicket), Username (root) and the password chosen.


<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/84bb8818-405c-403e-ac4c-bd736fef5fa8">

osTicket installed.

<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/a446334f-7afc-4b74-92cf-0a0ad38c8784">

<h3 align="center">Clean Up

Delete C:\inetpub\wwwroot\osTicket\setup:

![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/5112d074-53bb-40e7-9fc0-b28391451d74)

Set Permission to read-only.

<img width="1440" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/9f0e6b79-b979-48f7-a567-89ccac808673">

![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/786106a8-5428-48c5-b374-32a312033031)
  
<h3 align="center"> Login to osTicket Admin Panel (http://localhost/osTicket/scp/login.php)




  
<img width="700" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/477e44e8-48fa-4580-8673-8b911ce7cbb4">



<h3 align="center"> Installation of osTicket Completed.
