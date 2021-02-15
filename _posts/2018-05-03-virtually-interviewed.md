---
layout: post
title: "Virtually Interviewed"
---

I had a few phone interviews recently, and a technical second round lined up. But a question that's come up more often than I'd expected was about VLANs. Since it's not a common topic unless you're a network engineer, I made this post to give a casual introduction.

# Physical vs Virtual Area Networks

Before I can talk about the virtual, let's talk about the physical. A local area network (LAN) can be thought of as a collection of connected devices that don't have to communicate with each other through a router. Defined more formally, any device that's on the same broadcast domain are on the same LAN.

Virtual local area networks (VLAN) allow devices to logically be on the same broadcast domain when they're not. This allows the use of one Layer 3 (L3) switch that can be faster, save space, and use less power than having a separate L2 switch and L3 router. It also helps with administration and segmentation of larger networks. The image below shows a simple example.

![]({{site.baseurl}}/assets/2018-05-03-virtually-interviewed/vlan-segments.jpg){:class="img-responsive"}

###### source: [fs.com](https://www.fs.com/vlan-how-does-it-change-your-network-management-aid-601.html)

# But How?

If you understand Ethernet frames and packet switching technology, then the technical concept of how VLAN works shouldn't be a stretch. Unless it's malicious or experimental, end devices won't do VLAN tagging of packets.

The technical details are defined in IEEE 802.1Q, but the main take away is that tagging adds an extra field to an Ethernet frame. To end clients, this is completely transparent since it's added after it's received from a sender, and is removed when it's sent to the destination.

![]({{site.baseurl}}/assets/2018-05-03-virtually-interviewed/ethernet-frame.png){:class="img-responsive"}

###### source: [Wikipedia](https://en.wikipedia.org/wiki/File:Ethernet_802.1Q_Insert.svg)

# In Closing

Unless you actively manage a large computer systems network, VLANs are out of scope for the average use. But it's prevalence is understated, and I hope you've learned a little bit by reading my little bit.
