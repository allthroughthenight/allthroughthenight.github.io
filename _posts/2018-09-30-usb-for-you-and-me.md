---
layout: post
title: "USB for You and Me"
---
My workhorse of a laptop, an X230 Thinkpad, had gotten me through my undergrad career, two jobs, and an internship. Since buying it I've double the RAM from 4 to 8 GBs, and swapped the hybrid 500GB HDD for a 128 SSD. Both were well spent and increased the performance greatly.

During my move into a new place for my new job, I damaged my desktop PC's power supply. At the time the symptoms seemed more like it could've been the motherboard or even the CPU. But instead of ordering any parts, it'd be easier to just make the 1 hour and 20 minute drive to the nearest Frys electronics store and troubleshoot in-store. But since my budget at the time was air tight, I had to wait a few paychecks. In the meantime it was just me and my X230. No games, just the terminal and web surfing.

For sake of convenience I'd leave it in hibernation instead of just turning it off. The SSD made both tasks comparably the same, but I thought it could handle being powered on 24/7. That was a mistake.

The first problem was loss of my internet connection. Usually not a big issue, the internet at my place sucks so I just run a ping command to see when it comes back up.

```
user at X230 in ~/temp
$ ping google.com
zsh: command not found: ping
```

Okay, not a big deal, maybe my paths aren't right. Let's just get the absolute path and call it from there

```
user at X230 in ~/temp
$ whereis ping
zsh: command not found: whereis<
```

Phew, okay, we'll let's just turn it off and on again. Little buddy's up time was pushing about two weeks straight.

```
No boot device is available, press Enter to continue
```

This isn't the first time I'd had a problem like this, but it was very inopportune since I only had one computer at the time. At first I thought I should try and test my laptop hardware with another hard drive, but thinking about the weird terminal problems I was having, I probably screwed up an update or install. I was also worried about it having died a slow thermal death with the heat sync fan having failed or thermal paste flaking away. But to the touch, it wasn't any warmer than normal, and I could see, hear, and feel the fan spinning.

Luckily I always keep a live boot USB of Ubuntu for emergencies like this. And with it I was able to extract all the relevant data that I needed to backup, download the latest version of Ubuntu, and re-image another USB drive to start the install.

Then as part of my new computer set up, I have a few scripts that help automate the process and get my most used programs. That, along with distributing my config and dotfiles the recovery took about 45 mins total. Not including the 3 hour it took to download of the latest Ubuntu ISO, and my spiral of negativity that all was lost.

If there's one take away from all this, it's that you should always have a bootable USB drive available. It allows you to test whether issues are software (primarily the OS) or hardware, and allows you to have a working OS to get what you need in the mean time. Also you should try and test your doomsday recovery plan before you actually need it since [no plan survives first contact.](https://en.wikiquote.org/wiki/Helmuth_von_Moltke_the_Elder)