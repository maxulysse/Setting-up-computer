# Setting up all the coding stuff

## Install git

``` bash
sudo apt-get install git
```

## Getting hub

You can directly download the latest binary on [github.com/github/hub](https://github.com/github/hub/), but you can also compile your own using [go](https://golang.org/), and since it might come handy to have it set up...

## Setting up Go environnement

All instructions are on [golang.org](https://golang.org/doc/install?download=go1.6.2.linux-amd64.tar.gz)
```bash
cd Downloads
sudo wget https://storage.googleapis.com/golang/go1.6.2.linux-amd64.tar.gz
tar -C /usr/local -xzf go1.6.2.linux-amd64.tar.gz
rm -rf go1.6.2.linux-amd64.tar.gz
```

Add to .bashrc
```
export GOPATH=$HOME/workspace/go
export PATH=$PATH:$GOROOT/bin:/usr/local/go/bin
```

## Installing hub
```bash
git clone https://github.com/github/hub.git
cd hub
./script/build -o ~/bin/hub
cd ..
rm -rf hub
```
Follow instructions on [github.com/github/hub](https://github.com/github/hub/tree/master/etc) for autocompletion

## Setting up Github

- Checking for existing SSH keys: [help.github.com](https://help.github.com/articles/checking-for-existing-ssh-keys/#platform-linux)
- Creating an SSH Key: [help.github.com](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-linux)
- Adding the SSH key to the github account: [help.github.com](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/#platform-linux)

## Using zsh

Follow instructions on [github.com/MaxUlysse](https://github.com/MaxUlysse/myzsh)

## Adding The Fuck

Follow instructions on [github.com/nvbn](https://github.com/nvbn/thefuck)

## Getting Sublime Text 3

```bash
cd Downloads
wget https://download.sublimetext.com/sublime-text_build-3114_amd64.deb
sudo dpkg -i sublime-text_build-3114_amd64.deb
```

## Getting all the intesting plugins

- [Package Control](https://packagecontrol.io/installation)
- [Git Gutter](https://github.com/jisaacks/GitGutter)
- [Bracket Highliter](https://packagecontrol.io/packages/BracketHighlighter)
- [Markdown Editing](https://github.com/SublimeText-Markdown/MarkdownEditing)
- [SideBar Enhancements](https://github.com/titoBouzout/SideBarEnhancements/tree/st3)
- [Trimmer](https://github.com/jonlabelle/Trimmer)

## Building essentials

```bash
sudo apt-get install python-pip python-dev build-essential zlib1g-dev python3-dev python3-pip
pip install Cython --user
```

## R

```
sudo apt-get install r-base-core libcurl4-gnutls-dev
```
