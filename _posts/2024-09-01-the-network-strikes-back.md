---
layout: post
title: "The Network Strikes Back"
---

My partner works from home, so having a stable internet internet connection is required. My desktop is hard wired, and their work laptop uses wifi. Whenever we have internet issues, the wifi is impacted more than the wired connection, so I rarely notice while they rush to reboot the router before they're kicked from their coporate VPN.

Recently we've had a slew of ISP outtages, which causes my partner to constantly reboot our router to mitigate the issue. Days later after service was restored to normal, we still saw connectivity issues, along with our 5Ghz band not working. I didn't think much of it at first, then one evening the show we were streaming failed to load.

I check on our router at 192.168.1.1 expecting a Linksys log-in screen.

![]({{site.baseurl}}/assets/2024-09-01-the-network-strikes-back/linksys-login.png)

But instead I see this log-in screen.

![]({{site.baseurl}}/assets/2024-09-01-the-network-strikes-back/openwrt-luci-login.png)

At this point I'm worried that our router was hacked and our network got pwned, explaining the other intermitent internet issues. A google reverse image search of the login portal showed it's an OpenWRT's login page. Thinking back to my [last usage of OpenWRT]({{site.baseurl}}/2022/04/01/no-more-networking.html), I thought I flashed the partition with the OEM firmware, so this puzzled me.

Their page to [uninstall OpenWRT](https://openwrt.org/faq/uninstall_openwrt_back_to_stock) directs to ther [table of hardware](https://openwrt.org/toh/start) and [back to original firmware](https://openwrt.org/docs/guide-user/installation/generic.uninstall) about writing directly with `dd`. Neither page inspired confidence, but the second page had a [section at the bottom](https://openwrt.org/docs/guide-user/installation/generic.uninstall#via_bootloader) that links to reinstalling the OEM firmware via the GUI. Which is really just [installing it normally](https://openwrt.org/docs/guide-user/installation/generic.flashing), which then leads back to their [table of hardware](https://openwrt.org/toh/start), which finally brought me to the page for my [Linksys WRT1900AC](https://openwrt.org/toh/linksys/wrt1900ac) (phew). 

As I read through the instructions, I saw the section on [firmware recovery with the power switch](https://openwrt.org/toh/linksys/wrt1900ac#power_switch) explained below:

1. Power off router with power switch.
2. Turn power back on and power LED will light.
3. Repeat step 2. two more times.
4. Turn power back on and allow router to fully boot into the alternate firmware partition

After these steps my router started running the OEM firmware. Thinking about how this happened, I remember my partner would reset the router often to get internet back, likely having it to boot from the OpenWRT partition instead of the OEM partition. We didn't notice since the internet connectivity was okay and I used the same network names and passwords for the OpenWRT and OEM firmware, so our devices connected normally.

I thought about clearing the OpenWRT partition entirely, but I didn't want to be out of the house when my partner resets the router and ends up with no internet access. The solution I came up with was to reinstall OpenWRT, and change the SSIDs to "network-name_OpenWRT" with a different password. That way if they reset the router too much, it'd fail loudly by 1) making the wifi unusable and 2) broadcast a different SSID.