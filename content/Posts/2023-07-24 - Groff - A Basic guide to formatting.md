---
draft: false
date: 2023-07-24
tags:
  - website
---

📆 Post date: 24-07-2023

Originally posted on reddit - [A Basic guide to formatting (babies first groff)](https://www.reddit.com/r/groff/comments/aaowx3/a_basic_guide_to_formatting_babies_first_groff/)

# **Groff Guide**

The following is a very slimmed down list of basic groff commands using the MS macro set and Table pre-processor Examples of usage follow.

| COMMAND    | Explanation                                        |
| ---------- | -------------------------------------------------- |
| .TL        | Title                                              |
| .AU        | Author                                             |
| .NH N      | Heading (N = Subheading number)                    |
| .SH        | Sub Heading (not numbered)                         |
| .PP        | Paragraph                                          |
| .LP        | Non Indented Paragraph                             |
| .B "TEXT"  | Bold (.B "TEXT" AFTER BEFORE)                      |
| .I "TEXT"  | Italic (.I "TEXT" AFTER BEFORE)                    |
| .UL "TEXT" | Underline (.UL "TEXT" AFTER BEFORE)                |
| .BI        | Bold & Italic (.BI "TEXT" AFTER BEFORE)            |
| .BX "TEXT" | Boxed text                                         |
| .AB NO     | Abstract Begin (add no to suppress ABSTRACT title) |
| .AE        | Abstract End                                       |
| .TS        | Table Start (notes beginning of table area)        |
| .TE        | Table End (end of table area)                      |

EXAMPLES:

```
 .TL
```

**This is the titles of my document**

```
.AU
```

_I wrote this_

```
 .PP
```

 This text will be indented and the next line will not be intended, yeah, those dashes are to illustrate the intention and are totally not a result of the way markdown works in this editor (damn you reddit!, shakes fist)

```
.LP
```

This paragraph will start with no intent and often looks nicer for less formal documents, Its rather nice. However

```
 .B "this will be on BOLD"
```

but be on the same line as the rest

---

> [!info] Note
> This Was written by HexDSL, if this was liked by you, you can email him at [Hexdsl@gmail.com](mailto:hexdsl@gmail.com) or use [this link](https://discord.hexdsl.com) to join Discord


