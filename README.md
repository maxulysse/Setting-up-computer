# Upgrade Linux Kernel
Might be useful

Make sure system is up-to-date
``` bash
sudo apt-get update && sudo apt-get dist-upgrade -y
```

Reboot
``` bash
sudo reboot
```

Download the latest stable kernel 64bit version
``` bash
cd ~/Downloads
wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-headers-4.6.2-040602_4.6.2-040602.201606100516_all.deb
wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-headers-4.6.2-040602-generic_4.6.2-040602.201606100516_amd64.deb
wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-image-4.6.2-040602-generic_4.6.2-040602.201606100516_amd64.deb
```

Other versions can be find [here](http://kernel.ubuntu.com/~kernel-ppa/mainline/)

Upgrade the kernel
``` bash
sudo dpkg -i linux-*.deb
```

Cf [pcsteps.com](https://www.pcsteps.com/858-kernel-upgrade-linux-mint-ubuntu/)
Based on this [yourownlinux.com](http://www.yourownlinux.com/2016/06/how-to-install-linux-kernel-4-6-2-in-linux.html)
