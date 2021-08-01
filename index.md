- [Linux General Commands](#linux-general-commands)
  * [Linux Package Management](#linux-package-management)
  * [String Operations](#string-operations)
  * [Linux Tool Organization](#linux-tool-organization)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

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
