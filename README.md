# bdl
Easily and quickly download a batch of files using wget.

INTRODUCTION
------------

One of the things I liked about my old Windows days is how easy I found it to get downloaders. I wanted a similar program in Linux, and I prefer to write my own stuff when I can, so here comes bdl (Batch Downloader). This program will simply download -- with wget -- from directory links specified in a file you can edit with your chosen editor, such as *vim* or *nano*. It's simple, but useful.

As bdl uses *wget* (see *man wget(1)* for more info), a utility installed on most systems by default, bdl will resume downloading where it left off, should the connection be at any point lost. You'll have the option to suspend or shutdown the machine after downloading is completed, and/or to notify you via notify-send, if installed.

Editing or emptying the list of downloads is as easy as `bdl --edit` or `bdl --empty`, respectively.

INSTALLATION
------------

No package manager needed here. Load up a terminal on your Linux (BSD and Mac may also work) system, then run the following commands on the *bdl* file (the program/script) you got from this repository. These commands will change the permissions to the standard expected of executables found in *PATH*. If you're concerned or curious, see *man chmod(1)* and *man chown(1)*.

As a safety measure, please run the first command here BEFORE the others, to ensure that you don't overwrite anything:

    [ -f /usr/bin/bdl ]; echo $?
    
If you see a "1" after running that, you can run these:

    sudo chown root:root bdl
    sudo chmod 755 bdl
    sudo mv bdl /usr/bin/
    
You can of course place the executable anywhere you like, but it works best in a standard location within *PATH*. To uninstall bdl, it's even easier:

    sudo rm /usr/bin/bdl
