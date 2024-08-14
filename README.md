### Required Items:

- USB flash drive with at least 4 GB of storage (this drive will get erased, so make sure nothing important is on it)
- Laptop or computer running Windows 11
### Summary

Dual booting is the process of installing another operating system alongside your computer's original operating system, such as Windows or MacOS. You will have access to both operating systems and it will not erase anything on your device if done correctly.

This tutorial is for Windows 11 and will not work on MacOS, since dual booting Ubuntu with MacOS is not nearly as universal and some MacBooks have many security features that make it hard to do so. If you'd like to dual boot on a MacBook, let me know and I can help.

It does not hurt to keep a backup of your data on something like an external hard drive if you are worried about losing anything, but I have personally never ran into that problem. 

[Backing up to external hard drive (optional)](https://www.microsoft.com/en-us/windows/learning-center/back-up-files)
### Turning off BitLocker/Device Encryption

Not every Windows 11 device has BitLocker, but the majority of them do have it enabled. If you can't find anything in the search bar for either "Device Encryption" or "Manage BitLocker" your device most likely does not have it.

**Some versions of Windows 11 put it under the "Device Encryption" setting instead, while others just have it labelled as "BitLocker" in the control panel, so if one of the instruction sets doesn't work, try the other one.**
#### Turn off Device Encryption

1. Use the Windows search bar to search "Device encryption settings" and select "Open" 

![[3af69c26-4bab-4c71-9c3a-efea78083565.png|400]]

2. Select the option to "Off"

![[Pasted image 20240813161531.png|400]]

3. Press "Turn off" to confirm

![[a3c5e96a-1eb0-4f69-9cb3-9573dc17f623.png|400]]

4. Wait for decryption to finish
![[Pasted image 20240813164011.png|400]]

#### Turn off BitLocker 

1. Use the Windows search bar to search "Manage BitLocker" and select "Open" 

![[43585d85-9414-4227-9264-f6cc8f35011a.png|400]]

2. Press "Turn off BitLocker" under "Operating system drive"

![[Pasted image 20240813164643.png|400]]

3. Wait for the drive to finish decrypting (it will take a while), it will look like this once it's finished

![[Pasted image 20240813165312.png|400]]

### Creating a Bootable USB Drive

Rufus is a tool used to format your USB flash drive into a bootable drive with an operating system on it. Once Ubuntu has been installed using the USB flash drive, you will no longer need it anymore and can use Ubuntu without the USB flash drive plugged in.

1. Install Ubuntu 22.04 ISO [here](https://releases.ubuntu.com/jammy/ubuntu-22.04.4-desktop-amd64.iso)
2. Install Rufus [here](https://github.com/pbatard/rufus/releases/download/v4.5/rufus-4.5.exe) 
3. Using the Windows search bar, search for "rufus-4.5.exe" and press "Run as administrator"

 ![[Pasted image 20240813161906.png|400]]
 
4. Select "Yes" on the next prompt to allow Rufus to make changes to your device
5. Press the drop down menu under "Device" and select your USB flash drive, it may be named differently than "USB DRIVE (D:)" 

![[Pasted image 20240813162027.png|400]]

6. Press the "SELECT" button under "Boot selection" 

![[Pasted image 20240813162047.png|400]]

7. Search your Downloads folder for a file named "ubuntu-22.04.4-desktop-amd64" then press "Open" 

![[Pasted image 20240813162828.png|400]]
8. Double check that the correct drive and file are selected and then press "START"

![[Pasted image 20240813163029.png|400]]

9. Press "OK" for writing in ISO Image mode

![[Pasted image 20240813163226.png|400]]

10. Press "OK" to erase the flash drive (make sure nothing important is on this drive, if there is then press cancel and select a different USB drive)

![[Pasted image 20240813163356.png|400]]

11. This may or may not pop up, but if it does, press "OK"

![[Pasted image 20240813163529.png|400]]\

12. Wait for Rufus to finish creating the bootable USB drive
### Installing Ubuntu 22.04

1. Plug in your newly formatted USB drive
2. Use the Windows search bar to search "change advanced startup options" then press "Open"

 ![[Pasted image 20240813170630.png|400]]
 
3. Select "Restart now" under "Advanced startup"

![[Pasted image 20240813170823.png|500]]

4. Once the advanced startup menu comes up, select "Use a device" (you can use mouse or arrow keys + Enter)

![[IMG_1336.png|500]]

5. Select the USB flash drive in the list, it may be named differently than "Linpus lite" 

![[IMG_1338.png|500]]

6. Press enter with "Ubuntu" highlighted in the menu

![[Select-Ubuntu-from-Gub-menu.png|500]]

7. Select "Install Ubuntu"

![[Start-Ubuntu-22.04-Installation.png|500]]

8. Select "Continue" for the next few pages (the default settings are fine)
9. When the Wi-Fi page comes up, select your Wi-Fi network and enter your password to connect
10. Select "Continue" until the following page comes up:

![[Ubuntu-22.04-Along-side-Windows-11-option-is-missing-1.png|500]]

11. Make sure "Install Ubuntu alongside Windows Boot Manager" is selected and press "Continue"
12. Drag the divider to allocate the amount of storage space wanted for Ubuntu then press "Install Now" (personally I do half, but I would say it is good to have at least a quarter of your hard drive space allocated to Ubuntu)

![[Allocate-Ubuntu-22.04-Disk-space-from-Windows-11.png|500]]

13. Press "Continue" to confirm

![[Confirm-the-writing-of-Hard-disk.png|500]]

14. Choose your time zone (Chicago) on the next page and press "Continue"
15. Type in your desired username and password, then press "Continue"
16. Ubuntu will now start installing, wait for it to finish then press "Restart Now"
17. Following the prompt on the screen, remove the flash drive and press "Enter"

 ![[Pasted image 20240813232502.png]]
 
1. After the restart, this GRUB menu will now appear on your device any time it is turned on. Use the arrow keys + Enter to select which operating system you want to boot into. 

 ![[Windows-11-and-Ubuntu-22.04-Dual-boot-installation.png|500]]

19. You have now successfully finished dual booting your device. I recommend heading to the [ROS 2 Humble installation page](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html ). Note: this installation is done on Ubuntu, so you'll have to boot Ubuntu up. All the commands on there will be ran on the Terminal (keyboard shortcut to open it is Ctrl + Alt + T). Copy and paste in the commands line by line then press enter after each one, do not select multiple lines at once as this will not work.