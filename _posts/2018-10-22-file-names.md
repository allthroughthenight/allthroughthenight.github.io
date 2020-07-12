---
layout: post
title: "File Names"
---

File naming conventions are tough. Many try, few succeed. Just like variable naming, it leaves a lot open to [The Bike Shed Effect](http://bikeshed.com). Most default to the ALL_UPPER_AND_UNDERSCORES. Though simple to implement, it's a hassle to type. In my experience, having both cases helps with readability, and designers [Jock Kinneir & Margaret Calvert](http://www.britishroadsignproject.co.uk/jock-kinneir-margaret-calvert) would agree.

Also, organizations suck with standardizing how they want to write the time and date. Most are cultural i.e. day/month/year, year/month/day, etc. The problem with spelling out the month is that it doesn't organize well. And having month or day first groups everything too specifically. A better way is to have the year/month/day, starting broad then becoming more specific.

Considering how well that'd work, there's already a standard for it called [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) and it states that you just use the year, month, day. And if you want to be more specific, then you can add the time with hour, minute, seconds. This works great because then it organizes from largest to smallest, so you don't have to worry about weird grouping.