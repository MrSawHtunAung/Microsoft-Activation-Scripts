## Sources
This documents was copied from www.micorsoftactivationscripts.com.

# MAS - Microsoft Activation Scripts
Microsoft Activation Scripts is an open source Windows and Office activator that utilizes the HWID, Ohook, KMS38 and Online KMS activation methods.
Download Official ISO’s, get product keys and activate Windows 10/11, Office & so much more!
A must have tool for Windows Users, Devs and SysAdmins.

# Why Microsoft Activation Scripts?
Microsoft Activation Scripts (MAS) is the only working and virus free Windows and Office activator available.
No need to struggle with licenses and ISO downloads!

# About MAS
MAS (Microsoft Activation Scripts) is an open source Windows & Office activator by utilizing genuine Microsoft authentication processes and generic keys to register Windows and Office products.

For in-depth view of activation processes used by MAS, read below methods;

Activation Type|	Supported Product|	Activation Period|	Is Internet Needed|
| ------ | ------ | ------ | ------ |
|HWID|	Windows 10, 11|	Permanent|	Yes|
|Ohook|	Office|	Permanent|	No|
|KMS38|	Windows 10, 11, Server|	Till the year 2038|	No|
|Online KMS|	Windows 7, 8, 10, 11 & Office	|180 Days. Lifetime With Renewal Task|	Yes|

Microsoft Activation Scripts was created by WindowsAddict also known as Massgravel. However, the MAS project wouldn’t be possible without the kind help and use of other honorable developers’ tools and scripts.

# Installing MAS
## Method 1 - Powershell
1. Open PowerShell (Not CMD). To do that, right-click on the Windows start menu and select PowerShell or Terminal.
2. Copy and paste the code below and press enter
3. You will see the activation options. Choose [1] HWID for Windows activation. Choose [2] Ohook for Office activation.
4. That’s all
```irm https://get.activated.win | iex```

## Note
>* The IRM command in PowerShell downloads a script from a specified URL, and the IEX command executes it.
>* Always double-check the URL before executing the command.

## Method 2 - Traditional
1. Download the file, under download table.
2. Right-click on the downloaded zip file and extract
3. In the extracted folder, find the folder named All-In-One-Version
4. Run the file named MAS_AIO.cmd
5. You will see the activation options, follow the on-screen instructions.
6. That’s all.

# `$OEM$` Folders
The `$OEM$` folder is a special directory used during the installation of Windows to customize and automate the setup process. It allows system builders, IT administrators, or users to add drivers, applications, scripts, and other custom files to a Windows installation.
Here’s a breakdown of how it works and its common uses:
## How the `$OEM$` Folder Works
The `$OEM$` folder is typically placed in the Windows installation media (such as a USB drive or installation DVD) in the following path: `sources\$OEM$`.
During the installation, the Windows setup process automatically copies the contents of the `$OEM$` folder to the appropriate locations on the target system.
## Common Subfolders and Their Functions:
### `$OEM$$1`:
-	Maps to the root directory of the system drive `(usually C:\)`.
-	Any files or folders placed in this directory are copied directly to the root of the system drive during installation.

### `$OEM$$$`:
•	Corresponds to the Windows directory (usually C:\Windows).
•	Useful for adding files directly to the Windows installation, such as scripts or custom configuration files.
### `$OEM$$Docs`:
•	Maps to the Documents folder on the system.
•	Used to include documentation, user manuals, or guides that the user can access after installation.
### `$OEM$\Drivers`:
•	Often used to add device drivers that need to be installed with Windows.
•	Typically includes subfolders for different hardware components (e.g., audio, network, etc.).
### `$OEM$$Progs`:
Maps to the Program Files directory, allowing the inclusion of software that needs to be pre-installed.
## Common Uses:
>-	Adding Drivers: Automate the installation of custom drivers during the Windows setup, ensuring hardware compatibility.
>-	Custom Scripts: Include scripts for automatic configurations, user account creation, registry modifications, or software installations.
>-	Branding: OEMs often use the `$OEM$` folder to add branding elements like logos, wallpapers, or custom support information.
### Benefits
>-	Streamlines the installation process by automating custom setups.
>-	Reduces post-installation tasks, saving time and effort for IT administrators and OEMs.
### How to Create Pre-Activated Windows ISO
To create a pre-activated Windows installation .iso, do the following:
1.	Extract the `$OEM$` folder to the desktop using the MAS script.
2.	Copy the `$OEM$` folder to the sources folder in the Windows installation media (.iso or USB).
3.	The directory will appear like this: `\sources\$OEM$` in your altered .iso or on your bootable USB drive.
4.	Now use this .iso or bootable USB drive to install Windows, it will either already be activated (KMS38) as soon as it boots or will self-activate (HWID or Online KMS) at the first internet contact.
5.	You can check here for activation method details and select the activation method as per your requirement.

