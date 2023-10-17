# Introduction

This was a tool that I wrote for use with `mutt` way back in the day; either
the very late 1990s or early 2000s. I forget which. What follows is the
original description for it.

## Original description

These days some people seem to be confusing web browsers with MUAs and news
readers. Like it or not, you've got to deal with it. One such MUA-wannabe is
Netscape. It seems that this Web Browser likes to make its users think they
don't need a traditional .sig and that they should use its "vcard" setup.

To cope with the fact that I get mail from people who use such a Web Browser
to send mail, and to allow me to correctly view the vcard data, I wrote
mutt.vcard.filter (you will need [perl](http://www.perl.org/) 5.x or better
to use it).

`mutt.vcard.filter` is used with mutt's auto_view facility. To use it I have
the following entry in my `~/.mutt/mailcap` (my local mutt-only mailcap
file):

```
text/x-vcard; mutt.vcard.filter; copiousoutput
```

All that is then needed is to add a line like:

```
auto_view text/x-vcard
```

to your `~/.muttrc` (use your filename of choice) file and everything should
work just fine. I don't think I catch everything in the filter, but it does
handle all of the information I'm interested in. If you have any
enhancements or comments then please feel free to mail them to me.

NOTE: It appears that the above filter can only deal with some forms of
vcard data from some versions of netscape (and other software). I've
downloaded the vcard specification and it's **big**. Don't expect me to
write a fully working vcard filter any time soon, it's not that important to
me.

[//]: # (README.md ends here)
