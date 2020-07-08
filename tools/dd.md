title: Bootable USB from dd (linux)
subtitle: Guide tutorial to make a bootable USB from dd

<br>
<br>

### 'dd' command
dd is a command utility of [coreutils]() package with primary purpose is to convert and copy files

##### basic syntax
```
sudo dd if=name-of.iso of=/dev/sd? status=progress
```

Two things you need to know:  

- if == input file
- of == output file

input file will be this *iso*, output file will be the *usb* device node *#everything_is_file_in_linux* 👊

for input file provide the complete address to iso file
*supposing iso is in Download folder*

if=~/Downloads/releax-0.5.b.iso

<br>

#### Getting USB device node
a simple way is to use **lsblk**, execute the below command:

```
lsblk | grep disk
```

**Example Output:**

```
sda     8:0     0       1.8T    0   disk    \n
sdb     8:16    0     223.6G    0   disk    \n
sdc     8:32    0       7.7G    0   disk
```

Like i am using a *USB* device of 8gb , so my *USB* device is **sdc**  
so, output file is */dev/sdc*


<br>
<br>

**Example command:**

```
sudo dd if=~/Downloads/releax-0.5.b.iso of=/dev/sdc status=progress
```
