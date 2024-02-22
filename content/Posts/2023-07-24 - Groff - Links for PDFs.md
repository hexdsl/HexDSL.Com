---
draft: false
date: 2023-07-24
tags:
  - website
---

📆 Post date: 24-07-2023

Originally posted on Reddit [Clickable web Links in your final PDF!](https://www.reddit.com/r/groff/comments/ac7tkb/clickable_web_links_in_your_final_pdf/)

Today I was asked how you create clickable links in a PDF document, the truth is I had NO IDEA! I use groff for long form documents and it had never occurred to me that this is something I would want.

So I went and found out!

The Documentation should be found in a PDF file called 'pdfmark.pdf' in '/usr/share/doc/groff??????/' - its worth knowing that on Antergos/Arch Linux the documentation folder was missing until I moved to the 'groff-git' package (I have no idea why!)

Firstly you must compile wit the '-pdfmark' flag (-ms -pdfmark -tbl etc..) and here is some working sample code (I have verified this as working! - however, unsure if this is related to the implementation but it was quite slow to load, maybe more due to Zathura/QuteBrowser)

```
 .TL
THIS IS THE TITLE! OMG TITLE!
.NH
Headers are cool!
.LP
THIS IS SOME TEXT!
.pdfhref W -D http://www.gnu.org/software/groff -A , the groff web site
a great website!
```

I have now created multiple documents and this has worked perfectly each time.

Hope this helps. For more information please check the pdfmark.pdf file located in /usr/share/doc/groff/ (if its not there upgrade to groff-git package.)

---

> [!info] Note
> This Was written by HexDSL, if this was liked by you, you can email him at [Hexdsl@gmail.com](mailto:hexdsl@gmail.com) or use [this link](https://discord.hexdsl.com) to join Discord

