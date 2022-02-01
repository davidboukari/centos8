# centos8

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

