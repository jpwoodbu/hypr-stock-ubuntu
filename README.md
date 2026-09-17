# hypr-stock-ubuntu

This is a guide for setting up [Hyprland](https://hypr.land/) on
[Ubuntu](https://ubuntu.com/) 26.04 made with the following goals:

* Stock-native: Use only packages from the stock Ubuntu repos
* Non-invasive: Coexist with the already installed desktop environment
* Inspectable: Small config files and scripts
* Low surface area: Configs only in your homedir with minimal exceptions
* [Omarchy](https://omarchy.org/) hotkeys: Use the same key bindings as Omarchy

This guide aims to make it trivial to try out Hyprland on Ubuntu without
disrupting your existing setup. And since the included config and scripts are
small, it should be easy to see how it works and further customize it.

If you really like Hyprland and want to use it in a first class sort of way, I
recommend trying out [Omarchy](https://omarchy.org/).

## Quick Start

```sh
sudo apt install hyprland hypridle hyprlock hyprpaper hyprpolkitagent \
  hyprpicker waybar wofi swayosd foot wlsunset jq fonts-font-awesome \
  brightnessctl playerctl
```

TODO: Instructions for cloning the repo and copying files into their proper places.

TODO: Instructions for editing files in /etc

TODO: Make sure to comment to try the SUPER + K combo to see all the keybindings.

TODO: Callout the google-calendar.desktop file needing to be created for the clock on-click.

## Walkthrough

This section explains each package installed and what it does.

| Package | Description |
| :--- | :--- |
| `hyprland` | The compositor; the star of the show. |
| `hypridle` | Manages timers for when to dim the screen, lock the session, and suspend the machine when the user is idle. It also talks with `systemd` to make sure the session is locked when the machine is suspended. |
| `hyprlock` | Screen-lock app. It locks the session and displays an authentication prompt to unlock it. |
| `hyprpaper` | Manages the background wallpaper. |
| `hyprpolkitagent` | Shows an authentication pop-up dialog box when root privilege is needed. |
| `hyprpicker` | Used with key binding for copying pixel hex colors. |
| `waybar` | Displays a status bar across the top of the screen. |
| `wofi` | Displays menus for things like launching applications. |
| `swayosd` | Shows an on-screen-display for things like brightness and volume. |
| `foot` | Terminal program which works well with Hyprland; e.g. no title bar. |
| `wlsunset` | Changes the color temperature of the display; i.e. a night light. |
| `jq` | Parses the output from Hyprland tools inside some of the included scripts. |
| `fonts-font-awesome` | Provides icons for Waybar and the system menu. |
| `brightnessctl` | Used with key bindings to controls display brightness. |
| `playerctl` | Used with key bindings to controls media player. |

## Screenshots

TODO: fill in

## Known Issues

### No Bluetooth controls from the Waybar

Using the GNOME control center to manage things like WiFi and audio is 
functional, if clunky, but the Bluetooth controls from the GNOME control center
do not work when in a Hyprland session.

## FAQ

* [Why Hyprland?](#why-hyprland)
* [Why not just run Omarchy?](#why-not-just-run-omarchy)
* [Why is it important to coexist with other desktop environments?](#why-is-it-important-to-coexist-with-other-desktop-environments)
* [Why use Omarchy hotkeys?](#why-use-omarchy-hotkeys)
* [Why is $x Omarchy hotkey missing?](#why-is-x-omarchy-hotkey-missing)

### Why Hyprland?

I got a taste of Hyprland when trying out [Omarchy](https://omarchy.org/) and
really enjoyed it.

### Why not just run Omarchy?

I've been a long time Debian and Ubuntu user and I wasn't ready to switch just
yet. And while I like the vast of majority of the Omarchy setup, there were a
few things I didn't want to bring over to my system.

### Why is it important to coexist with other desktop environments?

I like GNOME. I might end up going back to GNOME eventually (although the more I
use Hyprland the less likely that seems). I want to be able to switch back and
forth between Hyprland and GNOME sessions and I expect others, also new to
Hyprland, may want that too.

### Why use Omarchy hotkeys

I think their [hotkeys](https://omarchy.org/manual/hotkeys/) are
well-thought-out. Since I might end up eventually switching to Omarchy, it makes
sense to stick to (a subset of) their bindings.

### Why is $x Omarchy hotkey missing?

Most likely, I've not yet needed it so I haven't added it. I plan to eventually
migrate every hotkey from Omarchy that is generally compatible with this setup.

### Why not use Universal Wayland Session Manager?

TODO: fill in
