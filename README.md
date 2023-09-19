# VMware VSphere8

In this repository I will be guiding you through the **Installation** and **Configuration** process for **VMware ESXi VSphere8**

With this guide you will be able to use this configured server for the following:

- **Remote Client Sessions**
- **Remote File Transfer**
- **and Much More!**
***
### Please Check the [VMware ESXi Compatability Guide](https://www.vmware.com/resources/compatibility/search.php) to Confirm Compatability with your System
***
### ESXi 8.0 [Hardware Requirements](https://docs.vmware.com/en/VMware-vSphere/8.0/vsphere-esxi-installation/GUID-DEB8086A-306B-4239-BF76-E354679202FC.html)
***
## Pre-Installation

1. Download the [VMware vSphere Hypervisor (ESXi) Image](https://customerconnect.vmware.com/evalcenter?p=vsphere-eval-8)

2. Format a **Bootable** Device (USB, CD, etc.)
   
#### WINDOWS

   - [RUFUS](https://rufus.ie/en/)
  

#### LINUX

   - [Fedora Media Writer](https://developers.redhat.com/blog/2016/04/26/fedora-media-writer-the-fastest-way-to-create-live-usb-boot-media)
   - [Etcher](https://etcher.balena.io/)

#### _Linux Terminal_
   1. **Open a terminal**
   2. **Identify the USB Drive:** Use the `lsblk` command to identify the device name of your USB drive
```
lsblk
```
   3. **Create the Bootable USB Drive Using `dd`:** Replace /path/to/esxi.iso with the actual path to your VMware ESXi ISO file and /dev/sdX with the device name of your USB drive:
```
sudo dd if=/path/to/esxi.iso of=/dev/sdX bs=4M status=progress
```
4. **Eject the USB drive:** After the process is complete, you can safely eject the USB drive:
```
sudo eject /dev/sdX
```
***
### Configuring the BIOS [Boot Settings](https://docs.vmware.com/en/VMware-vSphere/8.0/vsphere-esxi-installation/GUID-1298D6CC-B7B4-41EE-8F7E-98C58404F133.html)
***
## Installation
Begin the ESXi 8 Installation  
<img src="Images/Step_1.webp" alt="Step 1 Image" width="600" height="400">
```
(Enter) Continue
```
***
Accept the End User License Agreement (EULA)  
<img src="Images/Step_2.webp" alt="Step 2 Image" width="600" height="400">
```
(F11) Accept and Continue
```
***
VMware ESXi will now scan your device for available **Storage Devices**  
<img src="Images/Step_3.png" alt="Step 3 Image" width="700" height="500">
```
Select Your Storage Device
```
***
Select Keyboard Layout  
<img src="Images/Step_4.webp" alt="Step 4 Image" width="600" height="400">
```
(Enter) Continue
```
***
Enter a Root Password  
<img src="Images/Step_5.webp" alt="Step 5 Image" width="600" height="400">
```
(Enter) Continue
```
***
Confirm Install  
<img src="Images/Step_6.png" alt="Step 6 Image" width="600" height="400">
```
(F11) Install
```
***
Reboot Your System  
<img src="Images/Last_Step.webp" alt="Step 7 Image" width="600" height="400">
