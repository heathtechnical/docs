# Tools

 * fdisk
 * gdisk
 * parted

Use _lsblk_ to list storage devices:

    # lsblk
    NAME                 MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
    sda                    8:0    0   20G  0 disk
    ├─sda1                 8:1    0  500M  0 part /boot
    └─sda2                 8:2    0 19.5G  0 part
      ├─rhel_rhce01-root 253:0    0 17.5G  0 lvm  /
      └─rhel_rhce01-swap 253:1    0    2G  0 lvm  [SWAP]
    sr0                   11:0    1 1024M  0 rom
