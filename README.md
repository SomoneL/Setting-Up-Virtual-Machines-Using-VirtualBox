# Setting Up Virtual Machines Using VirtualBox
<h2>Description</h2>
In this project, I will demonstrate how to set up two virtual machines (VMs) using Oracle VirtualBox: one running Windows 10 (client) and the other running Windows Server 2019. VirtualBox allows users to run multiple operating systems on a single physical machine, which is an essential tool for testing, development, and IT support purposes.
<br />
<h2>Step 1: Download and Install VirtualBox </h2>
<ol>
   <li>Go to the VirtualBox Website:</li>
   <ul>
      <li>Navigate to the VirtualBox Downloads Page: https://www.virtualbox.org/wiki/Downloads</li>
      <li>Choose the version that matches your host operating system (Windows, macOS, or Linux).</li>
   </ul>
   <li>Download VirtualBox </li>
   <ul>
      <li>Click the link to download the VirtualBox installer for your operating system.</li>
   </ul>
   <li>Install VirtualBox</li>
   <ul>
      <li>Open the downloaded installer and follow the prompts to install VirtualBox.</li>
   </ul>
   <ul>
      <li>Leave the default options selected unless you require custom settings.</li>
   </ul>
</ol>
<h2>Step 2: Download Windows 10 and Windows Server 2019 ISO Files</h2>
<ol>
   <li>Go to Microsoft's Website to download both ISOs:</li>
   <ul>
      <li>The link to the Windows 10 iso: https://www.microsoft.com/en-us/software-download/windows10</li>
   </ul>
   <ul>
      <li>The link to the Windows 2019 iso: https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019</li>
   </ul>
   <li>Rename your ISO files to something you can recognize:</li>
   <ul>
      <li>The initial download with be a bunch of numbers instead of the file names.</li>
   </ul>
   <ul>
         <br/>
      </li>
   </ul>
   <ul><li>Original Download</li></ul>
   <br/>
   <img src="https://imgur.com/7KT2ggW.png" height="40%" width="40%" alt="script"/>
   <br/>
   <ul><li>Renamed Download</li></ul>
   <br/>
   <img src="https://imgur.com/rVoTuWD.png" height="40%" width="40%" alt="script"/>
   <br/>
</ol>
<h2>Step 3: Create a New Virtual Machine (Windows 10)</h2>
<ol>
<li>Open VirtualBox: </li>
<ul>
<li>Launch VirtualBox from your desktop or start menu.</li>
</ul>
<li>Create a New VM:</li>
<ul>
<li>Click New to create a new virtual machine.</li>
</ul>
<li>Name Your VM:</li>
<ul>
<li>Enter a name (e.g., "Windows 10 VM").</li>
</ul>
<ul>
<li>Select the Type as Microsoft Windows and the Version as Windows 10 (64-bit).</li>
</ul>
<ul>
<li>Click Next.</li>
</ul>
   <br/>
   <img src="https://imgur.com/Pgy1AUt.png" height="40%" width="40%" alt="script"/>
   <br/>
