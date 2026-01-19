<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this tutorial I will demonstrate the installation process of the open-source help desk ticketing system, osTicket.
At the time of this demonstration I will have used specific software versions listed below (with included download links). Latest versions of the software can be used and is normally recommended.

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
First let's enable IIS with Common Gateway Interface (CGI) in Windows.
</p>
<p>
Open the Control Panel (can be searched by typing in the search bar). Navigate to "Programs", then "Programs and Features", and click the text on the left side that says "Turn Windows features on or off". Navigate by scrolling down and find a box that says "Internet Information Services". Click on the box so it's selected. In the same window, click on the "+" symbol next to "Internet Information Services" and navigate to "World Wide Web Services", then "Application Development Features", and down to "CGI". Click on the box "CGI" so it's selected and click "OK". Please wait for Windows to apply the changes.
</p>
<p>
<img src="https://cdn.discordapp.com/attachments/1390632590247067770/1462593932687966426/image.png?ex=696ec23f&is=696d70bf&hm=042d4dbd6bcf4c1f41f6f5d89ca65d4ece7211c00277b85193fb012724332951" height="60%" width="60%"/> <img src= "https://cdn.discordapp.com/attachments/1390632590247067770/1462594399107285022/image.png?ex=696ec2ae&is=696d712e&hm=2edf8e51ca32424bf23c0de2b4f74875ccbb25d36785f78d617f434ba35eb354" height="38%" width="38%"/>
</p>
<p>
Now we will start installing the list of prerequisites mentioned above.
</p>
<p>
Let's start with the first two prerequisites, PHP Manager for IIS and Rewrite Module. Double-click on them and navigate through the installation process. A prompt will pop up saying "Do you want to allow this app to make changes to your device?". Select "Yes" (You may see this prompt mulitple times throughout this entire tutorial, be sure to always select "Yes" when they pop up, otherwise you will have issues).
</p>
<p>
The next prerequisite PHP 7.3.8 (or latest version) is a ZIP file which needs to be extracted to the C: drive in a PFP folder (C:\PFP). To do this, navigate to the C: drive with File Explorer, right-click inside the window to show the options menu, then go down to "New" and select "Folder". Name that folder "PHP". The next prerequisite PHP 7.3.8 (or latest version) is a ZIP file which needs to be extracted to the PFP folder that was created. Simply right-click on the ZIP folder and select "Extract all". Change the destination where the files will be extracted to "C:\PHP" and click "Extract". Please wait for the extraction process to complete.
</p>
<p>
<img src="https://cdn.discordapp.com/attachments/1390632590247067770/1462612343644098703/image.png?ex=696ed364&is=696d81e4&hm=ea2f553327adf5a93168098285d558643a6d9c4283c2d99f0e33d926309155fd" height="35.5%" width="35.5%"/> <img src="https://cdn.discordapp.com/attachments/1390632590247067770/1462878331405074609/image.png?ex=696fcb1d&is=696e799d&hm=52fa0be493b22ddc65d827e6dd018ca2ede62baebc52c4278527c1eb194e7695" height="63%" width="63%"/>
</p>
<p>
The next prerequisites to install are VC_redist.x86.exe and MySQL 5.5.62 (or latest version).
</p>
<p>
Go through the installation process for VC_redist.x86.exe and wait for it to complete. When going through the MySQL installation process, I will do a "Typical" install. Have the box selected before you click on "Finish" to launch the MySQL Instance Configuration Wizard.
</p>
<p>
<img src="https://cdn.discordapp.com/attachments/1390632590247067770/1462886857409957918/image.png?ex=696fd30d&is=696e818d&hm=c82e713233cb625a6adb017c7723e5d74e9f341c1419033f0104664fc2e32ac1" height="30%" width="30%"/> <img src="https://cdn.discordapp.com/attachments/1390632590247067770/1462887212814438442/image.png?ex=696fd362&is=696e81e2&hm=993e5fb1b9816b65c370269841bc3f8b6d771d1a6c937e9d0e6683a677f6377d" height="30%" width="30%"/>
</p>
<p>
When the Configuration Wizard pops up, I will select "Standard Configuration" and click "Next". I will click "Next" again as I will not be changing anything. The next window will have the option to make a root password under "Modify Security Settings" or "Creat An Anonymous Account". I will use a root password. It's advised you have a very strong root password, but for this demonstration I will be using a simple password called "root".
</p>
<p>
<img src="https://cdn.discordapp.com/attachments/1390632590247067770/1462887610191057167/image.png?ex=696fd3c1&is=696e8241&hm=2a92293bff2f11d862f522a3ec6c68f7a664b4c2a27d332cb398015b5c6696d8" height="30%" width="30%"/> <img src="https://cdn.discordapp.com/attachments/1390632590247067770/1462897098499424469/image.png?ex=696fdc97&is=696e8b17&hm=4f545d7341eeee879489a14a3c7ed6f24de40f61fa14d1626f4f9c0efdd8b2c1" height="30%" width="30%"/> <img src="https://cdn.discordapp.com/attachments/1390632590247067770/1462891224074813586/image.png?ex=696fd71f&is=696e859f&hm=e56fe6ecaa62131af3de9560ca6009af9645e6f153125750fb02c03bddb798aa" height="30%" width="30%"/>
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
