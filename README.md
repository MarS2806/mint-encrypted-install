mint-encrypted-install
======================

This is basically a partially-automated version of Naldi Stefano's
tutorials [here](https://community.linuxmint.com/tutorial/view/2026),
[here](https://community.linuxmint.com/tutorial/view/2231),
[here](https://community.linuxmint.com/tutorial/view/2061) and
[here](https://community.linuxmint.com/tutorial/view/2191), which were
partly based on blog posts by Pavel Kogan
[here](http://www.pavelkogan.com/2014/05/23/luks-full-disk-encryption/)
and
[here](http://www.pavelkogan.com/2015/01/25/linux-mint-encryption/). All
credit goes to them for figuring out how to do it; I just made it into
a script.

The Linux Mint 18 installer has an option for installing on LVM inside
an encrypted LUKS container, but this is only offered if you want to
erase the whole disk (no dual boot), and also leaves the `/boot`
partition unencrypted. If you want to encrypt everything including
`/boot`, or want to install any sort of encrypted system alongside
another OS for dual boot, you have to configure the bootloader and
initramfs manually -- which is time-consuming and easy to get
wrong. This script guides you through the process, and automates as
many of the commands as possible, making it much easier to set up.

This is still an advanced configuration, though, and assumes you are
comfortable with the terminal, shell scripts, partitioning, LVM, and
installing and managing normal non-encrypted Linux systems. If in
doubt, read the tutorials linked above, and above all, *PLEASE BE
CAREFUL*. Typing anything wrong here could erase your hard drive! Make
sure you test anything in a virtual machine before trying it on your
real machine.


Usage
-----

Boot the Mint live USB as normal. But instead of running the 'Install
Linux Mint' launcher on the desktop, open a terminal and run the
following commands:

    wget https://raw.githubusercontent.com/callumcameron/mint-encrypted-install/master/mint-encrypted-install
    ./mint-encrypted-install

This will guide you through the rest of the process.
