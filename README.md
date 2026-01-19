<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this tutorial I will demonstrate the installation process of the open-source help desk ticketing system, osTicket.
During this tutorial I will be using specific prerequisite software versions listed below. Latest versions of the software can be used and is usually recommended.

<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket [(download)](https://osticket.com/download/)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

<h2>List of Prerequisites</h2>

- PHP Manager for IIS [(download)](https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10)
- Rewrite Module [(download)](https://download.microsoft.com/download/1/2/8/128E2E22-C1B9-44A4-BE2A-5859ED1D4592/rewrite_amd64_en-US.msi)
- PHP 7.3.8 (or latest version) [(download)](https://www.php.net/downloads.php)
- VC_redist.x86.exe [(download)](https://aka.ms/vc14/vc_redist.x64.exe)
- MySQL 5.5.62 (or latest version) [(download)](https://dev.mysql.com/downloads/installer/)

<h2>Installation Steps</h2>
<p>
First, let's enable IIS with Common Gateway Interface (CGI) in Windows.
</p>
<p>
Open the Control Panel (can be searched by typing in the search bar). Navigate to "Programs", then "Programs and Features", and click the text on the left side that says "Turn Windows features on or off". </br>
Navigate by scrolling down and find a box that says "Internet Information Services". Click on the box so it's selected. </br>
In the same window, click on the "+" symbol next to "Internet Information Services" and navigate to "World Wide Web Services", then "Application Development Features", and down to "CGI". Click on the box "CGI" so it's selected and click "OK". </br>
Please wait for Windows to apply the changes.
</p>
<p>
<img src="https://media.discordapp.net/attachments/1390632590247067770/1462593932687966426/image.png?ex=696ec23f&is=696d70bf&hm=042d4dbd6bcf4c1f41f6f5d89ca65d4ece7211c00277b85193fb012724332951" height="80%" width="80%"/>
</p>
<p>
Next we will start installing the list of prerequisites mentioned above.
</p>
<p>
Let's start with the first two prerequisites, "PHP Manager for IIS" and "Rewrite Module". Install the software by double clicking on them and navigate through the installation process. </br>
Once that is complete, we will create a new directory in the C drive called PFP (C:\PFP). Open File Explorer, navigate to the C drive. Right-click inside the window, go down to "New" and select "Folder". Name that folder "PHP".
</p>
<p>
<img src="https://cdn.discordapp.com/attachments/1390632590247067770/1462612343644098703/image.png?ex=696ed364&is=696d81e4&hm=ea2f553327adf5a93168098285d558643a6d9c4283c2d99f0e33d926309155fd" height="80%" width="80%"/>
</p>
<p>
edit
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%"/>
</p>
<p>
edit
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%"/>
</p>
<p>
edit
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%"/>
</p>
<p>
edit
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%"/>
</p>
<p>
edit
</p>

<br />
