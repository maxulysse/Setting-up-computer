# How to upgrade Linux Kernel

All versions can be find on [kernel.ubuntu.com](http://kernel.ubuntu.com/~kernel-ppa/mainline/)

## Make sure system is up-to-date

``` bash
sudo apt-get update && sudo apt-get dist-upgrade -y
```

## Reboot

``` bash
sudo reboot
```

## Download the latest stable kernel version

Here, when this was written, it was v4.6.2 (64bit)
``` bash
cd ~/Downloads
wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-headers-4.6.2-040602_4.6.2-040602.201606100516_all.deb
wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-headers-4.6.2-040602-generic_4.6.2-040602.201606100516_amd64.deb
wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-image-4.6.2-040602-generic_4.6.2-040602.201606100516_amd64.deb
```

## Upgrade the kernel

``` bash
sudo dpkg -i linux-headers-4.6.2*.deb linux-image-4.6.2*.deb
```

## Reboot

``` bash
sudo reboot
```

## Sources:

- [pcsteps.com](https://www.pcsteps.com/858-kernel-upgrade-linux-mint-ubuntu/)
- [yourownlinux.com](http://www.yourownlinux.com/2016/06/how-to-install-linux-kernel-4-6-2-in-linux.html)
