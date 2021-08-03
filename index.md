- [Linux General Commands](#linux-general-commands)
  * [Linux Package Management](#linux-package-management)
  * [String Operations](#string-operations)
    + [Dump the device with strings.](#dump-the-device-with-strings)
    + [Write certain strings to files](#write-certain-strings-to-files)
    + [Covert numbers to binary or decimal](#covert-numbers-to-binary-or-decimal)
  * [Linux Tool Organization](#linux-tool-organization)
  * [Device Info Commands](#device-info-commands)
  * [Process related Commands](#process-related-commands)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>


# Linux General Commands
## Linux Package Management
Package list all the installed packages
```bash
dpkg --list
dpkg --listfiles <package name>
```

## String Operations
### Dump the device with strings.
```bash
hexdump -n 1000 /dev/nvme0n1 -C 
```
Write data to file
```
echo "0123456789abcdef" | dd of=/mnt/nfs_share/test.txt bs=1 seek=0 count=16
```
Redirect number to device/files
```
echo 3 | sudo tee /proc/sys/vm/drop_caches
```

### Write certain strings to files
* \<N\>	Any number: Specifies a minimum field width, if the text to print is shorter, it's padded with spaces, if the text is longer, the field is expanded
* \. The dot: Together with a field width, the field is not expanded when the text is longer, the text is truncated instead. "%.s" is an undocumented equivalent for "%.0s", which will force a field width of zero, effectively hiding the field from output

```bash
 # print 4096 0 s
 printf "0%.0s" {1..4096}
```

### Covert numbers to binary or decimal
```
echo "obase=2;15"|bc
1111
printf "%x" 15
f
echo "obase=10;ibase=16;1000" | bc
4096
```

## Linux Tool Organization
```bash
sudo update-alternatives --config gcc
```
 
## Device Info Commands
show the file system type and UUID
```bash
blkid /dev/<device>
```

## Process related Commands
return last return code
```bash
echo $? 
```

## Archive File
Compress /home/test files into <filename>.tar
* c – Creates a new .tar archive file.
* v – Verbosely show the .tar file progress.
* f – File name type of the archive file.
```bash
tar -cvf <filename>.tar /home/test
tar cvzf <filename>.tgz /home/test
tar cvfj <filename>.tar.bz2 /home/test
```
Untar tar Archive File
```
tar xvf <filename>.tar
```
Untar file to a folder
```
 tar -xvf <filename>.tar -C /home/dst
```
