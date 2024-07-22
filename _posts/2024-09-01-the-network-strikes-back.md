---
layout: post
title: "The Network Strikes Back"
---

My partner works from home, so having a stable internet internet connection is required. My desktop is hard wired to our modem, and their work laptop uses wifi. Whenever we have internet issues, the wifi is impacted more than the wired connection, so I rarely notice, while they scramble to reboot the router before they're kicked from their coporate VPN.

Recently we've had a slew of ISP outtages, which had cause them to constantly reboot our router to mitigate the issue. Days later after service was restored to normal, we'd still see connectivity issues, along with out 5Ghz band not working. I though it was a fluke at first and didn't think much of it. But one evening while we're both in the living room the program we're streaming starts to fail to load.

I get my laptop to check on our router at 192.168.1.1 expecting a Linksys login screen.

![]({{site.baseurl}}/assets/2024-09-01-the-network-strikes-back/linksys-login.png)

But instead I see this log-in screen.

![]({{site.baseurl}}/assets/2024-09-01-the-network-strikes-back/openwrt-luci-login.png)

My initial guit reaction was worry. I was worried that our router was comprimised and a malitious actor was sucking up all our network traffic, explaining our intermitent internet issues. Then after doing a google reverse image search of the login portal I learned it's OpenWRT's login page. Thinking back to my [last usage of OpenWRT]({{site.baseurl}}/2022/04/01/no-more-networking.html) I thought I flashed the partition with the OEM firmware, so this was a puzzle to me.

Their feeder page for [uninstall OpenWRT](https://openwrt.org/faq/uninstall_openwrt_back_to_stock) directs to and 2) [tbd](https://openwrt.org/docs/guide-user/installation/generic.uninstall) about writing directly with `dd`. Neither page inspired confidence, but the second page has a [section at the bottom](https://openwrt.org/docs/guide-user/installation/generic.uninstall#via_bootloader) that links to reinstalling the OEM firmware via the GUI. Which is really just [installing it normally](https://openwrt.org/docs/guide-user/installation/generic.flashing), which then leads to their [Table of Hardware](https://openwrt.org/toh/start), which finally brought me back to the page for my [Linksys WRT1900AC](https://openwrt.org/toh/linksys/wrt1900ac). As I read through the instructions, I saw the section on [firmware recovery with the power switch](https://openwrt.org/toh/linksys/wrt1900ac#power_switch) as explained below:

1. Power off router with power switch.
2. Turn power back on and power LED will light.
3. Repeat step 2. two more times.
4. Turn power back on and allow router to fully boot into the alternate firmware partition

Once I went through those steps my router was back to running the OEM firmware. I thought a bit how this happened, what were the signs, and why I didn't see it earlier. Thinking about my partner, they would rapidly reset it to get internet back, causing it to boot from the OpenWRT partition instead of the OEM partition. Internet connectivity was fine since I used the same SSID names and passwords.

I thought about trying to blast the OpenWRT partition since I'd be able to recover into the OEM parition with the reset steps. But I wouldn't want to be away from home when my partner resets the router too much and ends up with no internet access. The solution I came up with was to reflash the OpenWRT parition with a new install, and change the SSIDs to say "network-name_OpenWRT" with a different password. That way if they reset the router too much into the OpenWRT partition, it'll broadcast what's happening so they can reset it back.