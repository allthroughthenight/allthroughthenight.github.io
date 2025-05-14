---
layout: post
title: "Wordpress Migration"
---

I finally migrated my blog from [Wordpress.com](https://www.wordpress.com) to [GitHub pages](https://pages.github.com/). I could've started with GitHub pages, but I just wanted to get going. And now that things have been going, it's time to take the next step.

First I had to export my posts from Wordpress. Self-hosted sites allow you to install your own add-ons, like [jekyll-exporter](https://wordpress.org/plugins/jekyll-exporter) but I was using their free tier and went with the [built-in](https://wordpress.com/support/export) exporter.

To convert the export to markdown, I used [https://github.com/jekyll/jekyll-import](https://import.jekyllrb.com/docs/installation/). Not all the posts converted perfectly so I went back through to remove in-line HTML and asset linking.


I don't think I'll have other pages (About Me, Contact, Porfolio/Resume) for now. The main goal of this is to journal my technical learning and improve my writing, so I'll worry about those later.