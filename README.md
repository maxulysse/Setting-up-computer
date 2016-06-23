# Upgrade Linux Kernel
Might be useful

Make sure system is up-to-date
''' bash
sudo apt-get update && sudo apt-get dist-upgrade -y
'''

Reboot
''' bash
sudo reboot
'''

Download the latest stable kernel 64bit version
''' bash
cd ~/Downloads
wget http://kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-headers-4.6.2-040602-generic_4.6.2-040602.201606100516_amd64.deb http://kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-headers-4.6.2-040602-lowlatency_4.6.2-040602.201606100516_amd64.deb http://kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-image-4.6.2-040602-generic_4.6.2-040602.201606100516_amd64.deb http://kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-image-4.6.2-040602-lowlatency_4.6.2-040602.201606100516_amd64.deb
'''

Other versions can be find [here](http://kernel.ubuntu.com/~kernel-ppa/mainline/)

Upgrade the kernel
''' bash
sudo dpkg -i linux-*.deb
'''

Based on this [guide](https://www.pcsteps.com/858-kernel-upgrade-linux-mint-ubuntu/)