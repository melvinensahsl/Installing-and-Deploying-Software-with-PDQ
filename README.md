<h1>Overview : Lab 10 Installing and Deploying Software with PDQ</h1>

This repository documents my home lab experience focused on **Installing and Deploying Software with PDQ** using **VirtualBox**. The lab involves setting up PDQ Deploy and PDQ Inventory to automate software deployment and manage system configurations across multiple virtual machines.

<h2>Objectives</h2>

- **Learn PDQ Deploy:** Explore how to automate the installation of software applications across multiple virtual machines.
- **Understand PDQ Inventory:** Set up and configure PDQ Inventory for system management and monitoring.
- **Network Configuration:** Use VirtualBox to simulate a network environment with different configurations and virtual machines.


<h2>Documentation</h2>

In this home lab, I will demonstrate how to install **PDQ Deploy**, create software packages, and deploy them. We will be primarily using **Windows Server 2022** for this lab environment. To begin, select **Devices** at the top of the VirtualBox menu, then choose **Insert Guest Additions CD Image**.




1. <p align="center">
   <img src="https://i.imgur.com/jTvKyom.png" height="80%" width="80%" alt="Disk Sanitization Steps 1"/>
   <br />
   <br />
</p>

Now lets open up File Explore and we see that CD Drive (D) VirtualBox Guest additions has been added. 

2. <p align="center">
   <img src="https://i.imgur.com/5IX53uv.png" height="80%" width="80%" alt="Disk Sanitization Steps 2"/>
   <br />
   <br />
</p>

Double-click on VirtualBox Guest and click Next until you reach the Install option. Select Install, then choose Reboot now and click Finish. Once you log back into your Windows Server 2022 account, right-click on the gray folder icon in the system tray and select Shared Folders Settings....

3. <p align="center">
   <img src="https://i.imgur.com/FmSmmMR.png" height="80%" width="80%" alt="Disk Sanitization Steps 3"/>
   <br />
   <br />
</p>

Next, click Add New Folder. Set the Folder Path to your Downloads folder, and create a new folder named "SimoTech Lab".

4. <p align="center">
   <img src="https://i.imgur.com/yhsXSvE.png" height="80%" width="80%" alt="Disk Sanitization Steps 4"/>
   <br />
   <br />
</p>

After selecting the SimoTech Lab folder, right-click on the disk icon at the bottom of the screen and select Remove Disk from Virtual Drive.

5. <p align="center">
   <img src="https://i.imgur.com/cyHiFJ3.png" height="80%" width="80%" alt="Disk Sanitization Steps 5"/>
   <br />
   <br />
</p>

Next we will go onto our web browser and go to https://www.pdq.com/downloads/ to download PDQ Deploy and PDQ Inventory. 

6. <p align="center">
   <img src="https://i.imgur.com/TpG1mvI.png" height="80%" width="80%" alt="Disk Sanitization Steps 6"/>
   <br />
   <br />
</p>

We can go back to our Windows Server 2022, open File Explorer, and see that the Z: drive for SimoTech Lab is available. Once we open it, we will find the PDQ Deploy applications. We can then drag the application onto the desktop and begin the installation.

7. <p align="center">
   <img src="https://i.imgur.com/0U2jUy4.png" height="80%" width="80%" alt="Disk Sanitization Steps 7"/>
   <br />
   <br />
</p>


8. <p align="center">
   <img src="https://i.imgur.com/XNh64Wu.png" height="80%" width="80%" alt="Disk Sanitization Steps 8"/>
   <br />
   <br />
</p>

Select “Next” → accept the terms → “Next” then install. 

9. <p align="center">
   <img src="https://i.imgur.com/CHotNF1.png" height="80%" width="80%" alt="Disk Sanitization Steps 9"/>
   <br />
   <br />
</p>

Once the installation is finished, we can launch the application. Next we sign into our Administrator credentials. 

10. <p align="center">
    <img src="https://i.imgur.com/o1bNzkx.png" height="80%" width="80%" alt="Disk Sanitization Steps 10"/>
    <br />
    <br />
</p>

