# st-kostas

Table of Contents
=================
* [st-kostas](#st-kostas)
* [My custom st build](#My-custom-st-build)
* [Applied patches](#Applied-patches)

# My custom st build
My custom build of suckless simple terminal for my Linux install. I've decided to give a try to a suckless software with my Linux installation and I will document the process here.

# Applied patches
In this section I will list all the patches that I use for my simple terminal build:

* [Alpha](../main/patches/st-alpha-0.8.2.diff) - patch used for transparency effect.
* [Scrollback](../main/patches/st-scrollback-0.8.4.diff) - patch for scrollback through terminal with Shift + PgUp/PgDn keys.
* [Scrollback-mouse](../main/patches/st-scrollback-mouse-20191024-a2c479c.diff) - patch for scrolling through the terminal with Shift + Mousewheel.
* [Scrollback-mouse-altscreen](../main/patches/st-scrollback-mouse-altscreen-20200416-5703aa0.diff) - patch for scrolling trough the terminal with Mouse only.
* [w3m](../main/patches/st-w3m-0.8.3.diff) - for displaying image previews within terminal-based file manager. Although I'm not sure if this was necessary as within `Ranger` file manager image previews did not display while using `w3m`, but when I've switched to `ueberzug` for previewing images, they started to show up in `ranger`.
* [External pipe](../main/patches/st-externalpipe-0.8.4.diff) - for reading and writing simple terminal's screen through a pipe.
* [External pipe eternal](../main/patches/st-externalpipe-eternal-0.8.3.diff) - allows to use `externalpipe` with the entire terminal history.
