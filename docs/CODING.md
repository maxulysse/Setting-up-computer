# Setting up all the coding stuff

## Install git

``` bash
sudo apt-get install git
```

## Getting GitHub CLI

[Install on Linux](https://github.com/cli/cli/blob/trunk/docs/install_linux.md)

## Setting up Github

- Checking for existing SSH keys: [help.github.com](https://help.github.com/articles/checking-for-existing-ssh-keys/#platform-linux)
- Creating an SSH Key: [help.github.com](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-linux)
- Adding the SSH key to the github account: [help.github.com](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/#platform-linux)

## Using zsh

Follow instructions on [github.com/maxulysse](https://github.com/maxulysse/myzsh)

## Building essentials

```bash
sudo apt-get install python-pip python-dev build-essential zlib1g-dev python3-dev python3-pip ruby-dev
pip install Cython --user
```

## R

```
sudo apt-get install r-base-core libcurl4-gnutls-dev
```

## Docker

Follow instructions on [linuxbsdos.com](http://linuxbsdos.com/2016/12/13/how-to-install-docker-and-run-docker-containers-on-linux-mint-1818-1/)

Don't forget to add yourself to the `docker` group and then reboot
```
usermod -aG docker ${USER}
```

## Nextflow

```
curl -fsSL get.nextflow.io | bash
```
Then `mv nextflow` to somewhere in your `$PATH`
https://github.com/cli/cli/blob/trunk/docs/install_linux.md
