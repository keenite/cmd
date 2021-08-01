- [Linux General Commands](#linux-general-commands)
  * [Linux Package Management](#linux-package-management)
  * [String Operations](#string-operations)
  * [Linux Tool Organization](#linux-tool-organization)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

# Linux General Commands
## Linux Package Management
Package list all the installed packages
```bash
dpkg --list
dpkg --listfiles <package name>
```

## String Operations
Dump the device with strings.
```bash
hexdump -n 1000 /dev/nvme0n1 -C 
```

## Linux Tool Organization
```bash
sudo update-alternatives --config gcc
```
