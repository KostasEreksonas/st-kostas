# st-kostas

***Newpatch*** branch is used for applying new patches to `st` before merging them to the main branch. It's primary used as a fail-safe in case of errors.

Table of Contents
=================
* [st-kostas](#st-kostas)
* [My custom st build](#My-custom-st-build)
* [Applied patches](#Applied-patches)
* [Installation](#Installation)
* [Keybindings](#Keybindings)
* [Notes](#Notes)
* [Opening URL's](#Opening-urls)

# My custom st build
My custom build of suckless simple terminal for my Linux install. I've decided to give a try to a suckless software with my Linux installation and I will document the process here.

# Applied patches
In this section I will list all the patches that I use for my simple terminal build:

* [Alpha](../main/patches/st-alpha-0.8.2.diff) - patch used for transparency effect.
* [Anysize](../main/patches/st-anysize-0.8.4.diff) - a patch for allowing st to resize to any pixel size.
* [Scrollback](../main/patches/st-scrollback-0.8.4.diff) - patch for scrollback through terminal with Shift + PgUp/PgDn keys.
* [External pipe](../main/patches/st-externalpipe-0.8.4.diff) - for reading and writing simple terminal's screen through a pipe. Main purpose of this is to pipe urls from `simple terminal` to `dmenu`.
* [External pipe eternal](../main/patches/st-externalpipe-eternal-0.8.3.diff) - allows to use `externalpipe` with the entire terminal history.
* [Ligatures](../main/patches/st-ligatures-alpha-scrollback-20200430-0.8.3.diff) - ligatures patch for proper ligatures drawing.
* [Scrollback-mouse](../main/patches/st-scrollback-mouse-20191024-a2c479c.diff) - patch for scrolling through the terminal with Shift + Mousewheel.
* [Scrollback-mouse-altscreen](../main/patches/st-scrollback-mouse-altscreen-20200416-5703aa0.diff) - patch for scrolling trough the terminal with Mouse only.
* [w3m](../main/patches/st-w3m-0.8.3.diff) - for displaying image previews within terminal-based file manager. Although I'm not sure if this was necessary as within `Ranger` file manager image previews did not display while using `w3m`, but when I've switched to `ueberzug` for previewing images, they started to show up in `ranger`.

# Installation

In this section I will add instructions how to install this my custom `st` build.

1. Clone this git repository:

`git clone https://github.com/KostasEreksonas/st-kostas.git`

2. Go to the folder of the cloned repository:

`cd st-kostas`

3. Build the package:

`make`

4. Compile this custom `st` package ***with root privilleges***:

`make clean install`

5. Done!

# Keybindings

In this section I will present the custom keybindings for `st` terminal.

|		Keybind		|					Function				|
|:-----------------:|:-----------------------------------------:|
| Ctrl + Shift + U	| Piping urls from `st` window to `dmenu`	|

# Opening urls

For opening urls from `simple terminal`, `xurls` package is necessary. For Arch Linux it can be downloaded from [AUR](https://aur.archlinux.org/packages/xurls/).

Also I have copied a ***[piper](http://arza.us/paste/piper)*** script and put in a `piper` script file within `/usr/local/bin` location and made it executable with `chmod +x` command by running it with ***root*** privilleges.

# Notes

1. ***xlib header files (libx11)*** are neccessary for compiling the software.
2. If you want transparency and other visual effects, install a composition manager (in my case it is `picom`).
3. Multiple line urls are ***not*** handled.
