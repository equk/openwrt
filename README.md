       _______                     ________        __
     |       |.-----.-----.-----.|  |  |  |.----.|  |_
     |   -   ||  _  |  -__|     ||  |  |  ||   _||   _|
     |_______||   __|_____|__|__||________||__|  |____|
              |__| W I R E L E S S   F R E E D O M
     -----------------------------------------------------

This is a small repo for my OpenWrt patches.

I have been using openwrt on various routers since the Linksys WRT54GS (White Russian 2006)

## Current Routers

### Netgear WNR2200

* usb power patch
* ath9k init script

*usb port patch:* fixes usb to allow use of usb devices (used for storage)

*ath9k init script:* init usb modules before attempting root mount, allowing the use of overlay or root pivot (extroot)

More info on extroot can be found on the openwrt wiki:

[http://wiki.openwrt.org/doc/howto/extroot/extroot.theory](http://wiki.openwrt.org/doc/howto/extroot/extroot.theory)

not working:

* buttons (wifi + wps) but who really uses those?
* usb led (not really that beneficial)

Example setup of USB /layout pivot on a 8GB USB 2.0 flash drive

* /dev/sda1     1.3GB   EXT4    /overlay
* /dev/sda2     524MB   SWAP
* /dev/sda3     5.4GB   EXT4    /data

### TP-LINK TP-841ND

Will possibly upload patches relating to this router in future.

For now here is my diagram for USB mod + serial connection.

[https://equk.co.uk/content/images/2015/04/tplink_841nd_ref.jpg](https://equk.co.uk/content/images/2015/04/tplink_841nd_ref.jpg)
