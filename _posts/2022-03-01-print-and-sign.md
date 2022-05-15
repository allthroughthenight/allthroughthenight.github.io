---
layout: post
title: "Print and Sign"
---

I was asked to sign and return some legal documents, Foxit and Adobe have a signature stamp feature, so I can sign digitally. But since these were legal documents, I was asked to provide an real signature. I didn't want to go down to an Officer Store just to print, sign, and scan them, so I went back through some [hn](https://news.ycombinator.com/) post that mentioned how to fake a real signature.

[This](https://news.ycombinator.com/item?id=23160387) and [this](https://news.ycombinator.com/item?id=31083432)post sshow online service that do what you need. But since my documents had sensitive information I didn't feel comfortable uploading them. Reading the posts more, then had some good comments on how to do the same locally.

I first tried [this](https://news.ycombinator.com/item?id=23161664) command but it looked a bit too processed.

> convert -density 150 <input-file.pdf> -colorspace gray -linear-stretch 3.5%x10% -blur 0x0.5 -attenuate 0.25 +noise Gaussian -rotate 0.5 temp.pdf

I ended up going with [this](https://news.ycombinator.com/item?id=23160387) command which was more of a light touch.

> gs -dSAFER -dBATCH -dNOPAUSE -dNOCACHE -sDEVICE=pdfwrite -sColorConversionStrategy=LeaveColorUnchanged -dAutoFilterColorImages=true -dAutoFilterGrayImages=true -dDownsampleMonoImages=true -dDownsampleGrayImages=true -dDownsampleColorImages=true -sOutputFile=<output-file.pdf> temp.pdf

Another thing I didn't expect was that the PDF program you use to make the signature stamp has an impact as well. I'm a Foxit reader user, but for this process making the signature with Adobe will give you a much better result.

After spending an entire morning testing all of this, I felt ready to send my signed and scanned document. After I attached the document, before I typed my response I re-read the email and it said "Please provide an original signature". This seemed like a weird way of saying a real signature, so after looking it up I learned that [original signature](https://www.lawinsider.com/dictionary/original-signature) is an actual legal term. 

It seemed like all this work was for waste, I spend an entire morning making a whole new environment, dealing with dependencies, keeping track of the all the various signatures and documents I was testing. But the silver lining is that at lease I read that line, instead of submitting it and having to wait another week just to be told I needed to resubmit it. And now if someone asks me to print and sign something I'll have everything ready to get it done.

Since I'd have to sign the document I went down to the Office Store, which is usually empty, but the day I went had a line to use the printers. Also I'm used to nobody caring about the printers, but again, there was people waiting to use them as well. I'm used to the process taking ~5 minutes at most since I'll print from USB, and most of that time is just confirming the printer settings. This time took almost an hour total to get everything done.

I have an old HP multi-purpose inkjet printer. It never prints when I need it to, and I've only kept for the scanner. I digitize any document I have that's worth keeping and filing. So looking at both these problems I decided to go with the [hn recommendation](https://www.google.com/search?hl=en&q=hacker%20news%20printer%20recommendations) and get a Brother laser printer. 

At first I almost went with a combo printer-scanner, then realized I scan a lot more than I print, and got them as separate devices. For the printer I went with a [Brother HL-L2350DW](https://www.amazon.com/dp/B0763WDSYZ). I decided to spend the extra ~$50 for wireless printing, and save ~$80 to miss out on wired connectivity, but avoid having to run another ethernet cable around my office.

For my scanner, following hn recommendations again, they said that the The New York Times Wirecutter series has a list for [scanners](https://www.nytimes.com/wirecutter/reviews/the-best-cheap-scanner/), and I went with the [Canon CanoScan Lide 300](https://smile.amazon.com/dp/B07G5XZVLQ).

