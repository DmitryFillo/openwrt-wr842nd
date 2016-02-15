==================
OpenWrt TL-WR842ND
==================

My custom OpenWrt build and packages repo for TP-Link TL-WR842ND. I created it for personal use and so documentation is quite weak, but
I'll be happy if you'll use something from here.

.. contents::

Summary
=======

OpenWrt build without girl's stuff like UCI firewall, web interface, uhttpd, etc. But I included important (for me) features: mc with subshell, UTF-8 support, bash, openvpn, su, tcpdump, htop, etc. Package repository is quite small and includes `my own feed <https://github.com/DmitryFillo/openwrt-feed>`_. Ready for create pivot overlay with ext4 flash partition (fdisk, cfdisk, mkfs, swap utils).

This is very basic feautre overview, so some interesting stuff is not described. You can check build config for more information.

Download
========

`OpenWrt 15.05 Chaos Calmer <https://github.com/DmitryFillo/openwrt-wr842nd/tree/gh-pages/15.05>`_

If something will go wrong
==========================

Router's bootloader has TFTP support, so use `stripped stock firmware <https://github.com/DmitryFillo/openwrt-wr842nd/blob/master/TL-WR842ND-V2-stripped.zip>`_ for `TFTP recovering <https://wiki.openwrt.org/toh/tp-link/tl-wr842nd>`_.
