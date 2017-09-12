# bdl
Easily and quickly download a batch of files using wget.

INTRODUCTION
------------

One of the things I liked about my old Windows days is how easy I found it to get downloaders. I wanted a similar program in Linux, and I prefer to write my own stuff when I can, so here comes bdl (Batch Downloader). This program will simply download -- with wget -- from links specified in a file you can edit with your chosen editor, such as *vim* or *nano*. It's simple, but useful.

MORE DETAILS
------------

As bdl uses wget, a utility installed on most systems by default, bdl will resume downloading where it left off, should the connection be at any point lost. Here is the *--help|-h|-?* output which might give you some ideas as to what you can do with it:

                BDL - Batch Downloader (9th September 2017)
                Written by terminalforlife (terminalforlife@yahoo.com)
    
                Easily and quickly download a batch of files using wget.
    
    OPTS:       --help|-h|-?            - Displays this help information.
                --debug|-d              - Enables the built-in bash debugging.
                --tohere=T              - Where T is the location to download.
                --editor=E              - Where E is the command for your editor.
                --verbose|-v            - Display wget's more verbose output.
                --suspend|-s            - Immediately suspend machine when finished.
                --shutdown|-S           - Like above, but a shutdown after 1 minute.
                --notify|-N             - Use notify-send to inform of bdl completion.
                                          Notifies only after all files are finished.
                --edit|-e               - Change URL list with an available text editor.
                --empty|-C              - Empty the bdl download list entirely.
    
    FILE:       All files are found in '$HOME/.bdl'.

INSTALLATION
------------

No package manager needed here. Load up a terminal on your Linux (BSD and Mac may also work) system, then run the following commands on the *bdl* file (the program/script) you got from this repository. These commands will change the permissions to the standard expected of executables found in *PATH*. If you're concerned or curious, see *man chmod(1)* and *man chown(1)*.

    sudo chown root:root bdl
    sudo chmod 755 bdl
    sudo mv bdl /usr/bin/
    
You can of course place the executable anywhere you like, but it works best in a standard location within *PATH*. To uninstall bdl, it's even easier:

    sudo rm /usr/bin/bdl
