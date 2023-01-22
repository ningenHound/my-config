# my config

*Some settings, programs and scripts to make a linux desktop more usable and fun :-)*

Set of tools, scripts and configuration files with the aim to get a minimalistic and non intrusive graphic environment (even without a toolbar!) for my daily personal use.

This may be not too fancy, but is efficient and unbloated, with a strong focus on command line tools and lightweight software that *just works* while it gets out of the way.

Currently Running  on Debian, but it surely will work on other distros.

These are some of the programs i use, so in this repo you'll find scripts and configuration files integrated to them

- [openbox](http://openbox.org), a simple and lightweight window manager
- **rxvt-unicode**, a terminal emulator with unicode support by default
- [jgmenu](https://jgmenu.github.io/), a X11 menu
- **feh**, image viewer, can be used to set backgroud image for your desktop
- **tmux**, a popular terminal multiplexer
- **notify-send**, a program to send desktop notifications
- **dunst**, a notification daemon, i use it to display my desktop notifications
- **xrandr** and **arandr**, to manage multiple monitors
- **xset**, user preference utility for X
- **amixer**, command line mixer for alsa, i use it as a volume control



the **scripts** folder contains some useful shell scripts i use, for example, to display battery level (`Super key + 0`), date and time (`Super key + 9`) or volume control (Function keys for volume up and down). You will find the keyboard shortcuts in the rc.xml configuration file, within the openbox folder

In order to run the scripts on the `scripts` folder, you must define the `$MY_CONFIG` environment variable before, once you clone this repo, set the variable with the path where you cloned it.

To use the **configuration files** of this repo, you have two options, to replace your local ones with these, or to define symbolic links in your local config paths to link these files, the second option is recommended, so you can have your configs always in the repo

So for example, to link your rc.xml openbox config file, first, disable your local file, you can rename it with `mv rc.xml rc.xml.original` then create the link:

`ln -s /home/yourUser/my-config/rc.xml /home/yourUser/.config/openbox/rc.xml` (assuming you cloned this repo in your user folder)

The same procedure applies for the rest of the config files

