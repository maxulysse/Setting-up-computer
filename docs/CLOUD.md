# Getting cloud

## Owncloud

Instructions are on [software.opensuse.org](https://software.opensuse.org/download/package?project=isv:ownCloud:desktop&package=owncloud-client)

Should be done as root
```bash
echo 'deb http://download.opensuse.org/repositories/isv:/ownCloud:/desktop/Debian_8.0/ /' >> /etc/apt/sources.list.d/owncloud-client.list 
apt-get update
apt-get install owncloud-client
```

## Dropbox

Instructions are on [dropbox.com](https://www.dropbox.com/install?os=lnx)
