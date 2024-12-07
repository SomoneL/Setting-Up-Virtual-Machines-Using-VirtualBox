# Setting Up Virtual Machines Using VirtualBox

<h2>Description</h2>
In this project, I will demonstrate how to set up two virtual machines (VMs) using Oracle VirtualBox: one running Windows 10 (client) and the other running Windows Server 2019. VirtualBox allows users to run multiple operating systems on a single physical machine, which is an essential tool for testing, development, and IT support purposes.
<br />
<h2>Step 1: Download and Install VirtualBox </h2>
<ol>
   <li>Go to the VirtualBox Website:</li>
   <ul>
      <li>Navigate to the VirtualBox Downloads Page.</li>
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
      <li>Add pic for comparison. 
         <br/>
      </li>
      
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
</li></ul>
<li>Allocate Memory (RAM):</li>
<ul>
<li>Select how much RAM you want to allocate. For Windows 10, at least 2 GB (2048 MB) is recommended and click Next.</li>
</ul>
<ul>
<li>In System Properties, click Change and join the computer to your new domain by entering the domain name (e.g., yourdomain.local).</li>
</ul>
<ul>
<li>You’ll need to provide the Administrator account credentials for the domain.</li>
</ul>
</li></ul>
</ol>
<h2>Step 4: Install Group Policy Management </h2>
<ol>
   <li>Install Group Policy Management Feature:</li>
   <ul>
      <li>Open Server Manager and click Add roles and features.</li>
   </ul>
   <ul>
      <li>On the Features screen, check the box for Group Policy Management.</li>
   </ul>
   <ul>
      <li>Follow the prompts to complete the installation.</li>
   </ul>
   <ul>
      <li>Create groups for specific roles (e.g., admin, user, guest) by running the following code:</li>
   </ul>
   <img src="https://i.imgur.com/RXI5kjZ.png" height="30%" width="30%" alt="script"/>
   <br/>
   <li>Assign Permissions to Groups</li>
   </ul>
   <ul>
      <li>Use the chmod and chown commands to set directory permissions.</li>
   </ul>
   <img src="https://i.imgur.com/9c335UK.png" height="30%" width="30%" alt="script"/>
   <li>Enforce Access Control</li>
   <ul>
      <li>Verify permissions by switching to different users and testing to see if you can access the created directories.</li>
   </ul>
   <img src="https://i.imgur.com/pY3M8ON.png" height="30%" width="30%" alt="script"/>
</ol>



<h2>Step 5: Create and Apply Group Policies</h2>
<ol>
   <li>Open Group Policy Management:</li>
   <ul>
      <li>In Server Manager, click Tools and select Group Policy Management.</li>
   </ul>
   <li>Create a New Group Policy Object (GPO):</li>
   <ul>
      <li>In the Group Policy Management window, expand your domain (e.g., yourdomain.local).</li>
   </ul>
   <ul>
      <li>Right-click Group Policy Objects and select New.
   </ul>
   <ul>
      <li>Name the new GPO (e.g., Security Policy for Users).</li>
   </ul>
   <li>Edit the Group Policy:</li>
   <ul>
   <li>Right-click your new GPO and select Edit.</li>
   </ul>
    <ul>
   <li>The Group Policy Management Editor will open, allowing you to configure settings for users and computers.</li>
   </ul>
    <ul>
   <li>Examples of GPO settings:</li>
       <ul><li>Password Policy: Navigate to Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy to enforce password complexity and expiration.</li></ul>
       <ul><li>Software Restriction Policies: Use Computer Configuration > Policies > Windows Settings > Security Settings > Software Restriction Policies to control which software can run.</li></ul>
   </ul>



   
   <li>Link the GPO to an OU:</li>
   <ul>
   <li>In the Group Policy Management console, right-click on the OU where you want to apply the GPO (e.g., Users or Workstations).</li>
   </ul>
   <ul>
   <li>Select Link an Existing GPO and choose the GPO you just created.</li>
   </ul>
   <ul>
   </ul>
   <li>Test the Group Policy</li>
   <ul>
   <li>On the client computer (Windows 10), log in as a user that is part of the domain.</li>
   </ul>
   <ul>
   <li>Open Command Prompt and run the following command to update Group Policy: gpupdate /force</li>
   </ul>
   <ul>
   <li>Log off and log back in to see if the Group Policy settings have been applied.</li>
   </ul>
   <ul>
</ol>
<h2>Step 6: Documenting and Analyzing Your Results</h2>
<ol>
<li>Review the Group Policies:</li>
<ul>
<li>Go back to Group Policy Management to review which GPOs are linked to which OUs.</li>
</ul>
<ul>
<li>Ensure that the policies are correctly applied and functioning by testing on the client machines.</li>
</ul>
<br/>
<img src="https://i.imgur.com/tBsG67J.png" height="40%" width="40%" alt="script"/>
<br/>
<li>Troubleshooting:</li>
<ul>
<li>If the policies are not applying as expected, use Resultant Set of Policy (RSoP) or gpresult command to diagnose issues: gpresult /r</li>
</ul>
</li></ul>
   </ol>
<h2>Step 7: Conclusion</h2>
In this project, we have successfully set up virtual machines for both Windows 10 and Windows Server 2019 using VirtualBox. These VMs can be used to simulate various IT environments, conduct tests, or practice system administration tasks. This project is a great way to demonstrate your virtualization and IT skills in your e-portfolio.    
<ol>
</ol>
