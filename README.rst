==================
OpenWrt TL-WR842ND
==================

My custom OpenWrt build and packages repo for TP-Link TL-WR842ND. I created it for personal use and so documentation is quite weak, but
I'll be happy if you'll use something from here.

.. contents::

Summary
=======

OpenWrt build without girl's stuff like UCI firewall, web interface, uhttpd, etc. But I included important (for me) features: mc with subshell, UTF-8 support, bash, openvpn, su, tcpdump, htop, etc. Package repository is quite small and includes `my own feed <https://github.com/DmitryFillo/openwrt-feed>`_. Ready for create pivot overlay with ext4 flash partition (fdisk, cfdisk, mkfs, swap utils).

Pre-installed packages:

.. code:: bash

    base-files - 157.2-r48634
    bash - 4.3.39-1
    block-mount - 2016-01-10-96415afecef35766332067f4205ef3b2c7561d21
    busybox - 1.23.2-1
    bzip2 - 1.0.6-2
    cfdisk - 2.25.2-4
    curl - 7.40.0-3
    dnsmasq - 2.73-1
    dropbear - 2015.67-1
    e2fsprogs - 1.42.12-1
    fdisk - 2.25.2-4
    fstools - 2016-01-10-96415afecef35766332067f4205ef3b2c7561d21
    glib2 - 2.43.4-1
    hostapd-common - 2015-03-25-1
    hostapd-mini - 2015-03-25-1
    htop - 1.0.3-1
    iconv - 1.11.1-1
    iftop - 1.0pre2-1
    ip - 4.0.0-1
    iptables - 1.4.21-1
    iptables-mod-conntrack-extra - 1.4.21-1
    iw - 3.17-1
    iwinfo - 2015-06-01-ade8b1b299cbd5748db1acf80dd3e9f567938371
    jshn - 2015-11-08-10429bccd0dc5d204635e110a7a8fae7b80d16cb
    jsonfilter - 2014-06-19-cdc760c58077f44fc40adbbe41e1556a67c1b9a9
    kernel - 3.18.23-1-1aae7af192d63eeb37d12a3233a6349d
    kmod-ath - 3.18.23+2015-03-09-3
    kmod-ath9k - 3.18.23+2015-03-09-3
    kmod-ath9k-common - 3.18.23+2015-03-09-3
    kmod-cfg80211 - 3.18.23+2015-03-09-3
    kmod-crypto-aead - 3.18.23-1
    kmod-crypto-aes - 3.18.23-1
    kmod-crypto-arc4 - 3.18.23-1
    kmod-crypto-core - 3.18.23-1
    kmod-crypto-ecb - 3.18.23-1
    kmod-crypto-hash - 3.18.23-1
    kmod-crypto-manager - 3.18.23-1
    kmod-crypto-pcompress - 3.18.23-1
    kmod-crypto-sha1 - 3.18.23-1
    kmod-fs-ext4 - 3.18.23-1
    kmod-gre - 3.18.23-1
    kmod-ifb - 3.18.23-1
    kmod-ikconfig - 3.18.23-1
    kmod-input-core - 3.18.23-1
    kmod-ipt-conntrack - 3.18.23-1
    kmod-ipt-conntrack-extra - 3.18.23-1
    kmod-ipt-core - 3.18.23-1
    kmod-ipt-nat - 3.18.23-1
    kmod-iptunnel - 3.18.23-1
    kmod-lib-crc-ccitt - 3.18.23-1
    kmod-lib-crc16 - 3.18.23-1
    kmod-lib-textsearch - 3.18.23-1
    kmod-loop - 3.18.23-1
    kmod-mac80211 - 3.18.23+2015-03-09-3
    kmod-mppe - 3.18.23-1
    kmod-nf-conntrack - 3.18.23-1
    kmod-nf-ipt - 3.18.23-1
    kmod-nf-nat - 3.18.23-1
    kmod-nf-nathelper - 3.18.23-1
    kmod-nf-nathelper-extra - 3.18.23-1
    kmod-nls-base - 3.18.23-1
    kmod-nls-utf8 - 3.18.23-1
    kmod-ppp - 3.18.23-1
    kmod-pppoe - 3.18.23-1
    kmod-pppox - 3.18.23-1
    kmod-pptp - 3.18.23-1
    kmod-sched-core - 3.18.23-1
    kmod-scsi-core - 3.18.23-1
    kmod-slhc - 3.18.23-1
    kmod-tun - 3.18.23-1
    kmod-usb-core - 3.18.23-1
    kmod-usb-ohci - 3.18.23-1
    kmod-usb-storage - 3.18.23-1
    kmod-usb2 - 3.18.23-1
    libacl - 20140812-1
    libattr - 20150220-1
    libblkid - 2.25.2-4
    libblobmsg-json - 2015-11-08-10429bccd0dc5d204635e110a7a8fae7b80d16cb
    libbz2 - 1.0.6-2
    libc - 0.9.33.2-1
    libcharset - 1.11.1-1
    libcurl - 7.40.0-3
    libext2fs - 1.42.12-1
    libffi - 3.0.13-1
    libgcc - 4.8-linaro-1
    libiconv-full - 1.11.1-1
    libintl-full - 0.19.6-2
    libip4tc - 1.4.21-1
    libiwinfo - 2015-06-01-ade8b1b299cbd5748db1acf80dd3e9f567938371
    libjson-c - 0.12-1
    libjson-script - 2015-11-08-10429bccd0dc5d204635e110a7a8fae7b80d16cb
    liblzo - 2.08-1
    libmount - 2.25.2-4
    libncurses - 5.9-2
    libnl-tiny - 0.1-4
    libopenssl - 1.0.2f-1
    libpcap - 1.5.3-1
    libpcre - 8.38-1
    libpolarssl - 1.3.14-1
    libpthread - 0.9.33.2-1
    librpc - 2015-04-10-308e9964bfb623773dc0dcc99ef9d18d1551d6ae
    librt - 0.9.33.2-1
    libsmartcols - 2.25.2-4
    libssp - 4.8-linaro-1
    libubox - 2015-11-08-10429bccd0dc5d204635e110a7a8fae7b80d16cb
    libubus - 2015-05-25-f361bfa5fcb2daadf3b160583ce665024f8d108e
    libuci - 2015-08-27.1-1
    libuuid - 2.25.2-4
    libxtables - 1.4.21-1
    mc - 4.8.14-1.3
    mtd - 21
    nano - 2.4.1-1
    netifd - 2015-12-16-245527193e90906451be35c2b8e972b8712ea6ab
    openvpn-openssl - 2.3.6-5
    opkg - 9c97d5ecd795709c8584e972bfdf3aee3a5b846d-9
    ppp - 2.4.7-6
    ppp-mod-pppoe - 2.4.7-6
    ppp-mod-pptp - 2.4.7-6
    procd - 2015-10-29.1-d5fddd91b966424bb63e943e789704d52382cc18
    resolveip - 2
    ss - 4.0.0-1
    sudo - 1.8.14p3-1
    swap-utils - 2.25.2-4
    swconfig - 10
    tar - 1.28-2
    tc - 4.0.0-1
    tcpdump - 4.5.1-4
    terminfo - 5.9-2
    tune2fs - 1.42.12-1
    ubox - 2015-11-22-c086167a0154745c677f8730a336ea9cf7d71031
    ubus - 2015-05-25-f361bfa5fcb2daadf3b160583ce665024f8d108e
    ubusd - 2015-05-25-f361bfa5fcb2daadf3b160583ce665024f8d108e
    uci - 2015-08-27.1-1
    usign - 2015-05-08-cf8dcdb8a4e874c77f3e9a8e9b643e8c17b19131
    uuidd - 2.25.2-4
    wget - 1.17.1-1
    zlib - 1.2.8-1
    zoneinfo-europe - 2015d-1


This is very basic feautre overview, so some interesting stuff is not described. You can check build config for more information.

Download
========

`OpenWrt 15.05 Chaos Calmer <https://github.com/DmitryFillo/openwrt-wr842nd/tree/gh-pages/15.05>`_

If something will go wrong
==========================

Router's bootloader has TFTP support, so use `stripped stock firmware <https://github.com/DmitryFillo/openwrt-wr842nd/blob/master/TL-WR842ND-V2-stripped.zip>`_ for `TFTP recovering <https://wiki.openwrt.org/toh/tp-link/tl-wr842nd>`_.
