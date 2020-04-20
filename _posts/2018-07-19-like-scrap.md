---
layout: post
title: "Like Scrape?"
---

Due to some seasonal work that I have, I can spend days at a time without internet access. Though not a big deal on it's own, I can also have hours of free time with nothing to do. In short, I need to keep myself entertained offline. I have an e-reader that I've loaded up with books, and I can devour them voraciously when I get into them. But sometimes you want to veg out and enjoy some junk food for the mind.

I'm not new to having to bulk download media for offline consumption, but past efforts have been very laborious and not very efficient. For Youtube, I'd look for any downloading site or application, enter each URL manually, clog up the internet and jam up my browser, go do something for a few hours while everything downloaded, then come back and start it all over. As for movies, I'd be like any other pirate and use a bit torrent client, load multiple trackers, then adjust bandwidth usage and get a few movies over a few days.

And in my ignorance, all those methods worked great working with the knowledge I had at the time. But after getting a degree, and having more Linux experience, when the time arose to acquire a bunch of media again, I knew I'd do it better.

One of the most popular tools for getting Youtube videos is [youtube-dl](https://ytdl-org.github.io/youtube-dl/index.html). There are enough write-ups on how to get up and running, and adding instructions wouldn't improve the quality of this post, but what I will give you is the command I used to download playlist, number them in order, and make a manifest so downloads can be stopped and restarted later.</p>

```
$ youtube-dl --extract-audio --download-archive archive.txt --youtube-skip-dash-manifest --audio-format mp3 -o "%(playlist_index)s-%(title)s.%(ext)s" (youtube-url)
```

As for other materials for my alone time, [RipMe](https://github.com/ripmeapp/ripme)is a very powerful tool that works for almost any site you can think of. One thing to remember is that if you're trying to separate picture albums RipMe doesn't do it automatically. For that, below is a short 26 line script that helps solves that.

```python
# library to use shell commands
from subprocess import call

# open file of directory listing
inf = open('list.txt')

# for each line within the directory listing file
for line in inf:
    
    # remove trailing new line
    line = line.rstrip()

    # make a directory for each line i.e. each collection
    call(["mkdir", line])

    # get all fils of a collection by taking prefix
    # and adding wildcard to the end to match all
    fileName = line + "*"

    # compose shell command as single string
    finalCall = "mv " + fileName + " " + line

    # exec command with 'shell=True' so that
    # '*' is read as wildcard like in the shell
    call(finalCall, shell=True)
    
# close file reader
```

Photos in collections have identical leading strings, and using that, any time there are more that two files  with a match, the script will make a directory and move any matching files into there.

In closing, it only took an afternoon instead of a week to get all the media I'd need to enjoy myself. Why suffer trying to do it the hard way, when you can read up and educate yourself and make it easier. The former seems easier in the short term, but the latter is easier in the long term.