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
Right click the start menu then choose run and type 'control" for control panel. Go with programs, click on turn windows features programs on and off.Enable ISS,go ahead expand It then expand World web wide services, expand Application development features and enable CGI.CGI let us install php manager.
  
  ![image](https://user-images.githubusercontent.com/129979322/230538616-13772612-8f80-43ff-881d-c41def8e8965.png)
  ![image](https://user-images.githubusercontent.com/129979322/230538769-7bd7d427-a5b2-462a-853c-eced3da7fd0d.png)
  ![image](https://user-images.githubusercontent.com/129979322/230539426-90443585-c145-4310-9094-0a204cab4893.png)
  ![image](https://user-images.githubusercontent.com/129979322/230539154-154dc77c-d393-41f9-b34e-870a3b68d9d1.png)
![image](https://user-images.githubusercontent.com/129979322/230539846-2fbacfed-32b0-4fe4-9b88-02f0341c3d4a.png)
  ![image](https://user-images.githubusercontent.com/129979322/230622665-fb685f8b-9681-489c-b53e-9c8b188accd2.png)
  ![image](https://user-images.githubusercontent.com/129979322/230622943-4a93830f-ec38-4a4a-a625-ac8a8180733d.png)


we are going to install rewrite module(rewrite_amd64_en-US.msi) which is one of the requirement for OsTicket to work.Next will be creating the directory C:\PHP on the root of C:\Drive and download php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP we have just created.
Next step is download and install VC_redist.x86.exe.


  ![image](https://user-images.githubusercontent.com/129979322/230625274-5667d2ed-d8b6-4e17-ac24-6fdb3c95d43a.png)
  ![image](https://user-images.githubusercontent.com/129979322/230628877-5ea583fc-fd4c-4bb1-ab33-9c73a295fff3.png)
  ![image](https://user-images.githubusercontent.com/129979322/230629140-01aa9978-5fba-433e-a1c0-4b5ae81bbf25.png)
  ![image](https://user-images.githubusercontent.com/129979322/230629210-6984446b-96a9-4544-915f-83c730cf57fc.png)
  ![image](https://user-images.githubusercontent.com/129979322/230640048-405eefec-e2a7-4a56-ac49-b562a98e37f1.png)
![image](https://user-images.githubusercontent.com/129979322/230639772-0680595b-f143-4e76-a2af-37cb3f60af11.png)
  





<br />

<p>

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
