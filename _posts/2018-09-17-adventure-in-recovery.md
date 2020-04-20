---
layout: post
title: "Adventures in Recovery"
---

No matter who you are, where you're from, or what you do, we've all from time to time deleted a file we didn't mean to. Though I do my best to avoid it, it did happen to me recently. To complicate issues, it was on my mobile device instead of a computer. I have some surface level experience in data recovery, a lot of it theory based and almost none of it practical. This post will be about that fateful late night misadventure.

In short, I use an application on my phone that makes it an FTP server and allows me to manage files over wifi. It's a great help since I just open my phone, start the sever, do what I do on my computer, then stop the server on my phone. The problem is that with a phone, your pace is hindered by being stuck to a touch screen interface and your digits. While on a computer you can get a lot more done in the blink of an eye.

The task I need to complete was move some photos from my phone to my computer. Very routine, nothing special, and that made it all the more dangerous. I made the mistake of thinking that the file cue I was looking at was for new photos, but instead it was for past transfers. Thinking that I was done, I deleted the files, and went on with my evening.

About an hour later when it came time to work with the photos I saved I couldn't find them, and that's when the panic set in. My initial move was to connect my phone via USB and try some data recovery tool. But due to the limited space on my phone, I put majority of my media onto the SD card which can't be directly accessed through the phone's USB port. So I shut down my phone, removed the SD card, put it in an adapter, then into my laptops SD card slot. Unfortunately my SD card reader firmware was out of date and I couldn't update it properly.

The fix I came across had me manually compiling and building the .deb file. But as I kept reading, I realized "I'm probably not the first person on the plant to have deleted a file by accident on my phone". A quick Play Store search brought up a few apps, I install the first one and got to work. It seemed like it'd do what I needed to do, but what caught me off guard was a hidden directory called [face](https://www.reddit.com/r/Android/comments/2jm9j7/i_found_a_hidden_folder_called_face_on_my_phone/). I was initially worried that my device had been compromised, especially since my device is rooted. After reading about it, it's a directory made by Samsung to have reference material for their own face recognition software. Though it's not malicious, it was definitely creepy, and deleting it freed up a lot of internal storage.

In closing, I was able to recover the photo using an Android app though it wasn't that `1337 h4x0r`. Unfortunately I wasn't able to recover the whole photo and was only able to get part of it, with the rest of it being corrupted. But a better solution would've been to just pay attention in the first place.