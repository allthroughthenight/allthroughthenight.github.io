---
layout: post
title: "Wordpress Migration"
---

It's been a long time coming, but I was finally able to migrate my blog from [Wordpress](https://ramblevalley.wordpress.com) to [GitHub pages](https://pages.github.com/).
I could've just started with GitHub pages to begin with, but at the start I just wanted to get going.
And though Wordpress works for getting off the ground, I wanted to try in out on something I own a bit more.

My first move was to export my posts from Wordpress.
Self-hosted Wordpress.org sites allow you to install your own add-ons, like [jekyll-exporter](https://wordpress.org/plugins/jekyll-exporter) but I using a free Wordpress.com and would need to pay for that. So I just used their [built-in](https://wordpress.com/support/export) exporter.

For converting the export to markdown (for Jekyll), I used [https://github.com/jekyll/jekyll-import](https://import.jekyllrb.com/docs/installation/). Not all the posts converted perfectly to pure markdown, and I had to go back through to clean them up.

Since I use Vagrant as often as possible, making a Jekyll box was a given. There are some premade Jekyll boxes, but I'd rather just have my own Ansible playbook and not rely on maintainers.

Below is order list of tasks related to this, from most to lease
* Jekyll box set-up
* Converting export to markdown with a tool
* Cleaning up in-line HTML by hand

As of now, I don't think I'll have any pages, and just leave my public email, GitHub, and LinkedIn links in the footer.
I've thought about making an 'About', 'Contact', and mabye a sudo 'Resume' page.
But this isn't meant to be some big thing to me, and I don't want to have to maintain a LinkedIn profile, and a .docx resume, and the 'Resume' page.
I keep my LinkedIn up to day and check it every few weeks, and it has messaging so if someone wants to they can reach out.
If they don't like that, my public email is there also.
In my experience, if someone wants to contact you, they'll find a way.

