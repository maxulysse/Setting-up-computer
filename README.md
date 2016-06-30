# Setting up a new computer

## Install Linux Mint

- Download ISO on [linuxmint.com](https://www.linuxmint.com/).
- Create bootable USB [community.linuxmint.com](https://community.linuxmint.com/tutorial/view/744)
- Install

## Upgrade Linux Kernel
All versions can be find on [kernel.ubuntu.com](http://kernel.ubuntu.com/~kernel-ppa/mainline/)

### Make sure system is up-to-date
``` bash
sudo apt-get update && sudo apt-get dist-upgrade -y
```

Reboot
``` bash
sudo reboot
```

### Download the latest stable kernel version
Here, when this is written, it's for v4.6.2 (64bit)
``` bash
cd ~/Downloads
wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-headers-4.6.2-040602_4.6.2-040602.201606100516_all.deb
wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-headers-4.6.2-040602-generic_4.6.2-040602.201606100516_amd64.deb
wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.6.2-yakkety/linux-image-4.6.2-040602-generic_4.6.2-040602.201606100516_amd64.deb
```

### Upgrade the kernel
``` bash
sudo dpkg -i linux-headers-4.6.2*.deb linux-image-4.6.2*.deb
```

Reboot
``` bash
sudo reboot
```

### Sources:
- [pcsteps.com](https://www.pcsteps.com/858-kernel-upgrade-linux-mint-ubuntu/)
- [yourownlinux.com](http://www.yourownlinux.com/2016/06/how-to-install-linux-kernel-4-6-2-in-linux.html)

## Setting up all the coding stuff

### Install git
``` bash
sudo apt-get install git
```

### Getting hub
You can directly download the latest binary on [github.com/github/hub](https://github.com/github/hub/), but you can also compile your own using [go](https://golang.org/), and since it might come handy to have it set up...

### Setting up Go environnement
All instructions are on [golang.org](https://golang.org/doc/install?download=go1.6.2.linux-amd64.tar.gz)
```bash
cd Downloads
sudo wget https://storage.googleapis.com/golang/go1.6.2.linux-amd64.tar.gz
tar -C /usr/local -xzf go1.6.2.linux-amd64.tar.gz
rm -rf go1.6.2.linux-amd64.tar.gz
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
Follow instructions on [github.com/github/hub](https://github.com/github/hub/tree/master/etc) for autocompletion

### Setting up Github
- Checking for existing SSH keys: [help.github.com](https://help.github.com/articles/checking-for-existing-ssh-keys/#platform-linux)
- Creating an SSH Key: [help.github.com](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-linux)
- Adding the SSH key to the github account: [help.github.com](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/#platform-linux)

### Using zsh
Follow instructions on [github.com/MaxUlysse](https://github.com/MaxUlysse/myzsh)

### Getting Sublime Text 3

```bash
cd Downloads
wget https://download.sublimetext.com/sublime-text_build-3114_amd64.deb
sudo dpkg -i sublime-text_build-3114_amd64.deb
```

### Getting all the intesting plugins
- [Package Control](https://packagecontrol.io/installation)
- [Git Gutter](https://github.com/jisaacks/GitGutter)
- [Bracket Highliter](https://packagecontrol.io/packages/BracketHighlighter)
- [Markdown Editing](https://github.com/SublimeText-Markdown/MarkdownEditing)
- [SideBar Enhancements](https://github.com/titoBouzout/SideBarEnhancements/tree/st3)
- [Trimmer](https://github.com/jonlabelle/Trimmer)

### Building essentials

```bash
sudo apt-get install python-pip python-dev build-essential zlib1g-dev
pip install Cython --user
```

### R

```
sudo apt-get install r-base-core libcurl4-gnutls-dev
```

## Getting Owncloud & Dropbox

### Owncloud

Instructions are on [software.opensuse.org](https://software.opensuse.org/download/package?project=isv:ownCloud:desktop&package=owncloud-client)

Should be done as root
```bash
echo 'deb http://download.opensuse.org/repositories/isv:/ownCloud:/desktop/Debian_8.0/ /' >> /etc/apt/sources.list.d/owncloud-client.list 
apt-get update
apt-get install owncloud-client
```

### Dropbox

Instructions are on [dropbox.com](https://www.dropbox.com/install?os=lnx)

### Eduroam

Instructions and installer are on [cat.eduroam.org](https://cat.eduroam.org/)

## Other programs
Graphic
```bash
sudo apt-get install inkscape optipng
```

Writing
```bash
sudo apt-get install texlive texlive-latex-extra texlive-full
```
For [Mendeley](https://mendeley.com), follow instructions on (mendeley.com)(https://www.mendeley.com/download-mendeley-desktop/debian/instructions/)