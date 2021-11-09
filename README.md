# shell script to make persistent kali linux from live bootable Kali linux installer
#######################################
# example output when running script
#######################################

mint@LinuxMint$ ./make_kali_persistent.sh kali-linux-2020.4-live-amd64.iso
Enter USB Flash Drive(ex: /dev/sdb): /dev/sdb
Confirm kali-linux-2020.4-live-amd64.iso installation on /dev/sdb (y/n)?: y

Writing kali-linux-2020.4-live-amd64.iso to /dev/sdb ...
3504340992 bytes (3.5 GB, 3.3 GiB) copied, 259 s, 13.5 MB/s
3354+1 records in
3354+1 records out
3517394944 bytes (3.5 GB, 3.3 GiB) copied, 259.934 s, 13.5 MB/s

Making Persistenct Volume on /dev/sdb3 from 3518 to 15669 ...
Information: You may need to update /etc/fstab.

mke2fs 1.45.5 (07-Jan-2020)
Creating filesystem with 2966528 4k blocks and 742560 inodes
Filesystem UUID: f26fc694-a257-4d88-a258-aefc73acac05
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632, 2654208

Allocating group tables: done
Writing inode tables: done
Creating journal (16384 blocks): done
Writing superblocks and filesystem accounting information: done

Disk /dev/sdb: 14.61 GiB, 15669919744 bytes, 30605312 sectors
Disk model:  SanDisk 3.2Gen1
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0x3c89495a

Device     Boot   Start      End  Sectors  Size Id Type
/dev/sdb1  *         64  6867839  6867776  3.3G 17 Hidden HPFS/NTFS
/dev/sdb2       6867840  6869311     1472  736K  1 FAT12
/dev/sdb3       6871040 30603263 23732224 11.3G 83 Linux

# test Kali with persistence with KVM or QEMU
# sudo qemu-system-x86_64 -m 4G -drive format=raw,file=$DEVICE    
