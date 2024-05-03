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

- st-clipboard-20180309-c5ba9c0.diff
- st-delkey-20201112-4ef0cbd.diff
- st-osc10-20210106-4ef0cbd.diff
- st-rightclickpaste-0.8.2.diff
- st-selectioncolors-0.8.4.diff
- st-undercurl-0.8.4.diff
- st-xresources-20200604-9ba7ecf.diff
- st-externalpipe-0.8.4.diff
- st-font2-20190416-ba72400.diff
- st-scrollback-20210507-4536f46.diff
- st-scrollback-mouse-20191024-a2c479c.diff
- st-visualbell2-basic-2020-05-13-045a0fa.diff
- st-visualbell2-enhanced-2020-05-13-045a0fa.diff
- st-anysize-0.8.4.diff
- st-anygeometry-0.8.1.diff
- st-blinking_cursor-20200531-a2a7044.diff

## Stay Synced with Upstream

After cloning this repo, add the upstream repository as a remote:

    $ git remote add upstream "https://git.suckless.org/st"

To merge changes from upstream:

    $ git fetch upstream
    $ git merge upstream/master

