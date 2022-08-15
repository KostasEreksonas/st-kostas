# st-kostas

***Newpatch*** branch is used for applying new patches to `st` before merging them to the main branch. It's primary used as a fail-safe in case of errors.

Table of Contents
=================
* [st-kostas](#st-kostas)
* [My custom st build](#My-custom-st-build)
* [Applied patches](#Applied-Patches)
* [Installation](#Installation)
* [Keybindings](#Keybindings)
* [Notes](#Notes)
* [Opening URL's](#Opening-urls)

# My custom st build

My custom build of suckless simple terminal for my Linux install. I've decided to give a try to a suckless software with my Linux installation and I will document the process here.

# Applied Patches

Following is a list of patches that I have applied to my custom build of st:

* [Alpha](https://st.suckless.org/patches/alpha/) - patch used for transparency effect.
* [Anysize](https://st.suckless.org/patches/anysize/) - a patch for allowing st to resize to any pixel size.
* [External pipe](https://st.suckless.org/patches/externalpipe/) - for reading and writing simple terminal's screen through a pipe. Main purpose of this is to pipe urls from `simple terminal` to `dmenu`.
* [External pipe eternal](https://st.suckless.org/patches/externalpipe/) - allows to use `externalpipe` with the entire terminal history.
* [Ligatures](https://st.suckless.org/patches/ligatures/) - ligatures patch for proper ligatures drawing.
* [Scrollback](https://st.suckless.org/patches/scrollback/) - patch for scrollback through terminal with Shift + PgUp/PgDn keys.
* [Scrollback-mouse](https://st.suckless.org/patches/scrollback/) - patch for scrolling through the terminal with Shift + Mousewheel.
* [Scrollback-mouse-altscreen](https://st.suckless.org/patches/scrollback/) - patch for scrolling trough the terminal with Mouse only.
* [w3m](https://st.suckless.org/patches/w3m/) - for displaying image previews within terminal-based file manager.

# Installation

Installation steps are as follows:

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

|		 Keybind		|					Function				|
|:---------------------:|:-----------------------------------------:|
| Ctrl + Shift + U		| Piping urls from `st` window to `dmenu`	|
| Ctrl + Shift + PgUp	| Increase size of the terminal font		|
| Ctrl + Shift + PgDown | Decrease size of the terminal font		|

# Opening urls

For opening urls from `simple terminal`, `xurls` package is necessary. For Arch Linux it can be downloaded from [AUR](https://aur.archlinux.org/packages/xurls/).

Also I have copied a ***[piper](http://arza.us/paste/piper)*** script and put in a `piper` script file within `/usr/local/bin` location and made it executable with `chmod +x` command by running it with ***root*** privilleges.

# Notes

1. ***xlib header files (libx11)*** are neccessary for compiling the software.
2. If you want transparency and other visual effects, install a composition manager (in my case it is `picom`).
3. Multiple line urls are ***not*** handled.
