---
layout: post
title: "Wordpress Migration"
---

I finally migrated my blog from [Wordpress.com](https://www.wordpress.com) to [GitHub pages](https://pages.github.com/). I could've just started with GitHub pages to begin with, but in the beginning I just wanted to get going. And now that things have been going, it was time to take the next step.

First I had to export my posts from Wordpress. Self-hosted sites allow you to install your own add-ons, like [jekyll-exporter](https://wordpress.org/plugins/jekyll-exporter) but I using a free site and used their [built-in](https://wordpress.com/support/export) exporter.

To convert the export to markdown, I used [https://github.com/jekyll/jekyll-import](https://import.jekyllrb.com/docs/installation/). Not all the posts converted perfectly, and I went back through some to remove the in-line HTML and asset linking.

Since I use Vagrant as often, making a Jekyll box for testing was a given. There are some premade Jekyll boxes available, but I'd rather just have my own Ansible playbook I could use on any machine.

I don't think I'll have any pages (About Me, Contact, Porfolio/Resume) for now, the main goal of this is to journal my technical learning and improve my writing, so I'll worry about them later.