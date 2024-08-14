<h3><strong>Required Items:</strong></h3>

- USB flash drive with at least 4 GB of storage (this drive will get erased, so make sure nothing important is on it)
- Laptop or computer running Windows 11

<h3><strong>Summary</strong></h3>

Dual booting is the process of installing another operating system alongside your computer's original operating system, such as Windows or MacOS. You will have access to both operating systems and it will not erase anything on your device if done correctly.

This tutorial is for Windows 11 and will not work on MacOS, since dual booting Ubuntu with MacOS is not nearly as universal and some MacBooks have many security features that make it hard to do so. If you'd like to dual boot on a MacBook, let me know and I can help.

It does not hurt to keep a backup of your data on something like an external hard drive if you are worried about losing anything, but I have personally never ran into that problem.

[Backing up to external hard drive (optional)](https://www.microsoft.com/en-us/windows/learning-center/back-up-files)

<h3><strong>Turning off BitLocker/Device Encryption</strong></h3>

Not every Windows 11 device has BitLocker, but the majority of them do have it enabled. If you can't find anything in the search bar for either "Device Encryption" or "Manage BitLocker" your device most likely does not have it.

**Some versions of Windows 11 put it under the "Device Encryption" setting instead, while others just have it labelled as "BitLocker" in the control panel, so if one of the instruction sets doesn't work, try the other one.**

<h4><strong>Turn off Device Encryption</strong></h4>

<ol>
<li>Use the Windows search bar to search "Device encryption settings" and select "Open"</li>
</ol>

<p align="center">
  <img src="images/image1.png" width="400">
</p>

<ol start="2">
<li>Select the option to "Off"</li>
<li>Press "Turn off" to confirm</li>
<li>Wait for decryption to finish</li>
</ol>

<p align="center">
  <img src="images/image4.png" width="400">
</p>

<h4><strong>Turn off BitLocker</strong></h4>

<ol>
<li>Use the Windows search bar to search "Manage BitLocker" and select "Open"</li>
</ol>

<p align="center">
  <img src="images/image5.png" width="400">
</p>

<ol start="2">
<li>Press "Turn off BitLocker" under "Operating system drive"</li>
<li>Wait for the drive to finish decrypting (it will take a while), it will look like this once it's finished</li>
</ol>

<p align="center">
  <img src="images/image7.png" width="400">
</p>

<h3><strong>Creating a Bootable USB Flash Drive</strong></h3>

Rufus is a tool used to format your USB flash drive into a bootable drive with an operating system on it. Once Ubuntu has been installed using the USB flash drive, you will no longer need it anymore and can use Ubuntu without the USB flash drive plugged in.

<ol>
<li><a href="https://releases.ubuntu.com/jammy/ubuntu-22.04.4-desktop-amd64.iso" target="_blank">Install Ubuntu 22.04 ISO here</a></li>
<li><a href="https://github.com/pbatard/rufus/releases/download/v4.5/rufus-4.5.exe" target="_blank">Install Rufus here</a></li>
<li>Using the Windows search bar, search for "rufus-4.5.exe" and press "Run as administrator"</li>
</ol>

<p align="center">
  <img src="images/image8.png" width="400">
</p>
 
<ol start="4">
<li>Select "Yes" on the next prompt to allow Rufus to make changes to your device</li>
<li>Press the drop down menu under "Device" and select your USB flash drive, it may be named differently than "USB DRIVE (D:)"</li>
</ol>

<p align="center">
  <img src="images/image9.png" width="400">
</p>

<ol start="6">
<li>Press the "SELECT" button under "Boot selection"</li>
<li>Search your Downloads folder for a file named "ubuntu-22.04.4-desktop-amd64" then press "Open"</li>
</ol>

<p align="center">
  <img src="images/image11.png" width="400">
</p>

<ol start="8">
<li>Double check that the correct drive and file are selected and then press "START"</li>
<li>Press "OK" for writing in ISO Image mode</li>
<li>Press "OK" to erase the flash drive (make sure nothing important is on this drive, if there is then press cancel and select a different USB drive)</li>
<li>This may or may not pop up, but if it does, press "OK"</li>
<li>Wait for Rufus to finish creating the bootable USB drive</li>
</ol>

<h3><strong>Installing Ubuntu 22.04</strong></h3>

<ol>
<li>Plug in your newly formatted USB drive</li>
<li>Use the Windows search bar to search "change advanced startup options" then press "Open"</li>
</ol>

<p align="center">
  <img src="images/image16.png" width="400">
</p>
 
<ol start="3">
<li>Select "Restart now" under "Advanced startup"</li>
<li>Once the advanced startup menu comes up, select "Use a device" (you can use mouse or arrow keys + Enter)</li>
</ol>

<p align="center">
  <img src="images/image18.png" width="500">
</p>

<ol start="5">
<li>Select the USB flash drive in the list, it may be named differently than "Linpus lite"</li>
<li>Press enter with "Ubuntu" highlighted in the menu</li>
<li>Select "Install Ubuntu"</li>
</ol>

<p align="center">
  <img src="images/image21.png" width="500">
</p>

<ol start="8">
<li>Select "Continue" for the next few pages (the default settings are fine)</li>
<li>When the Wi-Fi page comes up, select your Wi-Fi network and enter your password to connect</li>
<li>Select "Continue" until the following page comes up:</li>
</ol>

<p align="center">
  <img src="images/image22.png" width="500">
</p>

<ol start="11">
<li>Make sure "Install Ubuntu alongside Windows Boot Manager" is selected and press "Continue"</li>
<li>Drag the divider to allocate the amount of storage space wanted for Ubuntu then press "Install Now" (personally I do half, but I would say it is good to have at least a quarter of your hard drive space allocated to Ubuntu)</li>
<li>Press "Continue" to confirm</li>
<li>Choose your time zone (Chicago) on the next page and press "Continue"</li>
<li>Type in your desired username and password, then press "Continue"</li>
<li>Ubuntu will now start installing, wait for it to finish then press "Restart Now"</li>
<li>Following the prompt on the screen, remove the flash drive and press "Enter"</li>
</ol>

<p align="center">
  <img src="images/image25.png">
</p>
 
<ol start="18">
<li>After the restart, this GRUB menu will now appear on your device any time it is turned on. Use the arrow keys + Enter to select which operating system you want to boot into.</li>
</ol>

<p align="center">
  <img src="images/image26.png" width="500">
</p>

<ol start="19">
<li>You have now successfully finished dual booting your device. I recommend heading to the <a href="https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html" target="_blank">ROS 2 Humble installation page</a>. Note: this installation is done on Ubuntu, so you'll have to boot Ubuntu up. All the commands on there will be ran on the Terminal (keyboard shortcut to open it is Ctrl + Alt + T). Copy and paste in the commands line by line then press enter after each one, do not select multiple lines at once as this will not work.</li>
</ol>
