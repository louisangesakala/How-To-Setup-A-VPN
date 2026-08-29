# Vitual Private Network (VPN)
<p align="center">
<img src="https://i.imgur.com/MntON5Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h1>VPN - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of using a VPN.<br />

<h2>Environments and Technologies Used</h2>

- A VPN (Proton VPN)
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>STEPS INCLUDED</h2>

- STEP 1 - Locate Local IP
- STEP 2 - Setting Up VM Using Azure
- STEP 3 - Locating IP Through VM (France)
- STEP 4 - Connecting to VPN Through VM
- STEP 5 - Locating IP Through VPN (Japan)

<h2>Installation Steps</h2>

<h3>STEP 1 - Locate your own personal IP address</h3> 

Locate your own personal IP address by going to "www.whatismyipaddress.com" which will be able to show you your local IP address. We will use this later as well. See EXAMPLE 1A below.

EXAMPLE 1A
<p>
<img src="https://i.imgur.com/pErPAKd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Next we will set up a virtual machine on Azure. 
  
</p>
<br />

<h3>STEP 2 - Setting up your Virtual Machine</h3>
Go to www.portal.azure.com and find Virtual Machines. (Create a free account with $200 if you need to). See Example 2A looking at the Virtual Machine set up page. 

EXAMPLE 2A
<p>
<img src="https://i.imgur.com/0PTOa7f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Creating the Virtual Machine. 
</p>
<p>For the purpose of this project, we will name our Virtual Machine (VM) as “VPN-France”, and the new Ressource Group as "RSG-France".</p>
<p>Select France Central for the Region.</p>
<p>Ensure the other items are selected as shown in EXAMPLE 2B screenshots below.</p>

EXAMPLE 2B
<p>
<img src="https://i.imgur.com/30mLba9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/yaSwvN5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<b>For the Username and Password you can create your custom information, just make a note of it.</b>
  
</p>
<br />

Check the "I confirm" box at the bottom of the page to confirm licensing, and then select “Review and Create”.<br>
Once it passes validation, select “Create” to complete the VM setup and laauch the deployment process. 
  
<p>
<img src="https://i.imgur.com/KbfiVNC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/WKUNqFG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<br />

NEXT: Once the deployment is completed, navigate to your list of Virtual Machines page, and click on the VM we just created.
<p>
  We find that the IP to the Virtual Machine is “172.189.57.196”. See EXAMPLE 2C
</p>

EXAMPLE 2C

<p>
<img src="https://i.imgur.com/hbTy2yB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


<h3>STEP 3 – Log Into the VM and Find IP Address</h3>
<p>
Now that we have set up the Virtual Machine, we will connect to it using “Remote Desktop Connection” on our laptop. If you don't have the app, download it on your desktop. EXAMPLE 3A shows what the app looks like using a Mac OS.</p>
<p>Click on the "+" icon, and "Add a PC".</p>
<p>Input the IP address for the VM that we located in EXAMPLE 2C and then use the credentials we set when creating the VM (see EXAMPLE 2B).</p>
  
</p>
<br />
EXAMPLE 3A
<p>
<img src="https://i.imgur.com/WcIUkLD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/1G88Aut.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>Once logged in, we will open the web browser, and look up www.whatismyipaddress.com from within the VM (EXAMPLE 3b).</p>
<br />

EXAMPLE 3B
<p>
<img src="https://i.imgur.com/NLl5g2m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>When looking at the IP address for this VM through www.whatismyipaddress.com, we see that this VM's location is France.</p>
  
</p>
<p>

<h3>STEP 4 – CONNECTING TO VPN (Free Version)</h3>

<p>Using the local computer go to protonvpn.com and create a free account.</p>
<p>Once your new account is set, copy the URL from the Proton VPN website (EXAMPLE 4A), and then paste the URL to the VM web browser.</p>

  
</p>
<br />

EXAMPLE 4A
<p>
<img src="https://i.imgur.com/orO2O5y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<p>Once you have logged into your Proton VPN account from within the VM -> select “Downloads” and choose to download the “Windows” x64 version. </p>

<p>
<img src="https://i.imgur.com/YIUJKOQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/kBkqCrb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

  <p>Launch the Proton app installation file and follow the installation steps.  </p>
  <p>Uncheck the other services included in your plan, and only check the "create desktop shortcut" box. Click Install.  </p>

<p>
<img src="https://i.imgur.com/bKK2WVS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

 <p>Once the Proton VPN app is installed, we will log in using our credentials, and connect to the VPN through the app.</p>
 <p>Once logged in, we notice that the IP address shown from within the app is the same as our VM set IP address as opposed to our local computer's IP address.</p>

<br />

<p>
<img src="https://i.imgur.com/28PHTZQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/pUn2w7b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
There are two ways to connect to a VPN server from within the Proton VPN app:</p>
  
<p>-On the left hand side of the app, where you can select a specific country you want your new IP address to be.</p>
<p>-By clicking on the "Connect" button displayed on the app's home page as soon as you open the app, to be assigned a random IP address from anywhere. </p>
<br />

<p>
<img src="https://i.imgur.com/3QGEr7U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  In our case, we will click on the "Connect" button and let the VPN assign a new secured IP address to our VM. see Example 4B <p>  
</p>
<br />

EXAMPLE 4B
<p>
<img src="https://i.imgur.com/eDZ9IYc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <b> We note that our new IP address is 72.251.221.1 located in the United States in New York. </b>
</p>

<p>
Next, let's look at at IP address again using www.whatismyipaddress.com in the VM browser.
</p>
<p>
  Now that the VPN connection has assigned a New York IP address to our VM, WhatIsMyIPAddress.com reflects this change by showing that exact IP address and location. see EXAMPLE 4C
</p>
<br />

EXAMPLE 4C
<p>
<img src="https://i.imgur.com/BlkYMUO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Looking at this exercise we see that we have utilized 3 different IP addresses just from your local computer to connect to the internet:<br>
-Home(local computer) IP (Dallas, USA): 63.249.62.121<br>
-Virtual Machin IP (France): 172.189.57.196<br>
-Virtual Machin IP VPN (New York, USA): 72.251.221.1<br>

  
</p>
<br />
If you no longer need the VM, ensure to remove it from the Asure account for unwanted charges.

END OF TUTORIAL
