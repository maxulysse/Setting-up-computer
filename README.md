# Setting up a new computer

## Upgrade Linux Kernel cf [pcsteps.com](https://www.pcsteps.com/858-kernel-upgrade-linux-mint-ubuntu/), [yourownlinux.com](http://www.yourownlinux.com/2016/06/how-to-install-linux-kernel-4-6-2-in-linux.html)

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
sudo dpkg -i linux-headers-4.6.2*.deb linux-image-4.6.2*.deb
```

## Setting up git/github/hub

Install git

``` bash
sudo apt-get install git
```

Getting hub cf [github.com](https://github.com/github/hub/)
You can directly download the latest binary, but you can also compile your own using Go

Setting up Go environnement cf [golang.org](https://golang.org/doc/install?download=go1.6.2.linux-amd64.tar.gz)
```bash
cd Downloads
sudo wget https://storage.googleapis.com/golang/go1.6.2.linux-amd64.tar.gz
tar -C /usr/local -xzf go1.6.2.linux-amd64.tar.gz
```

add to .bashrc
```
export GOPATH=$HOME/workspace/go
export PATH=$PATH:$GOROOT/bin:/usr/local/go/bin
```

Installing hub
```bash
git clone https://github.com/github/hub.git
cd hub
./script/build -o ~/bin/hub
cd ..
rm -rf hub
```

Setting up github
Checking for existing SSH keys: [help.github.com](https://help.github.com/articles/checking-for-existing-ssh-keys/#platform-linux)
Creating an SSH Key: [help.github.com](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-linux)
Addinf the SSH key to the github account: [help.github.com](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/#platform-linux)





