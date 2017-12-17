# bdl
Easily and quickly download a batch of files using wget.

**MASTER** - _Hopefully stable branch._\
**DEV** - _Development Branch (latest changes)_

INTRODUCTION
------------

One of the things I liked about my old Windows days is how easy I found it to get downloaders. I wanted a similar program in Linux, and I prefer to write my own stuff when I can, so here comes bdl (Batch Downloader). This program will simply download -- with wget -- from directory links specified in a file you can edit with your chosen editor, such as *vim* or *nano*. It's simple, but useful.

As bdl uses *wget* (see *man wget(1)* for more info), a utility installed on most systems by default, bdl will resume downloading where it left off, should the connection be at any point lost. You'll have the option to suspend or shutdown the machine after downloading is completed, and/or to notify you via notify-send, if installed.

Editing or emptying the list of downloads is as easy as `bdl --edit` or `bdl --empty`, respectively.

INSTALLATION
------------

Visit the installit repository to use the easy-to-use TFL downloader.
