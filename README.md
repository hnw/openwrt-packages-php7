# openwrt-packages-php7

This is `php7` OpenWrt port from LEDE.

# How to install binary package

```
$ opkg update
$ opkg install openssl-util
$ echo 'src/gz hnw https://dl.bintray.com/hnw/openwrt-packages/15.05.1/ar71xx' >> /etc/opkg/customfeeds.conf
$ opkg update
$ opkg install lv
```

# How to build

To build these packages, add the following line to the feeds.conf in the OpenWrt buildroot:

```
$ echo 'src-git hnw_php7 https://github.com/hnw/openwrt-packages-php7.git' >> feeds.conf
```

Then you can build packages as follows:

```
$ ./scripts/feeds update -a
$ ./scripts/feeds install php7
$ make packages/php7/compile
```
