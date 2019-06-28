# building-a-desktop

## Dual Boot Windows 10 and Ubuntu 18.04
1. Create a live USB drive of Ubuntu 18.04
2. Create a free space or unallocated space partition of your harddrive for Ubuntu 18.04
3. Disable fast startup in Windows [Optional]
4. Boot from the USB through BIOS mode
5. Choose install Ubuntu and choose installation type: Something Else
6. Use the free space to create root drive (mount point at / with primary partition, beginning location and Ext4), home drive (mount point at /home with primary partition, beginning location and Ext4), and swap (with 4096MB, logical partition, beginning location and swap)
7. Click install now
