---
layout: post
title: "More Networking Boards"
---

My previous [networking board]({{site.baseurl}}/2020/03/21/networking-board.html) was pretty good. It was space efficient, had a [pi-hole]({{site.baseurl}}/2020/01/31/ad-blocking.html) for ad-blocking, and overall did what it needed to. When I moved to a new place, I had more space to cover, and had to think of a new way to get connectivity everywhere.

When I first made my networking board, I bought the Linksys WRT1900AC to install [OpenWRT](https://openwrt.org/). I was alwasy afraid of flashing the ROM and bricking it. Even though it's just downloading and having the router update, it still put me off. Thinking back, I'm not sure why it took me more than two years to do it, but after some internet issues I finally did.

When I looked flashing and set-up [instructions](https://www.youtube.com/watch?v=GVjIOzErKcc), it was easier than I thought since I didn't have to load the ROM manually and I could just do it from my own computer. It took 15 minutes to flash the router, and another 30 minutes playing with settings. Once I was done connectivity was back, but I was still having issues connecting to the internet. 

The good things about OpenWRT is that it has a lot of setting and features for power users. The bad thing about OpenWRT is that it has a lot of settings and features for power users.

The first issue was that I didn't know how to set my [pi-hole](https://pi-hole.net/) as the primary DNS and DHCP server. I tired a few settings but that didn't work, and I was getting behind on tasks I had at work, so I just unplugged it and let the router do that stuff.

Another issue that came up the next day was that the 5G band wasn't working. The settings were correct, so I restarted the 5G band and the router and everything was started working. For a while. Till the following day it was down again. Looking around more, the 5G band chipset has a known issue since the upstream project is dead ([related xkcd](https://xkcd.com/2347/)) so they have a work around for them ([one](https://forum.openwrt.org/t/5ghz-wifi-issues-with-wrt1200ac-running-openwrt-21-02-x/111546/2), [two](https://forum.openwrt.org/t/wrt1900acs-v1-hangs-frequently-on-openwrt-21-02-0-rc3/102259))

* ![]({{site.baseurl}}/assets/2022-02-02-more-networking-boards/board-01.jpg)
* ![]({{site.baseurl}}/assets/2022-02-02-more-networking-boards/board-02.jpg)
* ![]({{site.baseurl}}/assets/2022-02-02-more-networking-boards/board-03.jpg)

The wifi can still be a bit spotty, and the network drops require a reboot, but hopefully I'll figure out the settings I need to get things going smoothly.