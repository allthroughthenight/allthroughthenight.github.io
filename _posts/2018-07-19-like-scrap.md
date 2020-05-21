---
layout: post
title: "Like Scrape?"
---

Due to seasonal work, I spend days at a time without any internet access and have hours of free time. I have an e-reader that I've loaded up with books, but sometimes I want to zone out and enjoy some junk food for the mind.

I'm not new to having to bulk media downloads, but my past efforts have been almost entirely manual. For Youtube, I'd look for any downloading site or application, open as many tabs as I could, slow down my browser, do something else while it's busy, then come back and start it all over. For movies I'd use a bit torrent client, load multiple trackers, then adjust bandwidth usage and get a few movies over a few days.

At the time all those methods worked for the knowledge I had at the time. But now that I have more expirience I knew I could do it better.

One of the most popular tools for getting Youtube videos is [youtube-dl](https://ytdl-org.github.io/youtube-dl/index.html). There are enough write-ups on how to get up and running, and adding instructions wouldn't improve the quality of this post, but what I will give you is the command I used to download playlist, number them in order, and make a manifest so downloads can be stopped and restarted later.

```
$ youtube-dl --extract-audio --download-archive archive.txt --youtube-skip-dash-manifest --audio-format mp3 -o "%(playlist_index)s-%(title)s.%(ext)s" (youtube-url)
```

In closing, it only took an afternoon instead of a week to get all the media I'd need to enjoy myself. Don't suffer trying to do it the hard way, learn a bit and do the easy way.