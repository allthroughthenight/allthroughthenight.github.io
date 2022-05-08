---
layout: post
title: "Ad Blocking"
---

I finally set up my Pi-hole DNS sinkhole and couldn't be happier.

Set-up is straight forward:
1. Set-up Raspberry Pi with [Raspbian](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)
2. ssh with [default credentials](https://www.raspberrypi.org/forums/viewtopic.php?p=1107371#p1107371)
3. Set-up [Pi-Hole](https://github.com/pi-hole/pi-hole/#one-step-automated-install)

In case you can't hard wire your Raspberry Pi, see below for `/etc/wpa_supplicant/wpa_supplicant.conf` to connect to wifi:

```
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=840

network={
 ssid="myWifi"
 psk="myPass"
}
```

A misconception is the you need an Raspberry Pi to run pihole, but there's also a [docker](https://github.com/pi-hole/docker-pi-hole/#running-pi-hole-docker) image that can be used in lieu of physical hardware.

There's also been problems when using pihole with Android devices on the Pi-hole forums ([1](https://discourse.pi-hole.net/t/pi-hole-with-sky-q-router-and-android-devices-tldr-turn-off-ipv6/16294)) ([2](https://discourse.pi-hole.net/t/pi-hole-works-everywhere-except-android-phones/3428/94)). The prevailing theory is that there's probably hard-coded values for Google's [Public DNS](https://developers.google.com/speed/public-dns/). So when an app reports that part of it fails to load (like ads) it defaults to the Public DNS. But an easy fix is to just have your router use the Pi-hole as it's DNS server. It also has the added benefit that any device on your network will automatically use the Pi-hole, without needing configurations.
