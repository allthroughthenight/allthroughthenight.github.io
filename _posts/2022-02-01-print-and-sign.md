---
layout: post
title: "Print and Sign"
---

Looking back at my media consumption over the past few years I saw a few issues:

* [deep understanding in the long run.](https://news.ycombinator.com/item?id=29621642)

* ![]({{site.baseurl}}/assets/2021-03-01-my-interviewing-success/2016-internship-applications.png)


# use adobe if possible, else foxit

# initial pass
convert -density 150 <input-file.pdf> -colorspace gray -linear-stretch 3.5%x10% -blur 0x0.5 -attenuate 0.25 +noise Gaussian -rotate 0.5 temp.pdf

# final pass
gs -dSAFER -dBATCH -dNOPAUSE -dNOCACHE -sDEVICE=pdfwrite -sColorConversionStrategy=LeaveColorUnchanged -dAutoFilterColorImages=true -dAutoFilterGrayImages=true -dDownsampleMonoImages=true -dDownsampleGrayImages=true -dDownsampleColorImages=true -sOutputFile=<output-file.pdf> temp.pdf

https://news.ycombinator.com/item?id=23160387

https://news.ycombinator.com/item?id=31083432