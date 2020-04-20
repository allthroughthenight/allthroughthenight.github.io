---
layout: post
title: "Home Lab Stand-Up"
---

If you enjoy tech, then you probably have a pile of gadgets and gizmos that aren't obsolete, but you don't have a current use for. They probably aren't worthless, but you don't use them any more so they'll just sit around until they find their way into the trash next year.

For myself, after doing a bunch of PC upgrades using [r/buildapcsales](https://www.reddit.com/r/buildapcsales) during the holiday season, I had an extra GPU and CPU. Since they were budget components, I knew that they'd become more irrelevant as time went on.

Talking with some friends, [r/homelab](https://www.reddit.com/r/homelab). In short, it's about people who're enthusiastic about home networking and geeking out about self hosting whatever they can.

Looking at what I had, a Home Theater PC seemed like a good idea, but I'm not much for gaming, and I spend more time at my desk than on the couch. I've really enjoy Virtual Box and Vagrant for simple headless VMs, but I didn't like having to leave my PC on while I was away. So I decided that a VM server would be an reasonable goal.

I looked at a few hypervisors, but they were all too feature rich for my simple use cases. Looking around more, [KVM](https://jerrygamblin.com/2017/06/12/quickly-building-a-cloud-virtual-lab) with [Kimchi](https://www.ubuntuboss.com/ubuntu-server-18-04-as-a-hypervisor-using-kvm-and-kimchi-for-vm-management) looked good. In short, it's allows provisioning via a web interface so provisioning is a breeze.

As of now it's just sitting under my TV, humming away. I've left it off for extended periods if I don't have anything planned. Partly for power bill reasons, and partly for the longevity of the cooling fans. But overall I've been able to make experimenting easier, by using hardware I already owned.