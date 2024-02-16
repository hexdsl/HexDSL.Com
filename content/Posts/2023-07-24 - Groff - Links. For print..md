---
Class: Blog
Status: Not_set
Priority: Medium
Created: 2023-07-24
---

📆 Post date: 24-07-2023 
Originally posted on reddit - [Links. For print.](https://www.reddit.com/r/groff/comments/agkgqn/links_for_print/)

I was asked about embedding link into groff documents a few weeks ago, I wrote [this](https://www.reddit.com/r/groff/comments/ac7tkb/clickable_web_links_in_your_final_pdf/) outlining how that is accomplished and while its still the ideal way to deal with *clickable* links there is a better way of dealing with links for printed documents (my use case)

The result of this code will be TEXT(URL) the URL is (by default) is a very well defined Currier like font

The first thing you will need to do is to call in the World Wide Web (WWW) macro set. I have come to realise that rather than doing this with flags you can just pull it in from inside your file (this makes the file more robust and portable)

We do this with the .mso command (please note this is case sensitive.) You maybe familiar with the .so command (Source Other, its for calling a file.) In this case we use the .mso command to specify that we are calling a macro file (this does not require a full address as it know where macro files are kept by default)

```
.mso www.tmac
```

This calls the World Wide Web tmac file (TMAC refers to 'Troff Macro') Now your document knows how to use this macro set. You should put this at the top of your document.

Now we use the .URL operator to show firstly the URL then a space and the name of the site (or other comment)

```
.URL http://www.hexdsl.com/ HexDSL
```

You can do this at any point in your document, as long as the .URL is UPPER CASE (mostly this is easy to remember, if you are calling commands that a are built into groff then we use lower case and UPPER CASE for Macro set commands, okay, that's not *that* easy but it helps me remember)

Here is a basic example document outlining all of this in one go (as well as couple of other things that have already been covered on [/r/groff](https://www.reddit.com/r/groff))

```
 .mso www.tmac

.TL

THIS IS A TEST DOCUMENT

.AU

/r/groff

.LP

Hello this is a test documnent that I have written. have you visited my

website? heres a link (for print, not for clicking)

.URL http://xpenguin.club XPenguin

.LP

Thank you for reading this!
```

You can read more about this as well as get a groff core command reference by checking the man page on your computer

``` 
man groff
```

If you are not running GNU/Linux or BSD then please install it. Then try the command again.


---


> [!info] Note
> This Was written by HexDSL, if this was liked by you, you can email him at [Hexdsl@gmail.com](mailto:hexdsl@gmail.com) or use [this link](https://discord.hexdsl.com) to join Discord

#Blog #groff 