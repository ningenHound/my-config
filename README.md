# my config

*Some settings, programs and scripts to make a Linux desktop more usable and fun :-)*

Set of tools, scripts and configuration files with the aim to get a minimalistic and non intrusive graphic environment (even without a toolbar!) for my daily personal use.

I use [Openbox](http://openbox.org) as window manager, this may not be too fancy, but is efficient and unbloated. To complement it, some scripts and programs with a strong focus on command line, they're lightweight and *just work* while remain out of the way.

Currently running  on Debian, but it surely will work on other distros.

These are some of the programs i use, so in this repo you'll find scripts and configuration files integrated to them:

- **rxvt-unicode**, a terminal emulator with unicode support by default
- [jgmenu](https://jgmenu.github.io/), a X11 menu
- **tmux**, a terminal multiplexer
- **feh**, image viewer, can be used to set backgroud image for your desktop
- **acpi**, shows battery status and other [ACPI](https://en.wikipedia.org/wiki/ACPI) information
- **notify-send**, a program to send desktop notifications
- **dunst**, a notification daemon, i use it to display my desktop notifications
- **xrandr** and **arandr**, to manage multiple monitors
- **xset**, user preference utility for X
- **setxkbmap**, set the keyboard using the X keyboard extension
- **amixer**, command line mixer for the [ALSA](https://alsa-project.org) soundcard driver, i use it as volume control

The **scripts** folder contains some useful shell scripts i use, for example, to display battery level (`Super key + 0`), date and time (`Super key + 9`) or volume control (Function keys for volume up and down). You will find the keyboard shortcuts in the rc.xml configuration file, within the openbox folder.

In order to integrate the scripts to Openbox configuration, you must install the programs listed above and define the `$MY_CONFIG` environment variable, with the value of the path where you cloned this repo.

To use the **configuration files** of this repo, you have two options:

1. Replace your local ones with these
2. Define symbolic links in your local config paths to link these files

The second option is recommended, so you can have all your configs in a single place

So for example, to link your rc.xml Openbox config file, first, disable your local file, you can rename it with:

`mv rc.xml rc.xml.original`

Then create the symbolic link:

`ln -s /home/yourUser/my-config/rc.xml /home/yourUser/.config/openbox/rc.xml` (assuming you cloned this repo in your user folder)

The same procedure applies to the rest of the config files.

Enjoy!

*TODO:* Make a shell script to automate the linking process

