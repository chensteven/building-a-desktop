# building-a-desktop

## Hardware requirements

* Motherboard
* CPU
* RAM
* HDD & SSD
* GPU
* PSU
* Case
* CPU Cooler
* Fans

## Software requirements

* OS
* Software Development
* Web Development
* Data Science
* Machine Learning
* Deep Learning

## Installation

### 1. Dual Boot Windows 10 and Ubuntu 18.04
1. Create a live USB drive of Ubuntu 18.04
2. Create a free space or unallocated space partition of your harddrive for Ubuntu 18.04
3. Disable fast startup in Windows [Optional]
4. Boot from the USB through BIOS mode
5. Choose install Ubuntu and choose installation type: Something Else
6. Use the free space to create root drive (mount point at / with primary partition, beginning location and Ext4), home drive (mount point at /home with primary partition, beginning location and Ext4), and swap (with 4096MB, logical partition, beginning location and swap)
7. Click install now

### 2. Install Windows 10 and Ubuntu 18.04 on different hard drives

#### Windows

#### Ubuntu

1. Use the free space to create root drive (mount point at / with primary partition, beginning location and Ext4), home drive (mount point at /home with primary partition, beginning location and Ext4), swap (with half of your memory stick MB, logical partition, beginning location and swap), and EFI with 500MB

2. Install Nvidia Display Driver

General rule here is to go on the website and find the appropriate driver for your video card version. Double check the version number.

Go to terminal and type in:
```
sudo apt-get-repository ppa:graphics-drivers/ppa
```

Then go to Software Updates and Additional Drivers tab to see if the above version number is there. If so, click Apply Changes on it.

Tips and Tricks:

*For UEFI/Bios*
- To support UEFI, you will need to install your OS in UEFI mode. Make sure you turn off CMS in your BIOS.

*For Windows Installation*

- If anytime the installation fails, using diskpart in Command Prompt can help you clean, format, partition or even convert your hard drives from MBR to GPT and vice versa.

*For Ubuntu Installation*

- If you are stuck at "failed to create kernel channel", then go to edit mode upon bootup and add nomodeset after "... quiet splash"
- If your mouse and keyboard is slow at login screen, then most likely it has to do with your new video card. Also add nomodeset after "... quiet splash". More information can be found here if login problem persists: https://gist.github.com/alexlee-gk/76a409f62a53883971a18a11af93241b
