---
layout: post
title: "Print and Sign"
---

I was asked to sign and return some legal documents. Foxit and Adobe let you sign digitally with their signature stamp feature. But since these were legal documents I was asked for a real signature. I didn't want to go down to the Officer Store to print, sign, and scan it, so I went back through some [hn](https://news.ycombinator.com/) posts that showed how to fake a real signature.

[This](https://news.ycombinator.com/item?id=23160387) and [this](https://news.ycombinator.com/item?id=31083432) post show services that do what you need. But since my documents has sensitive information I didn't want to upload them. Reading the posts more, they had comments on how to do the same locally.

I tried [this](https://news.ycombinator.com/item?id=23161664) command but it looked too processed.

> convert -density 150 <input-file.pdf> -colorspace gray -linear-stretch 3.5%x10% -blur 0x0.5 -attenuate 0.25 +noise Gaussian -rotate 0.5 temp.pdf

I ended up with [this](https://news.ycombinator.com/item?id=23160387) command that was more of a light touch.

> gs -dSAFER -dBATCH -dNOPAUSE -dNOCACHE -sDEVICE=pdfwrite -sColorConversionStrategy=LeaveColorUnchanged -dAutoFilterColorImages=true -dAutoFilterGrayImages=true -dDownsampleMonoImages=true -dDownsampleGrayImages=true -dDownsampleColorImages=true -sOutputFile=<output-file.pdf> temp.pdf

I didn't expect the PDF program you use to make a difference with the digital signature stamp. Between Foxit and Adobe, the later gave a much better result.

After spending all morning figuring this out, I was ready to send my pseudo signed and scanned document. I attached the document, then while typing my response I re-read the email and it said "Please provide an original signature". This seemed like a weird way of saying a real signature, so after looking it up I learned that an [original signature](https://www.lawinsider.com/dictionary/original-signature) is a actual legal term. 

Was all this work was for waste? I spent all morning making a new environment, dealing with dependencies, keeping track of signatures and documents, only to realize it didn't matter. A silver lining is that at least I read that line before submitting, instead of waiting for a response to get rejected again. And now if someone asks me to print and sign something I'll be ready.

I went down to the Office Store to print the document out, which is usually empty, but this day there was a line to use the printers. What would usually take ~5 minutes ended up being almost an hour.

I have an HP multi-purpose inkjet printer. It never prints when I need it to, and I've only kept it for the scanner. Looking at both problems, I decided to go with the [hn recommendation](https://www.google.com/search?hl=en&q=hacker%20news%20printer%20recommendations) and get a Brother laser printer. 

I almost went with a combo printer-scanner, then realized I scan a lot more than I print, and got them as separate devices. For the printer I went with a [Brother HL-L2350DW](https://www.amazon.com/dp/B0763WDSYZ).

For my scanner, the The New York Times Wirecutter series has a list of [scanners](https://www.nytimes.com/wirecutter/reviews/the-best-cheap-scanner/), and I went with the [Canon CanoScan Lide 300](https://smile.amazon.com/dp/B07G5XZVLQ).

Both make getting stuff done a lot easier now. This type of office set up is kind of overkill for most, but when it comes to those few times I need it, it's worth it.