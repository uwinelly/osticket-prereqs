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

We are going to start by creating a Virtual Machine using Microsoft azure portal.
We will be using a VM which is a remote computer that helps to protect our physichal machine just in case something goes wrong. 
Create a resource group name it "OsTicket" and then i will go ahead create a VM with 2-4 CPUs as shown in the example below.

  ![image](https://user-images.githubusercontent.com/129979322/230531734-0c98d33c-2545-4359-a736-59d828b33b73.png)<p>
  ![image](https://user-images.githubusercontent.com/129979322/230532636-ae0bab0d-ed7c-4c68-af2b-32a9210e1452.png)
  ![image](https://user-images.githubusercontent.com/129979322/230533674-a6ca3fb5-0714-44f6-bf7d-792a23ff2675.png)
  ![image](https://user-images.githubusercontent.com/129979322/230532930-ba36dde8-2641-46d6-8732-1355cb9ec1ff.png)
  
We are done creating the environment in Azure.  
Next, we are going to Remote desktop connect into our VM.Install a bunch of prerequisites as well as OsTicket making sure we can log into it.

  ![image](https://user-images.githubusercontent.com/129979322/230535141-9d3f6a63-d0ff-47e2-8328-d8dba7c5975c.png)
  
Simply open remote desktop connection and use the public IPv address to connect to your VM.Go ahead and login with the username and password you used while creating your VM.
  
  ![image](https://user-images.githubusercontent.com/129979322/230535575-e09be284-2813-452c-b45f-73f750f39a85.png)
  ![image](https://user-images.githubusercontent.com/129979322/230535770-ea02a294-2a23-4cc9-85c0-74f5db5fe407.png)
  
Click yes to connect anyway.
  
  ![image](https://user-images.githubusercontent.com/129979322/230535838-d9063489-cfd0-48ed-9a03-34a52ed890e4.png)

Done with our VM set up next we are going to install and enable ISS with CGI.
ISS (Internet Information services)is a web server that allows the computer to serve up website.
Because OsTicket runs out of a website.We need to set up and configure ISS in order to be able to run OsTicket.
Right click the start menu then choose run and type 'control" for control panel. Go with programs, click on turn windows features programs on and off.
Enable ISS,go ahead expand It then expand World web wide services, expand Application development features and enable CGI.CGI let us install php manager.
  
  ![image](https://user-images.githubusercontent.com/129979322/230538616-13772612-8f80-43ff-881d-c41def8e8965.png)
  ![image](https://user-images.githubusercontent.com/129979322/230538769-7bd7d427-a5b2-462a-853c-eced3da7fd0d.png)
  ![image](https://user-images.githubusercontent.com/129979322/230539426-90443585-c145-4310-9094-0a204cab4893.png)
  ![image](https://user-images.githubusercontent.com/129979322/230539154-154dc77c-d393-41f9-b34e-870a3b68d9d1.png)
  
If you wanted to make sure that your web serves are working,you can open a new browser and type in 127.0.0.1(whis is your local host or loopback).
You should be able to see the IIS page popup.If not double check your installation with CGI.
  
  ![image](https://user-images.githubusercontent.com/129979322/230539846-2fbacfed-32b0-4fe4-9b88-02f0341c3d4a.png)
  
Now,we are going to download PHP Manager for IIS and install rewrite module(rewrite_amd64_en-US.msi) which is one of the requirement for OsTicket to work.
  
  ![image](https://user-images.githubusercontent.com/129979322/230622665-fb685f8b-9681-489c-b53e-9c8b188accd2.png)
  ![image](https://user-images.githubusercontent.com/129979322/230622943-4a93830f-ec38-4a4a-a625-ac8a8180733d.png)
  ![image](https://user-images.githubusercontent.com/129979322/230625274-5667d2ed-d8b6-4e17-ac24-6fdb3c95d43a.png)
  
Next will be creating the directory C:\PHP on the root of C:\Drive and download php-7.3.8-nts-Win32-VC15-x86.zip) 
and unzip the contents into C:\PHP we have just created.


  ![image](https://user-images.githubusercontent.com/129979322/230628877-5ea583fc-fd4c-4bb1-ab33-9c73a295fff3.png)
  ![image](https://user-images.githubusercontent.com/129979322/230629140-01aa9978-5fba-433e-a1c0-4b5ae81bbf25.png)
  ![image](https://user-images.githubusercontent.com/129979322/230629210-6984446b-96a9-4544-915f-83c730cf57fc.png)
  
Next step is download and install VC_redist.x86.exe.
  
  ![image](https://user-images.githubusercontent.com/129979322/230640048-405eefec-e2a7-4a56-ac49-b562a98e37f1.png)
  ![image](https://user-images.githubusercontent.com/129979322/230639772-0680595b-f143-4e76-a2af-37cb3f60af11.png)

Then we will download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi).Make sure you choose "Typical" 
installation as well as "Launch the MySQL Instance Configuration Wizard" box checked off before you click "Finish".
  
  ![image](https://user-images.githubusercontent.com/129979322/230641158-dc915bcf-cda3-428f-a2a7-9d33b8258248.png)
  ![image](https://user-images.githubusercontent.com/129979322/230641541-c7ce8b8a-a88e-414e-bc18-885ba7a6e538.png)
  ![image](https://user-images.githubusercontent.com/129979322/230641850-6a8a1e04-66a2-4403-92a1-22ace505ab5e.png)
  
Go ahead and choose Standard configuration,click "next" and Password1 will be your new root password,click "Execute" and click "Finish"
  
  ![image](https://user-images.githubusercontent.com/129979322/230642380-ca1a9b30-0c17-4683-af46-0e6fd0c77611.png)
  ![image](https://user-images.githubusercontent.com/129979322/230643258-018bb897-9a1d-4735-b6f7-a61c42673621.png)
  ![image](https://user-images.githubusercontent.com/129979322/230643426-96cff922-3a69-45fc-975f-13464ac5ce44.png)
  
We will go ahead to the start menu, search for IIS right click it and then run it as an administrator.Double click on the "PHP Manager" icon and then click on register new PHP Version , browse to find your PHP Folder and look for your PHP-CGI file and open it click "ok".
  
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
  ![image](https://user-images.githubusercontent.com/129979322/230652929-87eec733-86f4-4d79-86fa-ef03745207af.png)
  
Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes
  
  ![image](https://user-images.githubusercontent.com/129979322/230655040-28f2e1bb-1e64-44f8-b491-787baaf13fa4.png)
  ![image](https://user-images.githubusercontent.com/129979322/230655267-ceb485bd-43a0-4742-9353-ad96c3fd2b37.png)
  ![image](https://user-images.githubusercontent.com/129979322/230655680-c43e94de-b901-4031-8f88-e6ab46066a14.png)
  ![image](https://user-images.githubusercontent.com/129979322/230657049-29c15ba0-f7f4-4689-a04a-814fd2cbac44.png)
  
  ![image](https://user-images.githubusercontent.com/129979322/230660067-8c4e0b78-bac9-4a8d-b0c9-eab24d380243.png)
  ![image](https://user-images.githubusercontent.com/129979322/230660338-cc525e3b-94fa-4d83-9660-1ff7d53da7c3.png)
  ![image](https://user-images.githubusercontent.com/129979322/230660612-f8793132-da1e-4b3f-a92f-52ad025e75fe.png)
  ![image](https://user-images.githubusercontent.com/129979322/230660831-81c744c7-52c0-4688-8ff7-ff8378b05cf6.png)
  ![image](https://user-images.githubusercontent.com/129979322/230661147-deb84aca-22a6-4664-b430-a139cb63e972.png)
  ![image](https://user-images.githubusercontent.com/129979322/230730226-9987d702-54c7-4ad8-b975-fa639964b6b9.png)
  
We are going to install Heidisql which allows us to connect to mySQL server we created above;and setup a database for OsTicket to use. Launch HeidiSql,open new for connection to the database.
  
  ![image](https://user-images.githubusercontent.com/129979322/230730833-b2496813-8775-4865-ab3d-cf74aeeb0d56.png)
  ![image](https://user-images.githubusercontent.com/129979322/230731074-ea388e5c-5ab1-41f7-a031-b83380a1b35d.png)
  ![image](https://user-images.githubusercontent.com/129979322/230732730-c9ebd915-1601-40d3-bc12-580389ef2aff.png)
  ![image](https://user-images.githubusercontent.com/129979322/230732863-49bb66e5-e00b-4865-9235-0ed6eb303ee3.png)

  ![image](https://user-images.githubusercontent.com/129979322/230733144-ee412047-5e9a-45f5-8606-21571dd059e6.png)
  ![image](https://user-images.githubusercontent.com/129979322/230733233-efcf1f3e-5201-40b4-b772-c6265fb5a195.png)
  ![image](https://user-images.githubusercontent.com/129979322/230733325-76eb16b5-fb49-4cf9-ae0a-00828a76c862.png)
  
  ![image](https://user-images.githubusercontent.com/129979322/230733458-234dcccc-07b7-4471-a736-71b8134c7909.png)
  ![image](https://user-images.githubusercontent.com/129979322/230733578-8d635e30-71cd-45d9-ba48-bc736c40f4cf.png)
  ![image](https://user-images.githubusercontent.com/129979322/230733611-2460f65a-4307-4891-88eb-3a08e26d6d6e.png)
  
Congratulations,now you can browse to your help desk login page: http://localhost/osTicket/scp/login.php
Next step is to delete the C:\inetpub\wwwroot\osTicket\setup and Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
  
  ![image](https://user-images.githubusercontent.com/129979322/230733963-e9b9e94f-9d49-40ed-8f71-0e2a93f74894.png)
  ![image](https://user-images.githubusercontent.com/129979322/230734036-02c962e9-8e66-4f52-8024-c0453d5264c0.png)
  ![image](https://user-images.githubusercontent.com/129979322/230734237-5ef42a53-ff24-4267-8b50-66400886af69.png)
  ![image](https://user-images.githubusercontent.com/129979322/230734671-0dd2ea89-5214-4cb7-9180-d73890a9c397.png)
  ![image](https://user-images.githubusercontent.com/129979322/230734802-87952c5c-b6f3-4e7f-b6d2-16aa3571cbe3.png)
  ![image](https://user-images.githubusercontent.com/129979322/230734903-38b68d6b-f4b5-4b03-bce1-9c72d286e921.png)
  ![image](https://user-images.githubusercontent.com/129979322/230735033-cea7e49c-1413-483e-a4e1-35e3b7045700.png)




























  













