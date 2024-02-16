
📆 Post date: 24-07-2023 

Originally posted in Reddit - [Basic TABLE (including examples)](https://www.reddit.com/r/groff/comments/abndkt/basic_table_including_examples/)

Tables are a little confusing at first (mostly due to example files being terrible) The below is an easy to understand example of a simple table. this one uses ';' as a separator and is all encased in boxed borders, both columns are left aligned.
```
 .TS
tab(;) allbox;
l,al.
HEADER 1;HEADER 2
BIG; Feet
Small; DOG
Cheshire; Cat
Sexy; Duck
.TE
```

Copy this into a file called (for example) example.ms and run the following command...

```
groff -ms -tbl -T pdf sample.ms > sample.pdf
```
  
Now load your nice new PDF in your preferred reader (i Use zathura) and you will (should) instantly be able to decipher the code (once you see it, its honestly pretty self explanatory)
For more information and an explination on this topiic beyond this simple explenation please check the man page for tbl.
```
man tbl
```

I hope this basic guide helps you to understand tables


---

> [!info] Note
> This Was written by HexDSL, if this was liked by you, you can email him at [Hexdsl@gmail.com](mailto:hexdsl@gmail.com) or use [this link](https://discord.hexdsl.com) to join Discord

#Blog #groff