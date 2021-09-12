---
layout: post
title: "USB for You and Me"
---

My workhorse laptop, an X230 Thinkpad, had gotten me through my undergrad, two jobs, and an internship. Since buying it I've double the RAM (from 4 to 8 GB), and swapped the hybrid 500GB HDD for a 128 SSD. Both were well spent and increased performance.

During my move into a new place for my new job, I damaged my desktop PC's power supply. At the time the symptoms seemed more like it could've been the motherboard or even the CPU. But instead of ordering any parts, it'd be easier to do an hour drive to the nearest Fry's electronics store and troubleshoot there. But my budget at the time was air tight, so I decided to wait a few paychecks. In the meantime it was just me and my X230. No games, just the terminal and web surfing.

For sake of convenience I'd leave it in hibernation instead of just turning it off. The SSD made both tasks comparably the same, so I thought it could handle being powered on 24/7. That was a mistake.

The first problem was loss of my internet connection. Usually not a big issue, the internet at my place sucks so I just ran a ping command to see when it comes back up.

```
user at X230 in ~/temp
$ ping google.com
zsh: command not found: ping
```

Maybe my paths aren't right, let's just get the absolute path and call it from there

```
user at X230 in ~/temp
$ whereis ping
zsh: command not found: whereis
```

Hmm, let's just turn it off and on again. It's uptime was almost two weeks straight.

```
No boot device is available, press Enter to continue
```

This isn't the first time I'd had a problem like this, but this time I only had one computer. At first I thought I should try and test my laptop hardware with another hard drive, but thinking about the weird terminal problems I was having, I probably screwed up an update or install. I was also worried about it having died a slow thermal death with the heat sync fan having failed or decades old thermal paste flaking away. But to the touch, it wasn't any warmer than normal, and I could see, hear, and feel the fan spinning.

Luckily I always keep a live boot USB of Ubuntu for emergencies like this. And with it I was able to extract all the relevant data that I needed to backup, downloaded the latest Ubuntu, and re-image another USB drive to start the install. Overall it took me about 3 hours to get from installation to casual web browsing.

If there's one take away from all this, it's that you should always have a bootable USB drive available. It allows you to test whether issues are software or hardware, and allows you to have a working OS to get what you need in the mean time.