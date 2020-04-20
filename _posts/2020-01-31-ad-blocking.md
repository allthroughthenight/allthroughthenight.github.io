---
layout: post
title: "Ad Blocking"
---

Overall it's been a long time coming, but I've finally set up my Raspberry Pi Pi-hole DNS sinkhole and couldn't be happier.

Without going into details, the overall process is fairly straight forward:
* Set-up your rPi with [Raspbian](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)
* ssh with the [default credentials](https://www.raspberrypi.org/forums/viewtopic.php?p=1107371#p1107371)
* Set-up [Pi-Hole](https://github.com/pi-hole/pi-hole/#one-step-automated-install)
* Enjoy!

In case you can't hardwire your rPi (like me), see the exampled below for the `/etc/wpa_supplicant/wpa_supplicant.conf` file needed to connect to wifi:

```
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=840

network={
 ssid="myWifi"
 psk="myPass"
}
```

A common misconception is the you need an rPi to run pihole. When really you don't since it's just a DNS server. If your home lab allows, they also have a [docker](https://github.com/pi-hole/docker-pi-hole/#running-pi-hole-docker) image that can be deployed.

There have also been some problems noticed when using pihole with Android devices on the Pi-hole forums ([1](https://discourse.pi-hole.net/t/pi-hole-with-sky-q-router-and-android-devices-tldr-turn-off-ipv6/16294)) ([2](https://discourse.pi-hole.net/t/pi-hole-works-everywhere-except-android-phones/3428/94)). The main consensus is that their may be a hard-coded value for Google's [Public DNS](https://developers.google.com/speed/public-dns/). So when an app reports that part of it fails to load (namely ads) it defaults to it. A work around is to ensure that also your default gateway (i.e. SOHO Wifi Router) has the Pi-hole set as it's DNS server. The added benefit is that any device in your network will automatically use the Pi-hole, without and configuration changes.