# centos8

## Migration centos 8 to Centos Stream
* https://forums.centos.org/viewtopic.php?f=54&t=78708
```
In order to convert from archived vault Centos 8 the procedure is
Under /etc/yum.repo.d
Change urls from Centos to vault.
Example :
name=CentOS Linux $releasever - BaseOS
#mirrorlist=http://mirrorlist.centos.org/?release=$ ... fra=$infra
mirrorlist=http://vault.centos.org/?release=$relea ... fra=$infra
baseurl=http://vault.centos.org/$contentdir/$re ... search/os/

dnf clean all
dnf swap centos-linux-repos centos-stream-repos ( This will produce erros , so repeat this command twice)
dnf update
reboot

```

## Migration Centos 8 to Centos Stream
* https://www.linode.com/docs/guides/migrate-from-centos-8-to-centos-stream/
```
cat /etc/centos-release
dnf install centos-release-stream -y
dnf swap centos-{linux,stream}-repos -y
dnf distro-sync -y
cat /etc/centos-release
```


* https://marclabs.com/centos-8-quoi-de-neuf/

```
sudo dnf copr enable mattrose/python3-terminator
```

