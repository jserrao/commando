## Linux/Ubuntu - Commands for making a RAID array

Digital Ocean has a [fantastic guide](https://www.digitalocean.com/community/tutorials/how-to-create-raid-arrays-with-mdadm-on-ubuntu-16-04) for doing this with `mdadm`, the Linux RAID utility. Read it.

1.  `lsblk -o NAME,SIZE,FSTYPE,TYPE,MOUNTPOINT` (shows you what's going on with your computer's hard drives). Output will look something like this - this shows three drives. `sda` and `sdb` are identical unformatted 4TB HDs while `sdc` is a 128GB SSD with an Ubuntu bootable partition and a swap space setup for when memory runs low):

```
NAME     SIZE FSTYPE TYPE MOUNTPOINT
sda      3.7T        disk
sdb      3.7T        disk
sdc    119.2G        disk
├─sdc1   512M vfat   part /boot/efi
├─sdc2 102.9G ext4   part /
└─sdc3  15.9G swap   part [SWAP]
```

02. `sudo mdadm --create --verbose /dev/md0 --level=1 --raid-devices=2 /dev/sda /dev/sdb` (Assuming the above drive setup, this command uses Linux's mdadm RAID creation utility to create an array. Here we are creating a RAID1 array with the `--create` flag, which means each byte saved to the array gets saved to each disk which creates a backup. You set the type of RAID array you want with the `--level=1` flag, which indicates a RAID1 array. We're striping two drives, so `--raid-devices=2` flag is set to 2. `/dev/sda /dev/sdb` describes the locations of the two drives we determined with the `lsblk` command.

03. `cat /proc/mdstat` (this command shows you where your striping process is at - this can take hours depending on the size of your drives. With 4TB 5400RPM SATA3 drives, this took about 8 hours for me). 

04. `sudo mdadm --detail --scan` (shows you what's going on with your RAID array). Output looks like this: 

```
ARRAY /dev/md/array-name metadata=1.2 name=server-name:array-name UUID=big:alphanumberic:string:here
```