</li></ul>
<li>Allocate Memory (RAM):</li>
<ul>
<li>Select how much RAM you want to allocate. For Windows 10, at least 2 GB (2048 MB) is recommended. For processor amount, if you have a PC with good RAM, use atleast 4 processors to aid in increased VM speed. If you are unsure you can just use 1 processor and click Next.</li>
</ul>
<br/>
<img src="https://imgur.com/5nfIONS.png" height="40%" width="40%" alt="script"/>
<br/>   
<li>Create a Virtual Hard Disk:</li>
<ul>
<li>Choose Create a virtual hard disk now and click Create.</li>
</ul>
<li>Select Storage:</li>
<ul>
<li>Choose Dynamically allocated so that the disk grows as needed and click Next.</li>
</ul>
<li>Set Disk Size:</li>
<ul>
<li>Allocate at least 50 GB for Windows 10 and click Create.</li>
</ul>
<br/>
<img src="https://imgur.com/Z8iJoAq.png" height="40%" width="40%" alt="script"/>
<br/>    
</ol>
<h2>Step 4: Install Windows 10 </h2>
<ol>
   <li>Mount the Windows 10 ISO:</li>
   <ul>
      <li>Select your newly created Windows 10 VM and click Start.</li>
   </ul>
   <ul>
      <li>A window will prompt you to select a start-up disk. Click the folder icon and navigate to the Windows 10 ISO you downloaded.</li>
   </ul>
   <ul>
      <li>Select the ISO and Click "Mount and Retry Boot"</li>
   </ul>
   <br/>
   <img src="https://imgur.com/bdcVL5v.png" height="40%" width="40%" alt="script"/>
   <br/>
   <li>Begin the Windows Installation:</li>
   </ul>
   <ul>
      <li>Follow the on-screen prompts to install Windows 10.</li>
   </ul>
   <ul>
      <li>Which type of installation do you want? - "Custom: Install Windows only (advanced)"</li>
   </ul>
    <ul>
      <li>Where do you want to install Windows? - Select "Drive 0 Unallocated Space" - Click Next.</li>
   </ul>
   <ul>
      <li>Choose the appropriate settings, including language, time, and keyboard layout.</li>
   </ul>
   <img src="https://imgur.com/qnI6FeZ.png" height="30%" width="30%" alt="script"/>
   <li>Create a User:</li>
   <ul>
      <li>During installation, you'll be asked to create a username and password for the new Windows 10 instance.</li>
   </ul>
   <li>Complete Installation:</li>
   <ul>
      <li>After the installation finishes, restart the VM. You’ll have a working instance of Windows 10.</li>
   </ul>
</ol>
<h2>Step 5: Create a New Virtual Machine (Windows Server 2019)</h2>
<ol>
   <li>Open VirtualBox: </li>
   <ul>
      <li>Launch VirtualBox from your desktop or start menu.</li>
   </ul>
   <li>Create a New VM:</li>
   <ul>
      <li>In the VirtualBox Manager, click New again to create a second VM for Windows Server 2019.</li>
   </ul>
   <li>Name Your VM:</li>
   <ul>
      <li>Name the VM (e.g., "Windows Server 2019 VM").</li>
   </ul>
   <ul>
      <li>Select Microsoft Windows as the type and Windows 2019 (64-bit) as the version.</li>
   </ul>
   <ul>
      <li>Click Next.</li>
   </ul>
      <img src="https://imgur.com/r9rOuCo.png" height="30%" width="30%" alt="script"/></ol>
   </li></ul>
   <li>Allocate Memory (RAM):</li>
   <ul>
      <li>Select how much RAM you want to allocate. For Windows Server 2019, at least 4 GB (4096 MB) is recommended. For processor amount, if you have a PC with good RAM, use atleast 4 processors to aid in increased VM speed. If you are unsure you can just use 1 processor and click Next.</li>
   </ul>
<br/>
   <img src="https://imgur.com/z4P9Aga.png" height="40%" width="40%" alt="script"/>
<br/>
   <li>Create a Virtual Hard Disk:</li>
   <ul>
      <li>Choose Create a virtual hard disk now and click Create.</li>
   </ul>
   <li>Select Storage:</li>
   <ul>
      <li>Choose Dynamically allocated so that the disk grows as needed and click Next.</li>
   </ul>
   <li>Set Disk Size:</li>
   <ul>
      <li>Allocate at least 60 GB for Windows Server 2019 and click Create.</li>
   </ul>
<br/>
   <img src="https://imgur.com/O2iLUGR.png" height="40%" width="40%" alt="script"/>
<br/> 
</ol>
<h2>Step 6: Install Windows Server 2019</h2>
<ol>
   <li>Mount the Windows Server 2019 ISO:</li>
   <ul>
      <li>Select the new Windows Server 2019 VM and click Start.</li>
   </ul>
   <ul>
      <li>A window will prompt you to select a start-up disk. Click the folder icon and navigate to the Windows Server 2019 ISO you downloaded.
Select the ISO and Click "Mount and Retry Boot"</li>
   </ul>
   <br/>
   <img src="https://imgur.com/9tjz8Oa.png" height="40%" width="40%" alt="script"/>
   <br/>
   <li>Begin Windows Server Installation:</li>
   <ul>
      <li>Follow the on-screen instructions to install Windows Server 2019.</li>
   </ul>
    <ul>
      <li>Select Windows Server 2019 Standard (Desktop Experience) as the installation type.</li>
   </ul>
   <ul>
      <li>Choose the appropriate options for language, time, and keyboard input.</li>
   </ul>
<li>Set Administrator Account:</li>
    <ul>
      <li>Set up a password for the Administrator account.</li>
   </ul>
