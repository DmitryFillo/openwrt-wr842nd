======================
OpenWrt for TL-WR842ND
======================

My custom OpenWrt build and packages repo for TP-Link TL-WR842ND. I created it for personal use and so documentation is quite weak, but
I'll be happy if you'll use something from here.

.. contents::

Summary
=======

Minimalistic OpenWrt without girl's stuff like UCI firewall, web interface, uhttpd, but mc with subshell, UTF-8 support, bash, openvpn, su, tcpdump are available
out the box. Package repository is small too and includes monit, python, `my own feed <https://github.com/DmitryFillo/openwrt-feed>`_, etc.

This is very basic feautre overview, so some interesting stuff is not described. You can check build config for more information.

Download
========

`http://fillo.me/openwrt-wr842nd/ <http://fillo.me/openwrt-wr842nd/>`_.

If something will go wrong
==========================

Router's bootloader has TFTP support, so use `stripped stock firmware <https://github.com/DmitryFillo/openwrt-wr842nd/blob/master/TL-WR842ND-V2-stripped.zip>`_ for `TFTP recovering <https://wiki.openwrt.org/toh/tp-link/tl-wr842nd>`_.
