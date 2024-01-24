## Download NVidia Driver for your Graphic card (Linux Version)

## Assign permission to setup file

```
chmod +x File_name
```

## Install "gcc" and "make"

```
apt install gcc
```
```
apt install make
```
## Run this commands to disable Nouveau

Step 1: Download Package
```
sudo bash -c "echo blacklist nouveau > /etc/modprobe.d/blacklist-nvidia-nouveau.conf"

```

Step 2: Install Package
```
sudo bash -c "echo options nouveau modeset=0 >> /etc/modprobe.d/blacklist-nvidia-nouveau.conf"

```
## Confirm the content of the newly created modeprobe file blacklist-nvidia-nouveau.conf:

```
cat /etc/modprobe.d/blacklist-nvidia-nouveau.conf

```
```
blacklist nouveau
options nouveau modeset=0

```
```
sudo update-initramfs -u

```
```
sudo reboot
```

## Now run the setup again
```
./File_name
```