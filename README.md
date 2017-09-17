# bdl
Easily and quickly download a batch of files using wget.

INTRODUCTION
------------

One of the things I liked about my old Windows days is how easy I found it to get downloaders. I wanted a similar program in Linux, and I prefer to write my own stuff when I can, so here comes bdl (Batch Downloader). This program will simply download -- with wget -- from directory links specified in a file you can edit with your chosen editor, such as *vim* or *nano*. It's simple, but useful.

As bdl uses *wget* (see *man wget(1)* for more info), a utility installed on most systems by default, bdl will resume downloading where it left off, should the connection be at any point lost. You'll have the option to suspend or shutdown the machine after downloading is completed, and/or to notify you via notify-send, if installed.

Editing or emptying the list of downloads is as easy as `bdl --edit` or `bdl --empty`, respectively.

INSTALLATION
------------

Download and use the `install_bdl` installer by using this terminal command:

```bash
wget -cq https://raw.githubusercontent.com/terminalforlife/bdl/master/install_bdl
```

Now execute the installer with this:

```bash
sudo bash install_bdl
```

Or if you prefer, make it executable, then more easily run it like so:

```bash
chmod u+x install_bdl
./install_bdl
```

Example installation of bdl:

    ➤  chmod u+x install_bdl
    ➤  sudo ./install_bdl
    L096: Checking conflict: /usr/bin/bdl
    L108: Downloading here: /usr/bin/bdl
    L112: Correcting attributes: /usr/bin/bdl

Example uninstallation of bdl:

    ➤  sudo ./install_bdl --uninstall
    L087: Uninstalling program.
    L118: Sending to trash: /usr/bin/bdl
