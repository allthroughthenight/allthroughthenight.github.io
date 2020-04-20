---
layout: post
title: "Virtually Interviewed"
---

I've had a few phone interviews recently, and have a technical 2nd round lined up. But a question that's come up more often than I'd expected was about VLANs. Since it's a niche topic for software developers and undergraduate students, this post will give casual introduction to VLANs, to the best of my knowledge, and without plagiarizing.

#### Physical vs Virtual Area Networks

Before I can talk about the virtual, let's talk about the physical. A local area network (LAN) can be thought of as a collection of connected devices that don't have to communicate with each other through a router. A more rigorous definition would be that any device that's on the same broadcast domain are on the same LAN.

Virtual local area networks (VLAN) allow devices to logically be on the same broadcast domain, while being physically separated. This allows for the use of singular Layer 3 (L3) switches which can be faster, save space, and use less power than having separate L2 switches and L3 routers. It also simplifies segmentation of larger networks, help swith maintenance, administration, auditing, and threat mitigation.

The image below shows a simple example of devices that are physically separated, but by using VLANs, they're able to be grouped logically and communicate with each other as if they were.

<p><!-- wp:image {"align":"center","id":41} --></p>
<div class="wp-block-image">
<figure class="aligncenter"><img src="{{ site.baseurl }}/assets/vlan-segments.jpg" alt="vlan-segments" class="wp-image-41" /></figure>
</div>
<p><!-- /wp:image --></p>

###### source: [fs.com](https://www.fs.com/vlan-how-does-it-change-your-network-management-aid-601.html)

### But How?

If you understand Ethernet frames and packet switching technology, then the technical concept of how VLAN works shouldn't be a stretch. Unless it's malicious or experimental, end devices won't do VLAN tagging of packets.

The technical details are defined in IEEE 802.1Q, but the main take away is that tagging adds an extra field to an Ethernet frame. To end devices, this is process is completely transparent since it's added after it's received from a sender, and is removed when it's sent to the destination.

<p><!-- /wp:paragraph --></p>
<p><!-- wp:image {"align":"center","id":42,"width":821,"height":85} --></p>
<div class="wp-block-image">
<figure class="aligncenter is-resized"><img src="{{ site.baseurl }}/assets/ethernet-frame.png" width="821" height="85" /></figure>
</div>
<p><!-- /wp:image --></p>

###### source: [Wikipedia](https://en.wikipedia.org/wiki/File:Ethernet_802.1Q_Insert.svg)

#### In Closing

Unless you're actively manage a large computer systems network, rely on VoIP, or are an avid [homelab-er](https://old.reddit.com/r/homelab/), VLANs are out of scope for the average use. But it's prevalence is understated, and I hope you've learned a little bit by reading my little bit.
