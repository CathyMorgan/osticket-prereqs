<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

  

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

  

5. Click on "Internet Information Services" to expand it. Expand the "World Wide Web" tab. Next, expand the "Application Developer" tab. Check the "CGI*" button and press Ok.

Enabling CGI is necessary to download the PHP Manager, which is a back-end web programming language that allows osTicket to function smoothly on a web browser.


<img width="1042" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/6aca310c-daf5-4d72-ad94-674a1d1f93d1">

<br />


  
![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/f568f668-f300-44da-8c4a-d1b910c650a2)

<h3 align="center">Install PHP Manager</h3>
<br />
<p>
  
  <br />

To install the PHP Manager and download the required files, follow these steps:

- Begin by downloading the PHP Manager file.
- During the installation process, make sure to agree with all the terms and conditions.
- Once the installation is finished, you will have successfully downloaded the PHP Manager into your operating system.

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


<img width="528" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/adeee886-f94d-4f3e-8e62-6c30bbb582e8">

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
  

  <h3 align="center">Install osTicket v1.15.8
  

  <h3 align="center">Reload IIS (Open IIS, Stop and Start the server)
  

  <h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled
  

  <h3 align="center">Refresh the osTicket site in your browser, observe the changes
  

    <h3 align="center">Rename
    
    
    <h3 align="center">Assign Permissions: ost-config.php
    
    
    <h3 align="center">Continue Setting up osTicket in the browser (click Continue)
    

    <h3 align="center">Download and Install HeidiSQL
    
    
    <h3 align="center">Continue Setting up osTicket in the browser
    

     <h3 align="center">Clean up
     

    <h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)
    


  <h3 align="center">Installation of osTicket Completed.
    
    
    

  .
8.
