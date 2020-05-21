---
layout: post
title: "Adventures in Recovery"
---

We've all deleted a file we didn't mean to, and it happen to me recently. I have some surface level experience in data recovery, a lot of it theory based and almost none of it practical. This post will be about that late night misadventure.

In short, I use an application on my phone that makes it an FTP server and allows me to manage files over wifi. It's a great since I just open my phone, start the sever, and do what I need to on my computer with a full monitor, mouse, and keyboard.

I needed to move some photos from my phone to my computer. Very routine, nothing special, and that's what made it dangerous. I made the mistake of thinking that the files were already transfered without refreshing, so I deleted it them from my phone and went on with my evening.

Later on when it came time to work with the photos I couldn't find them in my downloads folder on my computer, and that's when the panic set in. My initial move was to connect my phone via USB and try some data recovery tool. But due to the limited space on my phone, I put majority of my media onto the SD card which can't be directly accessed through the phone's USB port. So I shut down my phone, removed the SD card, and used my laptop's SD card slot. Unfortunately my SD card reader firmware was out of date and I couldn't update it properly.

The fix I came across had me manually compiling and building the .deb file. But as I kept reading, I realized "I'm probably not the first person on the planet that deleted a file by accident on their phone". A quick Play Store search brought up a few apps, I installed the first one and got to work. It seemed like it'd do what I needed to do, but what caught me off guard was a hidden directory called [face](https://www.reddit.com/r/Android/comments/2jm9j7/i_found_a_hidden_folder_called_face_on_my_phone/). I was initially worried that my device had been compromised, especially since my device is rooted. After reading about it, it's a directory made by Samsung to have reference material for their own face recognition software. Though it's not malicious, it was definitely creepy, and deleting it freed up a lot of internal storage.

In closing, I was able to recover the photo using an Android app. Unfortunately I wasn't able to recover the whole photo and was only able to get part of it, with the rest of it being corrupted. But a better solution would've been to just pay attention in the first place.