#### Notes
>-	On Windows 8 and later, running setupcomplete.cmd is disabled if the default installed key for the edition is from the OEM channel, except for Enterprise editions and Windows Server operating systems.
>-	However, in Windows 10, IoT Enterprise editions were not included in the Enterprise category list during the installation process. As a result, Enterprise with an OEM key can handle setupcomplete.cmd, but IoT Enterprise (LTSC) cannot. This was fixed in later Windows 11 versions.
>-	In Windows 10 IoT Enterprise (LTSC), you can resolve this issue by using the Non-IoT Windows 10 Enterprise LTSC ISO. In this case, the HWID method in preactivation will install the IoT LTSC key to change the edition and enable HWID activation.
>-	In Windows 11 IoT Enterprise (LTSC), it works fine as expected by default.

### Edit ISO File
1.	As stated above, you can copy the `$OEM$` folder to your bootable USB so you don’t have to edit the ISO file. However, if you need to, then follow the steps below.
2.	Download AnyBurn Free Portable and extract this zip file
3.	Run the file named AnyBurn(64-bit)\AnyBurn.exe
4.	Select the option named Edit image file
5.	Follow the on-screen instructions and add the `$OEM$` folder to the sources folder so that the directory will appear like this:
`\sources\$OEM$`
6.	Save the ISO, that’s it.

#### KMS38 - Server Cor/Acor
-	Windows Server Cor/Acor (No GUI) editions don’t have the clipup.exe file.
-	To KMS38 activate it, you need to download the missing ClipUp.exe file from this link.
-	File: ClipUp.exe
SHA-256: 0d6e9f6bbd0321eda149658d96040cb4f79e0bd93ba60061f25b28fecbf4d4ef
This file has digital signatures that can be verified. You can also get this file from the official Windows Server 2016 x64 RTM ISO.
-	Put the ClipUp.exe beside the KMS38 Activation script. That would be either MAS_AIO.cmd or KMS38_Activation.cmd
-	The activation script will check ClipUp.exe in the current folder (from where script is running) and will use it accordingly.

### HWID
>When using HWID activation, no files are stored on the system, and Windows 10-11 will be activated when connected to the internet for the first time.

### Ohook
>If Office is preinstalled then Ohook method will activate the Office immediately without Internet. This activation uses custom sppc.dll file for the activation.

### KMS38
>When using KMS38 activation, no files are stored on the system, and Windows 10-11-Server becomes activated immediately without Internet.

### Online KMS
>When using Online KMS activation, Windows-Server and Office (Preinstalled) both will be activated when connected to the internet for the first time. This option uses a renewal task for lifetime activation.

### HWID + Ohook
>In this method, Windows 10-11 will be activated with HWID, and Office (Preinstalled) will be activated using Ohook.

### HWID + Online KMS
>In this method, Windows 10-11 will be activated with HWID, and Office (Preinstalled) will be activated using Online KMS.

### KMS38 + Ohook
>In this method, Windows 10-11-Server will be activated with KMS38, and Office (Preinstalled) will be activated using Ohook.

### KMS38 + Online KMS
>In this method, Windows 10-11-Server will be activated with KMS38, and Office (Preinstalled) will be activated using Online KMS.

### Online KMS + Ohook
>In this method, Windows-Server will be activated with Online KMS, and Office (Preinstalled) will be activated using Ohook.

# ----

# Check Activation Status
A robust Windows Powershell script to display the licensing status of Microsoft Windows and Office.

