---
layout: post
title: "Data Deception Despair"
---

The [NPD leak](https://www.theverge.com/2024/8/14/24220212/national-public-data-breach-social-security-3-billion) is the largest data leak of PII in American history. It includes phone numbers, addresses, emails, and full names. Those combined would allow most attackers to easily take over enough accounts to make some money. Instead the vector that attackers have chosen is a lot more impersonal.

For myself, it was a normal morning, till I saw the email below.

![]({{site.baseurl}}/assets/2025-03-01-data-deception-despair/email-01.png)

Becuase of my aggressive email filtering, getting an email to with my full name and address was surprising. I check all the info to confirm it wasn't a fluke (ignore the spam banner, that was after the fact).

I opened the attatchment in the browser and started reading.

![]({{site.baseurl}}/assets/2025-03-01-data-deception-despair/page-01.png)

The first part is still shocking, with my full name and address, along with a street vi- wait. I've looked at my place from street view enough to know where angle was from. Also I had our [Google street view removed](https://www.aarp.org/home-family/personal-technology/info-2021/remove-home-from-google-street-view.html). So that explains why the view is off angle. When their tool tried to get a view of my place it didn't work, and settled for an off angle instead. This is getting weirder, but let's keep reading.

![]({{site.baseurl}}/assets/2025-03-01-data-deception-despair/page-02.png)

Okay this is just some kind of extortion. I'm 98% sure I'm safe to ignore it, and I made sure not to download any attachments. If they have any tracking pixels in the email that's fine, but overall it feels about as dangerous as any other dodgey link.

A lot of the techno-bable is close enough at a glance, but once you go below surface level it all falls apart. And knowing a bit about cyber security and cyber crime, if they had a rootkit to any device, manually monitoring cameras and website history is too much work for an extortion. It'd be easier to do a ransomware attack or sniff for passwords.

I showed this to my partner and they just laughed immediatly after the first paragraph. Outside of my context which is "an email to my inbox is real" they saw through it right away. I deleted the email without incident, and looking around [this reddit](https://www.reddit.com/r/techsupport/comments/1ev091l/this_is_what_a_hackerscammer_is_sending_me/) post shows the same sentiments.

Overall the attack wasn't that sophisticated. But I could see it working on anyone who isn't as tech litterate. I've also avoided posting the exact text to prevent myself from getting flagged, filtered, or even boosted by others searching this up as well.

Data breaches are a big problem, and companies that aggregate public data are a danger because these situations can happen. I don't expect any effective legislature to take shape within my lifetime, but I hope in the future people can look back and say "that was bad, good thing we fixed it".