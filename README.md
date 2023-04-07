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
Next step is download and install VC_redist.x86.exe.download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)



  ![image](https://user-images.githubusercontent.com/129979322/230625274-5667d2ed-d8b6-4e17-ac24-6fdb3c95d43a.png)
  ![image](https://user-images.githubusercontent.com/129979322/230628877-5ea583fc-fd4c-4bb1-ab33-9c73a295fff3.png)
  ![image](https://user-images.githubusercontent.com/129979322/230629140-01aa9978-5fba-433e-a1c0-4b5ae81bbf25.png)
  ![image](https://user-images.githubusercontent.com/129979322/230629210-6984446b-96a9-4544-915f-83c730cf57fc.png)
  ![image](https://user-images.githubusercontent.com/129979322/230640048-405eefec-e2a7-4a56-ac49-b562a98e37f1.png)
![image](https://user-images.githubusercontent.com/129979322/230639772-0680595b-f143-4e76-a2af-37cb3f60af11.png)
  ![image](https://user-images.githubusercontent.com/129979322/230641158-dc915bcf-cda3-428f-a2a7-9d33b8258248.png)
  ![image](https://user-images.githubusercontent.com/129979322/230641541-c7ce8b8a-a88e-414e-bc18-885ba7a6e538.png)
  ![image](https://user-images.githubusercontent.com/129979322/230641850-6a8a1e04-66a2-4403-92a1-22ace505ab5e.png)
  ![image](https://user-images.githubusercontent.com/129979322/230642380-ca1a9b30-0c17-4683-af46-0e6fd0c77611.png)
![image](https://user-images.githubusercontent.com/129979322/230643258-018bb897-9a1d-4735-b6f7-a61c42673621.png)
  ![image](https://user-images.githubusercontent.com/129979322/230643426-96cff922-3a69-45fc-975f-13464ac5ce44.png)
![image](https://user-images.githubusercontent.com/129979322/230643912-6af50e34-dc3f-4a6b-9d57-ef9bc57214e8.png)
  ![image](https://user-images.githubusercontent.com/129979322/230646813-6f2fd16b-7053-4931-b28b-9e383b23f267.png)
  ![image](https://user-images.githubusercontent.com/129979322/230647422-fc347443-c9d3-4c66-b9c1-82ebcbbf0a01.png)
  
![image](https://user-images.githubusercontent.com/129979322/230648402-a69f73c0-aac3-44cc-a190-f80f602e3419.png)
Always make sure you reload IIS by clicking on your local host ever"VM-OsTicket"and click"restart"under Manage server.
  Now lets go ahead and Install osTicket v1.15.8 download osTicket.Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”.Go to sites -> Default -> osTicket
On the right, click “Browse *:80”



![image](https://user-images.githubusercontent.com/129979322/230650924-a31a3e52-501a-401b-8359-987659b56f90.png)
  ![image](https://user-images.githubusercontent.com/129979322/230651400-19383d9f-5bfa-47a3-8f0c-bdbfad8ce38a.png)
  ![image](https://user-images.githubusercontent.com/129979322/230651691-f75854b5-9c0b-4bd6-94fe-0fa040750b62.png)
  ![image](https://user-images.githubusercontent.com/129979322/230651932-7ad72bb5-5b63-4931-a0b9-2847c42977ee.png)
  ![image](https://user-images.githubusercontent.com/129979322/230652679-43f884d9-b6e6-4a67-8c9f-1ddbbc4998f9.png)










  





<br />

<p>

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
