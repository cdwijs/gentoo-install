Download  LiveGUI USB Image from here: https://www.gentoo.org/downloads/

dd into memory stick.

``` bash
$ lsblk
NAME        MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
sda           8:0    0 465.8G  0 disk 
├─sda1        8:1    0   100M  0 part 
├─sda2        8:2    0    16M  0 part 
├─sda3        8:3    0 465.1G  0 part 
└─sda4        8:4    0   509M  0 part 
sdb           8:16   1  14.5G  0 disk 
└─sdb1        8:17   1  14.5G  0 part /run/media/cedric/ARCH_202102
nvme0n1     259:0    0 931.5G  0 disk 
├─nvme0n1p1 259:1    0   512M  0 part /boot
└─nvme0n1p2 259:2    0   931G  0 part /home


# dd if=/home/cedric/Downloads/livegui-amd64-20230723T170155Z.iso of=/dev/sdb bs=1MB status=progress

```