Now that PDQ Deploy is ready, let's re-enable our internet connection. To do this, we need to go to Devices → Network → Network Settings, and change the setting to NAT. Then, open Control Panel → View Network Status and Tasks, and click on Change Adapter Settings. Right-click on Ethernet and select Properties. Next, double-click on Internet Protocol Version 4, and set it to Obtain an IP address automatically.

11. <p align="center">
    <img src="https://i.imgur.com/wBuHbB2.png" height="80%" width="80%" alt="Disk Sanitization Steps 11"/>
    <br />
    <br />
</p>

Our internet should now be active. To verify, we can open Command Prompt and ping google.com. Additionally, the internet icon on the bottom right of the screen should be available, indicating a successful connection.


12. <p align="center">
    <img src="https://i.imgur.com/W9FTCUh.png" height="80%" width="80%" alt="Disk Sanitization Steps 12"/>
    <br />
    <br />
</p>



13. <p align="center">
    <img src="https://i.imgur.com/eyJQlim.png" height="80%" width="80%" alt="Disk Sanitization Steps 13"/>
    <br />
    <br />
</p>

Now, let's go back to PDQ Deploy and select "Extend" to activate the inactive subscription.

14. <p align="center">
    <img src="https://i.imgur.com/Hbhgtlq.png" height="80%" width="80%" alt="Disk Sanitization Steps 14"/>
    <br />
    <br />
</p>

Extending the subscription will grant us a free trial of the Enterprise version, which allows access to all the available packages. We will need to enter our information and provide an email address. Once that's completed, we can start deploying packages using PDQ Deploy. Let's proceed by deploying Mozilla Firefox.

15. <p align="center">
    <img src="https://i.imgur.com/EBu7lDX.png" height="80%" width="80%" alt="Disk Sanitization Steps 15"/>
    <br />
    <br />
</p>

Double-click on the Mozilla Firefox package, and it will automatically start downloading. Once completed, it will appear in the Packages section.

16. <p align="center">
    <img src="https://i.imgur.com/JxlPMTo.png" height="80%" width="80%" alt="Disk Sanitization Steps 16"/>
    <br />
    <br />
</p>

Right click on Mozilla Firefox and select “Deploy once” 

17. <p align="center">
    <img src="https://i.imgur.com/lE7SlIy.png" height="80%" width="80%" alt="Disk Sanitization Steps 17"/>
    <br />
    <br />
</p>

Then select “Choose targets” → “Active Directory” → “Computers” 

18. <p align="center">
    <img src="https://i.imgur.com/5aomnNo.png" height="80%" width="80%" alt="Disk Sanitization Steps 18"/>
    <br />
    <br />
</p>

Then select “Server2022” as our target then select “OK”.

19. <p align="center">
    <img src="https://i.imgur.com/axv59iA.png" height="80%" width="80%" alt="Disk Sanitization Steps 19"/>
    <br />
    <br />
</p>

Select “Deploy Now”.

20. <p align="center">
    <img src="https://i.imgur.com/vrlj87g.png" height="80%" width="80%" alt="Disk Sanitization Steps 20"/>
    <br />
    <br />
</p>

We have officially deploy Mozilla Firefox, the deploy worked perfectly and we can see that Firefox is installed onto our desktop. 

21. <p align="center">
    <img src="https://i.imgur.com/FcXvXIv.png" height="80%" width="80%" alt="Disk Sanitization Steps 21"/>
    <br />
    <br />
</p>

Congratulations! We have successfully installed and set up **PDQ Deploy**, created and deployed software packages.

Now, let's switch back to a static IP. Open **Control Panel** and navigate to **View Network Status and Tasks** → **Change Adapter Settings**. Right-click on the network connection (**Ethernet**) and select **Properties** to begin configuring the network settings.

Enter the previously configured static IP settings:

- **IP Address:** 12.1.10.4
- **Subnet Mask:** 255.0.0.0
- **Default Gateway:** 12.1.10.1
- **Preferred DNS Server:** 12.1.10.2
- **Alternate DNS Server:** 12.1.10.1

Click **OK** to apply the settings.

 👉 [Next Lab 11 : PDQ Inventory: Hardware and Software Reporting](https://github.com/melvinensahsl/PDQ-Inventory-Hardware-and-Software-Reporting/tree/main)
