<h3>Required Items:</h3>

- USB flash drive with at least 4 GB of storage (this drive will get erased, so make sure nothing important is on it)
- Laptop or computer running Windows 11

<h3>Summary</h3>

Dual booting is the process of installing another operating system alongside your computer's original operating system, such as Windows or MacOS. You will have access to both operating systems and it will not erase anything on your device if done correctly.

This tutorial is for Windows 11 and will not work on MacOS, since dual booting Ubuntu with MacOS is not nearly as universal and some MacBooks have many security features that make it hard to do so. If you'd like to dual boot on a MacBook, let me know and I can help.

It does not hurt to keep a backup of your data on something like an external hard drive if you are worried about losing anything, but I have personally never ran into that problem.

[Backing up to external hard drive (optional)](https://www.microsoft.com/en-us/windows/learning-center/back-up-files)

<h3>Turning off BitLocker/Device Encryption</h3>

Not every Windows 11 device has BitLocker, but the majority of them do have it enabled. If you can't find anything in the search bar for either "Device Encryption" or "Manage BitLocker" your device most likely does not have it.

**Some versions of Windows 11 put it under the "Device Encryption" setting instead, while others just have it labelled as "BitLocker" in the control panel, so if one of the instruction sets doesn't work, try the other one.**

<h4>Turn off Device Encryption</h4>

1. Use the Windows search bar to search "Device encryption settings" and select "Open" 

<p align="center">
  <img src="images/image1.png" width="400">
</p>

2. Select the option to "Off"

<p align="center">
  <img src="images/image2.png" width="400">
</p>

3. Press "Turn off" to confirm

<p align="center">
  <img src="images/image3.png" width="400">
</p>

4. Wait for decryption to finish

<p align="center">
  <img src="images/image4.png" width="400">
</p>

<h4>Turn off BitLocker</h4>

1. Use the Windows search bar to search "Manage BitLocker" and select "Open" 

<p align="center">
  <img src="images/image5.png" width="400">
</p>

2. Press "Turn off BitLocker" under "Operating system drive"

<p align="center">
  <img src="images/image6.png" width="400">
</p>

3. Wait for the drive to finish decrypting (it will take a while), it will look like this once it's finished

<p align="center">
  <img src="images/image7.png" width="400">
</p>

<h3>Creating a Bootable USB Drive</h3>

Rufus is a tool used to format your USB flash drive into a bootable drive with an operating system on it. Once Ubuntu has been installed using the USB flash drive, you will no longer need it anymore and can use Ubuntu without the USB flash drive plugged in.

1. Install Ubuntu 22.04 ISO [here](https://releases.ubuntu.com/jammy/ubuntu-22.04.4-desktop-amd64.iso)
2. Install Rufus [here](https://github.com/pbatard/rufus/releases/download/v4.5/rufus-4.5.exe)
3. Using the Windows search bar, search for "rufus-4.5.exe" and press "Run as administrator"

<p align="center">
  <img src="images/image8.png" width="400">
</p>
 
4. Select "Yes" on the next prompt to allow Rufus to make changes to your device
5. Press the drop down menu under "Device" and select your USB flash drive, it may be named differently than "USB DRIVE (D:)" 

<p align="center">
  <img src="images/image9.png" width="400">
</p>

6. Press the "SELECT" button under "Boot selection" 

<p align="center">
  <img src="images/image10.png" width="400">
</p>

7. Search your Downloads folder for a file named "ubuntu-22.04.4-desktop-amd64" then press "Open" 

<p align="center">
  <img src="images/image11.png" width="400">
</p>

8. Double check that the correct drive and file are selected and then press "START"

<p align="center">
  <img src="images/image12.png" width="400">
</p>

9. Press "OK" for writing in ISO Image mode

<p align="center">
  <img src="images/image13.png" width="400">
</p>

10. Press "OK" to erase the flash drive (make sure nothing important is on this drive, if there is then press cancel and select a different USB drive)

<p align="center">
  <img src="images/image14.png" width="400">
</p>

11. This may or may not pop up, but if it does, press "OK"

<p align="center">
  <img src="images/image15.png" width="400">
</p>

12. Wait for Rufus to finish creating the bootable USB drive

<h3>Installing Ubuntu 22.04</h3>

1. Plug in your newly formatted USB drive
2. Use the Windows search bar to search "change advanced startup options" then press "Open"

<p align="center">
  <img src="images/image16.png" width="400">
</p>
 
3. Select "Restart now" under "Advanced startup"

<p align="center">
  <img src="images/image17.png" width="500">
</p>

4. Once the advanced startup menu comes up, select "Use a device" (you can use mouse or arrow keys + Enter)

<p align="center">
  <img src="images/image18.png" width="500">
</p>

5. Select the USB flash drive in the list, it may be named differently than "Linpus lite" 

<p align="center">
  <img src="images/image19.png" width="500">
</p>

6. Press enter with "Ubuntu" highlighted in the menu

<p align="center">
  <img src="images/image20.png" width="500">
</p>

7. Select "Install Ubuntu"

<p align="center">
  <img src="images/image21.png" width="500">
</p>

8. Select "Continue" for the next few pages (the default settings are fine)
9. When the Wi-Fi page comes up, select your Wi-Fi network and enter your password to connect
10. Select "Continue" until the following page comes up:

<p align="center">
  <img src="images/image22.png" width="500">
</p>

11. Make sure "Install Ubuntu alongside Windows Boot Manager" is selected and press "Continue"
12. Drag the divider to allocate the amount of storage space wanted for Ubuntu then press "Install Now" (personally I do half, but I would say it is good to have at least a quarter of your hard drive space allocated to Ubuntu)

<p align="center">
  <img src="images/image23.png" width="500">
</p>

13. Press "Continue" to confirm

<p align="center">
  <img src="images/image24.png" width="500">
</p>

14. Choose your time zone (Chicago) on the next page and press "Continue"
15. Type in your desired username and password, then press "Continue"
16. Ubuntu will now start installing, wait for it to finish then press "Restart Now"
17. Following the prompt on the screen, remove the flash drive and press "Enter"

<p align="center">
  <img src="images/image25.png">
</p>
 
18. After the restart, this GRUB menu will now appear on your device any time it is turned on. Use the arrow keys + Enter to select which operating system you want to boot into. 

<p align="center">
  <img src="images/image26.png" width="500">
</p>

19. You have now successfully finished dual booting your device. I recommend heading to the [ROS 2 Humble installation page](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html). Note: this installation is done on Ubuntu, so you'll have to boot Ubuntu up. All the commands on there will be ran on the Terminal (keyboard shortcut to open it is Ctrl + Alt + T). Copy and paste in the commands line by line then press enter after each one, do not select multiple lines at once as this will not work.
