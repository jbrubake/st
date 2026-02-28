# st - simple terminal

`st` is a simple terminal emulator for X which sucks less.

## Requirements

In order to build st you need the `Xlib` header files.

## Installation

Edit `config.mk` to match your local setup (`st` is installed into the
`/usr/local` namespace by default).

Afterwards enter the following command to build and install `st` (if necessary
as root):

    make clean install

## Running st

If you did not install `st` with make clean install, you must compile the `st`
terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

The `st-urlhandler` script is written by [Luke Smith](https://github.com/LukeSmithxyz/st)

## Applied Patches

- st-anygeometry-0.8.1.diff : allows you to set st's width and height as pixels instead of cells
- st-anysize-0.8.4.diff : allows st to resize to any pixel size
- st-blinking_cursor-20200531-a2a7044.diff : allows the use of a blinking cursor
- st-clipboard-20180309-c5ba9c0.diff : sets CLIPBOARD on selection
- st-delkey-20201112-4ef0cbd.diff : return BS on pressing backspace and DEL on pressing the delete key
- st-externalpipe-0.8.4.diff : reading and writing st's screen through a pipe
- st-font2-20190416-ba72400.diff : allows to add spare font besides default
- st-osc10-20210106-4ef0cbd.diff : 
- st-rightclickpaste-0.8.2.diff : 
- st-scrollback-20210507-4536f46.diff : scroll back through terminal output using Shift+{PageUp, PageDown}
- st-scrollback-mouse-20191024-a2c479c.diff : allow scrolling using Shift+MouseWheel
- st-selectioncolors-0.8.4.diff : adds the two color-settings selectionfg and selectionbg
- st-undercurl-0.8.4.diff : adds support for special underlines
- st-visualbell2-basic-2020-05-13-045a0fa.diff : renders a configurable visual indication on terminal bell event
- st-visualbell2-enhanced-2020-05-13-045a0fa.diff : renders a configurable visual indication on terminal bell event.
- st-xresources-20200604-9ba7ecf.diff : adds the ability to configure st via Xresources

## Stay Synced with Upstream

After cloning this repo, add the upstream repository as a remote:

    $ git remote add upstream "https://git.suckless.org/st"

To merge changes from upstream:

    $ git fetch upstream
    $ git merge upstream/master

