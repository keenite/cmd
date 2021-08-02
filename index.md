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
Write data to file
```
echo "0123456789abcdef" | dd of=/mnt/nfs_share/test.txt bs=1 seek=0 count=16
```
Write 4k data to file
* <N>	Any number: Specifies a minimum field width, if the text to print is shorter, it's padded with spaces, if the text is longer, the field is expanded
* .	The dot: Together with a field width, the field is not expanded when the text is longer, the text is truncated instead. "%.s" is an undocumented equivalent for "%.0s", which will force a field width of zero, effectively hiding the field from output
```
printf "0%.0s" {1..4096} > /mnt/nfs_share/4k.txt
```

## Linux Tool Organization
```bash
sudo update-alternatives --config gcc
```
