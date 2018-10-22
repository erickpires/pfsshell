PFS (PlayStation File System) tool for Linux/Mac/Unix
=====================================================

Information
===========

This is a tool to allow you to browse and transfer files to/from PFS filesystems.

Original source code
====================

http://web.archive.org/web/20061220090822/http://hdldump.ps2-scene.org/

~uyjulian

Compilation and installation
============================

To compile you just need to clone the repository and run:
```
make
```

The only requirement is a C compiler.

To install just copy the pfsshell executable to somewhere on your $PATH.

For Arch Linux users there's also an AUR [package](https://aur.archlinux.org/packages/pfsshell-git/).

Usage
====

To access a list of all available commands type `help`.

To use the filesystem manipulation commands you will have to specify a device
and mount a partition.

## Specifying the device

For example, to specify the device on *nix systems use:
```
device /dev/sdb
```

Or on Windows:
```
device hdd1:
```

(Obvious the device letter and hdd number may vary on you system).

## Mounting the partition

Assuming you already have a device with an APA partition table and
PFS partitions, you can mount a partition using:
```
mount partition_name
```

If the device does not have an APA partition table, you may use the
`initialize` command to create it.

If you don't have a PFS partition, or wish to create a new one you may
use the `mkpart` command.