### Features
-	Require Windows Powershell 2.0 at minimum
-	Practical replacement for slmgr.vbs functions /dli /dlv xpr
-	Shows the activation expiration date for supported products
-	Shows the ProductKeyChannel for Windows Vista / 7 / 8 primary installed key (available for uplevel Windows by default)
-	Shows the status of add-on licenses (Extended Security Updates, APPXLOB, OCUR…, etc)
-	Shows the status of Automatic VM Activation for Windows Server 2012 and later
-	Shows the status of Subscription Activation for Windows 11 24H2 and later
-	Implement vNextDiag.ps1 functions to detect Office vNext licenses (subscription or lifetime)
-	Implement Client Licensing Check tool for Windows 8 and later

### Usage
1.	Download and Open MAS_AIO or use the standalone app by abbodi1406
2.	On the Menu, press 5 to Check Activation Status.
   ![image](https://github.com/user-attachments/assets/71d60589-85b5-44f5-83bb-244466b188a0)
   ![image](https://github.com/user-attachments/assets/cfc60681-c560-4397-9a54-ca94696b4a5d)

### Supported products
-	Windows Vista and later / Windows Server 2008 and later.
-	Office 2010 and later (MSI or C2R), installed on Windows XP and later.
-	Office UWP apps on Windows 10/11.
-	Windows and Office KMS Host (CSVLK), installed on Windows Server 2003 and later.

### Unsupported
- Status of Token-based or Active Directory (AD) Volume Licensing.

  # ----

  # Command Line Switches
You can use the below switches in MAS AIO, separate files version and in Powershell one-liner to run in unattended mode.
If you want to use it in Windows Pre-Activation then check this page for more details.

## Switches List
| Switches |	Meaning |
| ------ | ------ |
|/HWID|	Activate with HWID|
|/HWID-NoEditionChange	|Some editions don’t support HWID, script by default change edition to nearest available to enable HWID activation. This switch can be used to stop this change. You don’t need to add /HWID switch with this.
|||	 
|/Ohook	Install| Ohook to activate Office|
|/Ohook-Uninstall	|Uninstall Ohook|
||| 	 
|/KMS38|	Activate with KMS38|
|/KMS38-RemoveProtection|	Remove KMS38 protection|
|/KMS38-NoEditionChange	|Some editions don’t support KMS38, script by default change edition to nearest available to enable KMS38 activation. This switch can be used to stop this change. You don’t need to add /KMS38 switch with this.|
|||
|/K-Windows	|Activate only Windows with Online KMS|
|/K-Office|	Activate only Office with Online KMS|
|/K-ProjectVisio|	Activate only Project/Visio with Online KMS|
|/K-WindowsOffice|	Activate all Windows and Office with Online KMS|
|/K-NoEditionChange|	Some editions don’t support KMS, script by default change edition to nearest available to enable KMS activation. This switch can be used to stop this change.|
|/K-NoRenewalTask|	Whenever you run any activation, the script installs the auto-renewal task by default. To NOT auto-install renewal task with activation, use this switch.|
|/K-Uninstall|	Uninstall Online KMS including renewal tasks|
|/K-Server-YOURKMSSERVERNAME|	To specify a server address for activation, where YOURKMSSERVERNAME needs to be edited for server name|
|/K-Port-YOURPORTNAME|	To specify a port for activation, where YOURPORTNAME needs to be edited for port address|
||| 	 
|/S	|Run operations in silent mode (no output)|

### Uses In Powershell One Liner
```& ([ScriptBlock]::Create((irm https://get.activated.win))) /para```
- Replace `/para` in this command with the switches from the above table. You can also use multiple switches. For example, `/HWID /Ohook`
- This Powershell one-liner will work on Windows 8.1 and later versions only.
- Make sure to use the below command beforehand to enable TLs1.2 on older Windows versions.
`[Net.ServicePointManager]::SecurityProtocol=[Net.SecurityProtocolType]::Tls12`
- To change the edition through the command line, check here. We didn’t automate it in MAS because it requires a reboot in some cases.

### Rules
- Script will run in unattended mode if any switch is used.
- `/S` switch is not applicable in MAS separate files version scripts.
- All switches are case-insensitive, and work in any order, but must be separated with spaces.
- KMS Uninstall switch will take precedence over other KMS switches.
- KMS38 remove protection switch will take precedence over KMS38 activation.

