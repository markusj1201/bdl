# bdl
Easily and quickly download a batch of files using wget.

**MASTER** - _Hopefully stable branch._\
**DEV** - _Development Branch (latest changes)_

## INTRODUCTION

One of the things I liked about my old Windows days is how easy I found it to get downloaders. I wanted a similar program in Linux, and I prefer to write my own stuff when I can, so here comes bdl (Batch Downloader). This program will simply download -- with wget -- from directory links specified in a file you can edit with your chosen editor, such as *vim* or *nano*. It's simple, but useful.

As bdl uses *wget* (see *man wget(1)* for more info), a utility installed on most systems by default, bdl will resume downloading where it left off, should the connection be at any point lost. You'll have the option to suspend or shutdown the machine after downloading is completed, and/or to notify you via notify-send, if installed.

Editing or emptying the list of downloads is as easy as `bdl --edit` or `bdl --empty`, respectively.

Here's the --help output, as of 4th March, 2018:

```
$ bdl --help
            BDL - BATCH DOWNLOADER (2018-03-04)
            Written by terminalforlife (terminalforlife@yahoo.com)

            Easily and quickly download a batch of files using wget.

SYNTAX:     bdl [OPTS]

OPTS:       --help|-h|-?            - Displays this help information.
            --version|-v            - Output only the version datestamp.
            --debug|-D              - Enables the built-in bash debugging.
            --insert|-I LINK        - Quickly append a link to the download list.
            --dest|-d PATH          - Where PATH is the location to download.
            --editor|-E CMD         - Where CMD is the command for your editor.
            --suspend|-s            - Immediately suspend machine when finished.
            --shutdown|-S           - Like above, but a shutdown after 1 minute.
            --notify|-N             - Use notify-send to inform of bdl completion.
            --edit|-e               - Change URL list with an available text editor.
            --clear|-C              - Empty the bdl download list entirely.

FILE:       All files are found in '$HOME/.bdl'.

TIP:        You can specify the destination for your downloads on a per-download
            basis, all you need to do is append the destination path to the end of
            the line with the direct download URL.

            Those destination paths given (per the above tip) currently do not
            support variables, such as the environment variables $HOME and $USER.
```

## INSTALLATION

Visit the installit repository to use the easy-to-use TFL downloader.
