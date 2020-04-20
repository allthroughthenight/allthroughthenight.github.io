---
layout: post
title: "Networking Board"
---

As a somewhat avid [homelabber](https://www.reddit.com/r/homelab), I've all had the dream of 'maxing out'. Imagine, my own personal closed server rack, full of servers doing my bidding in a garage or basement. With a bespoke-built cooling solution that was whisper quiet, but strangely efficient. The clients on my LAN would enjoy trasparent ad-blocking, and voraciously consume entertainment media with blisteringly fast inter-connectivity with a multi terabyte NAS with [SFP](https://en.wikipedia.org/wiki/Small_form-factor_pluggable_transceiver) interfaces and switches. And to feed this hungry network, I would have a fiber optic connection from my ISP, with no less than a gigabit connection. That, is the end game.

But having lived life a bit, I've realized that simpler is usually better (and cheaper). When I get home, I just want things to work. But I do like having control over my domain, and saving a bit a money. So instead of renting my [SOHO](https://www.lifewire.com/soho-routers-and-networks-explained-3971344) router from my ISP, I figured I would do it myself.

I started by looking for compatible devices, and set a budget based on average pricing. Then when my budget was ready, I started working on the [networking board](https://duckduckgo.com/?q=home+network+board&amp;ia=images&amp;iax=images). I was originally inspired by the video done by Linus Tech Tips. It overall resonated with me since 1) I have a corner of networking stuff that's piled up a needed to be organized and 2) I'm a renter so I can't drill holes everywhere.

Overall I'm satisfied with how it turned out. I don't think the cost savings alone are worth it, but I like having control of my devices, so I don't have to worry about any weird box an ISP forces me to use but I still have to pay for.

My next goal is to flash my Linksys WRT with [openWRT](https://openwrt.org), but I've only had it for a few months, so I'd like to enjoy everything working before I risk bricking it. And I didn't bother with cable management either. Partly because knowing myself, I'll change everything in a few months. So instead I focused on securing everything simply so that it'd be easy to adjust later.

<div class="wp-block-embed__wrapper">
https://www.youtube.com/watch?v=saD_SFOYCWk
</div>

###### The inspiration

<p><!-- /wp:core-embed/youtube --></p>
<p><!-- wp:image {"align":"center","id":518,"sizeSlug":"large"} --></p>
<div class="wp-block-image">
<figure class="aligncenter size-large"><img src="{{ site.baseurl }}/assets/networking-board.jpg?w=768" alt="" class="wp-image-518" />
</figure>

###### The final build, with everything secured

<p><!-- /wp:core-embed/youtube --></p>
<p><!-- wp:image {"align":"center","id":518,"sizeSlug":"large"} --></p>
<figure class="aligncenter size-large"><img src="{{ site.baseurl }}/assets/network-diagram.png?w=346" alt="" class="wp-image-519" />
</figure>

###### A diagram of the board, done with [draw.io](https://app.diagrams.net)