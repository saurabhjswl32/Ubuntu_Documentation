# Mounting Disk in Ubuntu


## Check disk mount point via "disk tool"

## Format the disk which you want to mount

## Create "data" directory within / (root directory)

## Give file permission to data directory
```
chmod 777 data
```

## Open Terminal and type below command with sudo
```
vim /etc/fstab
```

## Enter below entry in bottom of fstab file
```
/dev/sda* /data           ext4    defaults        0       2

```
## Reboot the machine

## Create a file in data directory with normal account

```
touch test.txt

```