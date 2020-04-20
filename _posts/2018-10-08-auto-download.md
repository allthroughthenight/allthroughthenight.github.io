---
layout: post
title: "Auto Download"
---

I'm a big fan of making virtualization possible for the everyday person. The biggest reason are:

* Allows you to not be tied to any hardware
* Teaches good data back-up and storage habits

With enterprises moving to thin client models, we could see the same arrive in the home. But the home personal computing market is dwindling with everything being able to be done with mobile devices.

One of the best virtualization tools available for free is [Virtual Box](https://www.virtualbox.org), which can be combined with [Vagrant](https://www.vagrantup.com), a headless hypervisor. Vagrant is really meant for making repeatable and predictable development, testing, production environments, but depending on what OS you install, you can do legitimate work with a box.

As much as I'm a fan of virtualization, I'm not a fan of most streaming services. With the freedom of the internet constantly on the line, I'd much rather have the ability to keep my media off-line for consumption anywhere. Though torrenting is an option, most media can be found on any main stream website. Considering YouTube is the [second largest search engine](https://www.mushroomnetworks.com/infographics/youtube---the-2nd-largest-search-engine-infographic/), why not use a tool catered to scarping it. [Youtube-dl](https://youtube-dl.org) solves this problem and then some. By having to ability to run from the command line and operate from input files unattended, it offers a lot of freedom for bulk downloading. The basics steps are below:

1. Collect URLs of things I want
2. Throw them into a plain text document, one link per line
3. Run the following command

```
youtube-dl --extract-audio --download-archive archive.txt --youtube-skip-dash-manifest --audio-format mp3 -i -o "%(title)s.%(ext)s" -a &lt;youtube-url&gt;
```

The tl;dr of the command is that it reads URLs from a file (expecting one per line), and keeps track of what has and been downloaded. So if something fails or you want to start later, you can re-run the same command and it'll skip what it already has.

So now we have our VM and our tool, but how to we move files around? You could use an FTP client like [FileZilla](https://filezilla-project.org), but considering both devices are on the same hardware, why not share a location? Vagrant allows for [synced folders](https://www.vagrantup.com/docs/synced-folders/basic_usage.html), which let you share a directory that both machines can access. So now once a batch is complete you can shut down the VM and enjoy your sweet free media on your host machine with no fuss.