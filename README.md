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

- Azure Virtual Machine
- OsTicket installation files
- Heidi SQl

We are going to start by creating a Virtual Machine using Microsoft azure portal.We will be using a VM which is a remote computer that helps to protect our physichal machine just in case something goes wrong. Create a resource group name it "OsTicket" and then i will go ahead create a VM with 2-4 CPUs as shown in the example below.
![image](https://user-images.githubusercontent.com/129979322/230531734-0c98d33c-2545-4359-a736-59d828b33b73.png)<p>
![image](https://user-images.githubusercontent.com/129979322/230532636-ae0bab0d-ed7c-4c68-af2b-32a9210e1452.png)
![image](https://user-images.githubusercontent.com/129979322/230533674-a6ca3fb5-0714-44f6-bf7d-792a23ff2675.png)
![image](https://user-images.githubusercontent.com/129979322/230532930-ba36dde8-2641-46d6-8732-1355cb9ec1ff.png)
we are done creating the envirronement in Azure.
  
<p>
Next we are going to Remote desktop connect into our vm install a bunch of prerequisites as well as install OsTicket. Make sure we can log into it.

<br />

![image](https://user-images.githubusercontent.com/129979322/230535141-9d3f6a63-d0ff-47e2-8328-d8dba7c5975c.png)
![image](https://user-images.githubusercontent.com/129979322/230535575-e09be284-2813-452c-b45f-73f750f39a85.png)
![image](https://user-images.githubusercontent.com/129979322/230535770-ea02a294-2a23-4cc9-85c0-74f5db5fe407.png)
![image](https://user-images.githubusercontent.com/129979322/230535838-d9063489-cfd0-48ed-9a03-34a52ed890e4.png)

Done with our VM set up next we are going to install and enable ISS with CGI.ISS (Internet Information services)is a web server that allows the computer to serve up website.Because OsTicket runs out of a website.We need to set up and configure ISS in order to be able to run OsTicket.
Right click the start menu then choose run and type 'control" for control panel. Go with programs, click on turn windows features programs on and off
  
  ![image](https://user-images.githubusercontent.com/129979322/230538616-13772612-8f80-43ff-881d-c41def8e8965.png)
  ![image](https://user-images.githubusercontent.com/129979322/230538769-7bd7d427-a5b2-462a-853c-eced3da7fd0d.png)




<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
