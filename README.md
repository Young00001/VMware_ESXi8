# VMware VSphere8

In this repository I will be guiding you through the **Installation** and **Configuration** process for **VMware ESXi VSphere8**

With this guide you will be able to use this configured server for the following:

- **Remote Client Sessions**
- **Remote File Transfer**
- **and Much More!**
***
### ESXi 8.0 [Hardware Requirements](https://docs.vmware.com/en/VMware-vSphere/8.0/vsphere-esxi-installation/GUID-DEB8086A-306B-4239-BF76-E354679202FC.html)

***
## Installation

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
