# st-kostas

Custom build of a suckless simple terminal (st) utility.

Table of Contents
=================
* [Installation](#Installation)
* [Applied patches](#Applied-Patches)
* [Keybindings](#Keybindings)
* [Notes](#Notes)

# Installation

1. Clone this git repository:

`git clone https://github.com/KostasEreksonas/st-kostas.git`

2. Go to the folder of the cloned repository:

`cd st-kostas`

3. Build the package:

`make`

4. Compile the package with ***root*** privilleges:

`make clean install`

# Applied Patches

Following is a list of patches that I have applied to my custom build of st.

* [Alpha](https://st.suckless.org/patches/alpha/)
* [Alpha Focus Highlight](https://st.suckless.org/patches/alpha_focus_highlight/)
* [Anysize](https://st.suckless.org/patches/anysize/)
* [Blinking cursor](https://st.suckless.org/patches/blinking_cursor/)
* [Colorschemes](https://st.suckless.org/patches/colorschemes/)
* [CSI](https://st.suckless.org/patches/csi_22_23/)
* [Dynamic Cursor Color](https://st.suckless.org/patches/dynamic-cursor-color/)
* [External pipe](https://st.suckless.org/patches/externalpipe/)
* [External pipe eternal](https://st.suckless.org/patches/externalpipe/)
* [Ligatures](https://st.suckless.org/patches/ligatures/)
* [Scrollback](https://st.suckless.org/patches/scrollback/)
* [Scrollback-mouse](https://st.suckless.org/patches/scrollback/)
* [Scrollback-mouse-altscreen](https://st.suckless.org/patches/scrollback/)
* [w3m](https://st.suckless.org/patches/w3m/)

# Keybindings

In this section I will present the custom keybindings for `st` terminal.

|		 Keybind		|					Function				|
|:---------------------:|:-----------------------------------------:|
| Ctrl + Shift + U		| Open a menu with web links from terminal	|
| Ctrl + Shift + PgUp	| Increase size of the terminal font		|
| Ctrl + Shift + PgDown | Decrease size of the terminal font		|

# Notes

1. To grab URL's from within the simple terminal, `xurls` package is necessary. For Arch Linux it can be downloaded from [AUR](https://aur.archlinux.org/packages/xurls/). Also, I use a supplementary script named ***[piper](http://arza.us/paste/piper)*** to open a selected link with a program of choice.

2. For transparency and other visual effects, a composition manager is required (i.e. compton or picom).
