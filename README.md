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

Following is a list of patches that I have applied to my custom build of st:

* [Alpha](https://st.suckless.org/patches/alpha/) - patch used for transparency effect.
* [Alpha Focus Highlight](https://st.suckless.org/patches/alpha_focus_highlight/) - different terminal opacity values when (un)focusing the terminal.
* [Anysize](https://st.suckless.org/patches/anysize/) - a patch for allowing st to resize to any pixel size.
* [External pipe](https://st.suckless.org/patches/externalpipe/) - for reading and writing simple terminal's screen through a pipe. Main purpose of this is to pipe urls from `simple terminal` to `dmenu`.
* [External pipe eternal](https://st.suckless.org/patches/externalpipe/) - allows to use `externalpipe` with the entire terminal history.
* [Ligatures](https://st.suckless.org/patches/ligatures/) - ligatures patch for proper ligatures drawing.
* [Scrollback](https://st.suckless.org/patches/scrollback/) - patch for scrollback through terminal with Shift + PgUp/PgDn keys.
* [Scrollback-mouse](https://st.suckless.org/patches/scrollback/) - patch for scrolling through the terminal with Shift + Mousewheel.
* [Scrollback-mouse-altscreen](https://st.suckless.org/patches/scrollback/) - patch for scrolling trough the terminal with Mouse only.
* [Solarized](https://st.suckless.org/patches/solarized/) - solarized colorscheme created by Ethan Schoonover for st.
* [w3m](https://st.suckless.org/patches/w3m/) - for displaying image previews within terminal-based file manager.

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
