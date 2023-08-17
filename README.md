<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

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
<h3 align="center">Create Virtual Machine in Azure</h3>
<br />
<p>

<h2>Installation Steps</h2>

1. The first step is to create a resource group within Azure.

![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/587c74d8-1878-44d3-bab0-45eaac109e47)

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
4. 

<img width="1042" alt="image" src="https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/6aca310c-daf5-4d72-ad94-674a1d1f93d1">


![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/cc7ca959-244c-4c3d-a153-3c83105dfe23)

![image](https://github.com/CathyMorgan/osticket-prereqs/assets/107357582/f568f668-f300-44da-8c4a-d1b910c650a2)


