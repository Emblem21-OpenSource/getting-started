# Create a Bootable USB of an ISO

## OSX

```
# How to make a bootable USB of an ISO on OSX
curl "<ISO URL>" -o "~/os.iso"
hdiutil convert -format UDRW -o ~/os.img ~/os.iso

# Insert USB
diskutil list

$ USB should be /dev/disk2, if it isn't, change all instances of /dev/disk2 with the right device path
diskutil partitionDisk /dev/disk2 1 "Free Space" "unused" "100%"
sudo dd if=~/os.img.dmg of=/dev/disk2 bs=1m
diskutil unmountDisk /dev/disk2
diskutil eject /dev/disk2
```
