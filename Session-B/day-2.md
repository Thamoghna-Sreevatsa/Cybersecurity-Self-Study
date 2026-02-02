# Linux System Startup


1. When the system is powered ON, the BIOS (Basic I/O System) initializes the hardware and perfroms tests on the Main Memory(RAM). This test is called POST (Power ON Self Test). BIOS is stored on a ROM Chip on the motherboard.

2. Next comes the bootloader. It is usually stored in the boot sector for traditional/MBR(Master Boot Record) systems and in the EFI partition for EFI/UEFI(Unified Extensible Firmware Interfaces). Until this point , no info stored is accessed by the system but after this, Date and Time are accessed from the CMOS values from the motherboard's battery powered chip. The most commonly found bootloader on Linux is GRUB (Grand Unified Bootloader)(This is also the bootloader for my Linux), ISO Linux for booting from removable media like USBs and Das-U Boot for booting on embedded devices. Bootloaders generally present a UI where alt options for booting Linux/other OS' present on the system can be chosen.

3. Boot loader is responsible for loading the Kernel image and Initial RAM Disk/filesystem into memory.

4. For MBR systems:

   MBR(512 Bytes in size) ---> Examines partition table to find a suitable partition ---> Searches for second stage bootloader (like GRUB) and loads it into RAM ---> Splash Screen is displayed giving us options on which OS to boot ---> Kernel of selected OS is loaded onto RAM and control is passed to it ---> Kernel uncompresses itself and initializes the hardware device drivers built into it.

5. For EFI/UEFI systems:

   UEFI Firmware reads boot manager data ---> Determines which UEFI app is to be launched and from where ---> UEFI app ( Example: GRUB) is then launched as defined in the boot entry of the firmware's boot manager ---> """ ( from here on solash screen and stuff is the same as MBR systems).

