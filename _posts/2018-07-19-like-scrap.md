---
layout: post
title: "Like Scrape?"
---

Due to seasonal work, I can spend weeks at a time without internet access with a lot of free time. I have an e-reader that I've loaded up with books, but sometimes I want to enjoy something else.

I've bulk downloaded media before, but past efforts have been mostly manual. For Youtube, I'd look for any downloading site or application, open as many tabs as I could, copy-and-paste each video link into each tab, then just wait for them to finish. For movies I'd use a bit torrent client, load multiple trackers, then adjust bandwidth usage and get a few movies over a few days.

At the time all those methods worked with what I knew at the time, but I have more experience now so I can do better.

One of the most popular tools for getting Youtube videos is [youtube-dl](https://ytdl-org.github.io/youtube-dl/index.html). There are enough write-ups on how to use it, but what I will give you is the command I use to download playlist, number them in order, and make a manifest to keep track of what's been downloaded I can pause and resume it as needed.

```
$ youtube-dl --extract-audio --download-archive archive.txt --youtube-skip-dash-manifest --audio-format mp3 -o "%(playlist_index)s-%(title)s.%(ext)s" (youtube-url)
```

In closing, it only took an afternoon instead of a week to get all the media I'd need to enjoy myself. Don't suffer trying to do it the hard way, learn a bit and do the easy way.