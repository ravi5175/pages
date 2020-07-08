title: Bootable USB from rufus (windows)
subtitle: Guide tutorial to make a bootable USB from rufus

<br>
<br>

### Rufus
Rufus is a utility that helps format and create bootable USB flash drives, such as USB keys/pendrives, memory sticks, etc.

It can be especially useful for cases where:

- you need to create USB installation media from bootable ISOs (Windows, Linux, UEFI, etc.)
- you need to work on a system that doesn't have an OS installed
- you need to flash a BIOS or other firmware from DOS
- you want to run a low-level utility

Despite its small size, Rufus provides everything you need!

<br>
<br>

### releax OS configurations
first of all you need to check if your system uses efi or boot legacy, follow [this Guide](https://www.tenforums.com/tutorials/85195-check-if-windows-10-using-uefi-legacy-bios.html) to get the same.

#### Legacy
- Partition Schemas : *MBR*
- Target System : *BIOS or UEFI*
- File System : *FAT32*

#### EFI
- Partition Schemas : *GPT*
- Target System : *UEFI*
- File System : *FAT32*
