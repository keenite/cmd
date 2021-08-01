# Linux General Commands
## Linux Package Management
Package list all the installed packages
```
dpkg --list
dpkg --listfiles <package name>
```

## String Operations
Dump the device with strings.
```shell
hexdump -n 1000 /dev/nvme0n1 -C 
```

## Linux Tool Organization
```
sudo update-alternatives --config gcc
```
