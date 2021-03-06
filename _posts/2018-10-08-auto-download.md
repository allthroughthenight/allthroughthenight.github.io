---
layout: post
title: "Auto Download"
---

I'm a big fan of virtualization for the average tech person because:

* You're to not be tied to specific hardware
* You learn good data back-up and storage habits

One of the best virtualization tools available for free is [Virtual Box](https://www.virtualbox.org), which can be combined with [Vagrant](https://www.vagrantup.com). As much as I'm a fan of virtualization, I'm not a fan of most streaming services. and would rather keep my media off-line to view whenever. Though torrenting is an option, most media can be found on YouTube. Considering it's the [second largest search engine](https://www.mushroomnetworks.com/infographics/youtube---the-2nd-largest-search-engine-infographic/), why not use a tool catered to scarping it. [Youtube-dl](https://youtube-dl.org) solves this problem and then some. By having to ability to run from the command line and operate from input files unattended, it offers a lot of freedom for bulk downloading.

The basics steps are below:
1. Collect URLs of things I want
2. Put them into a plain text document, one link per line
3. Run the following command

```
youtube-dl --extract-audio --download-archive archive.txt --youtube-skip-dash-manifest --audio-format mp3 -i -o "%(title)s.%(ext)s" -a <youtube-urls-files>;
```

In summary, it reads URLs line-by-line from a file, downloads audio only, convert the download to mp3, and keeps track of whats already been downloaded in case the download has to be stopped and started again.

But once you download everything you need to move all the files around. Vagrant allows for [synced folders](https://www.vagrantup.com/docs/synced-folders/basic_usage.html), which let you share a directory that both machines can access. So once a job is complete you can shut down the VM and enjoy your sweet free media on your host machine with no fuss.