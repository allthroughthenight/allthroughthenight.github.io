---
layout: post
title: "The Network Strikes Back"
---

My partner works from home, so having a stable internet internet connection is required. My desktop is hard wired to our modem, and their work laptop uses wifi. Whenever we have internet issues, the wifi is impacted more than the wired connection, so I rarely notice, while they scramble to reboot the router before they're kicked from their coporate VPN.

Recently we've had a slew of ISP outtages, which had cause them to constantly reboot our router to mitigate the issue. Days later after service was restored to normal, we'd still see connectivity issues, along with out 5Ghz band not working.

I though it was a fluke at first and didn't think much of it. But one evening while we're both in the living room the program we're streaming starts to fail to load.

I get my laptop to check on our router at 192.168.1.1 expecting a Linksys login screen.

![]({{site.baseurl}}/assets/2024-09-01-the-network-strikes-back/linksys-login.png)

But instead I see this log-in screen.

![]({{site.baseurl}}/assets/2024-09-01-the-network-strikes-back/openwrt-luci-login.png)

My initial guit reaction was worry. I was worried that our router was comprimised and a malitious actor was sucking up all our network traffic, explaining our intermitent internet issues. Then after doing a google reverse image search of the login portal I learned it's OpenWRT's login page.

Thinking back to my last usage of OpenWRT 


[homelab]({{site.baseurl}}/2019/05/01/home-lab-stand-up.html)