<li>Complete Installation:</li>
    <ul>
      <li>After installation is complete, restart the virtual machine.</li>
   </ul>
   </li></ul>
</ol>
<h2>Step 7: Finalize the VMs</h2>
<ol>
   <li>Install Guest Additions (Optional):</li>
   <ul>
      <li>For better performance, you can install Guest Additions by clicking Devices > Insert Guest Additions CD Image in VirtualBox, then following the installation prompts in each VM.</li>
   </ul>
   <li>Update Windows:</li>
   <ul>
      <li>Log into both VMs and run Windows Update to make sure your system is up-to-date.</li>
   </ul>
    <ul>
      <li>For Windows 10, open Settings > Update & Security > Windows Update.</li>
   </ul>
    <ul>
      <li>For Windows Server 2019, open Server Manager > Local Server > Windows Update.</li>
   </ul>
</ol>
   <h2>Step 8: Test Connectivity Between VMs (Optional)</h2>
<ol>
   <li>Configure Network Settings:</li>
   <ul>
      <li>You can set up the network settings in VirtualBox to allow the two VMs to communicate with each other but first you will have to create a Host-Only Network in VirtualBox. At the top of the VirtualBox window, click File > Tools > Network Manager. In the tools window, click Create. If one has not already been created, a new one will be. Make sure your 'Adapter' and 'DHCP Server' Properties match these:</li>
   </ul>
   <br/>
   <img src="https://imgur.com/qm1CPuL.png" height="40%" width="40%" alt="script"/>
   <br/>
   <br/>
   <img src="https://imgur.com/0jNkto4.png" height="40%" width="40%" alt="script"/>
   <br/>
   <li>Set Network Settings:</li>
   <ul>
      <li>You can set up the network settings in VirtualBox to allow the two VMs to communicate with each other. Click on one VM at a time and go to Settings > Network for each VM and check "Enable Network Adapter", Attached to: Host-only Adapter, select the available or created adapter of your choice but make sure both VMs have the exact same Network Settings.</li>
   </ul>
   <br/>
   <img src="https://imgur.com/b84H3JZ.png" height="40%" width="40%" alt="script"/>
   <br/>
   <li>Ping Between VMs: </li>
   <ul>
      <li>Open Command Prompt on each VM and ping the other VM to ensure network connectivity. Use the following command: 'ipconfig' to grab each VMs individual IP. While logged into Windows 10 VM in command prompt, run 'ping -your server 2019 VM IP-'. You should receive a reply indicating the two VMs can communicate over the same network. </li>
   </ul>
  <br></br> 
<ul>
   <li>Running ipconfig on Windows 10 VM. The IP address for this VM is: 192.168.56.105 </li>
   </ul>
   <br/>
   <img src="https://imgur.com/7ho0NxL.png" height="40%" width="40%" alt="script"/>
   <br/>
   <ul>
   <li>Running ipconfig on Windows Server 2019 VM. The IP address for this VM is: 192.168.56.106 </li>
   </ul>
   <br/>
   <img src="https://imgur.com/Rg2asRK.png" height="40%" width="40%" alt="script"/>
   <br/>
   <li>Pinging the Server 2019 VM from the Windows 10 VM receiving a successful reply indicating network communication. </li>
   </ul>
   <br/>
   <img src="https://imgur.com/GV8iJnd.png" height="40%" width="40%" alt="script"/>
   <br/>
   <ul>
   <li>Pinging the Windows 10 VM from the Server 2019 VM receiving a successful reply indicating network communication. </li>
   </ul>
   <br/>
   <img src="https://imgur.com/QsjruBy.png" height="40%" width="40%" alt="script"/>
   <br/>
      <li>TIP: Be sure to turn off Windows Firewall settings in both VMs so they can ping eachother.</li>
   </ul>
   <br/>
   <img src="https://imgur.com/zwY7EX8.png" height="40%" width="40%" alt="script"/>
   <br/>
    
</ol>
<h2>Step 9: Conclusion</h2>
In this project, we have successfully set up virtual machines for both Windows 10 and Windows Server 2019 using VirtualBox. These VMs can be used to simulate various IT environments, conduct tests, or practice system administration tasks. This project is a great way to demonstrate your virtualization and IT skills in your e-portfolio.    
<ol></ol>
