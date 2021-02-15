---
layout: post
title: "Home Lab Stand-Up"
---

If you enjoy tech, then you probably have a pile of old stuff that's not completely useless, but you don't have a use for. They aren't worthless, but you don't use them any more so they'll just sit around until they find their way into the trash.

For myself, after doing a bunch of PC upgrades with [r/buildapcsales](https://www.reddit.com/r/buildapcsales) during the holiday season, I had an extra GPU and CPU. Since they were budget components, I knew that they'd become more irrelevant as time went on.

Talking with some friends, they suggested checking out [r/homelab](https://www.reddit.com/r/homelab). In short, it's about people who're enthusiastic about home networking and geeking out about self hosting whatever they can.

Looking at what I had, a Home Theater PC seemed like a good idea, but I'm not much for gaming, and I spend more time at my desk than on the couch. I've really enjoy Virtual Box and Vagrant for simple headless VMs, but I didn't like leaving my PC on while I'm away. So I decided that a VM server would be an reasonable goal.

I looked at a few hypervisors, but they were all too complicated for my simple usage. Looking around more, [KVM](https://jerrygamblin.com/2017/06/12/quickly-building-a-cloud-virtual-lab) with [Kimchi](https://www.ubuntuboss.com/ubuntu-server-18-04-as-a-hypervisor-using-kvm-and-kimchi-for-vm-management) seemed simple enough, by having a simple web server to provision machines.

As of now it's just sitting under my TV, humming away. I've left it off for extended periods if I don't have anything planned. Partly for power bill reasons, and partly for the longevity of the fans. But overall I've been able to make experimenting easier, and utilize hardware I already own.