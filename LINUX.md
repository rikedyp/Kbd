# APL Prefix Keyboard Layouts for Linux
These files enable typing APL symbols on Linux in X11 and Wayland using the prefix (A.K.A. *introducer* or *dead*) key method. This is the default method on <a target="_blank" href="https://tryapl.org">TryAPL.org</a> and in the <a href="https://github.com/dyalog/ride">Remote IDE (RIDE)</a>.

For example, with the APL Prefix Backtick (UK) layout, typing <kbd>\`</kbd> (backquote/backtick/grave) followed by <kbd>a</kbd> produces `⍺` (APL symbol alpha).

To get the symbol used by the prefix key, press <kbd>prefix</kbd> followed by <kbd>space</kbd>. For example, on the UK backtick layout, <kbd>\` + space</kbd> gives `` ` ``.

## Install
Copy the file `apl_prefix` into the `xkb/symbols` folder for your distribution. This is usually `/usr/share/X11/xkb/symbols`.

Save one of the **XCompose** files as `/home/user/.XCompose`.

In X11 environments, run `setxkbmap`:

```
setxkbmap apl_prefix
```

The default layout is UK backtick prefix. Alternative languages and prefix keys are available using the `variant` modifier.

```
setxkbmap apl_prefix -variant ,dkonehalf
```

Finally, restarting an application should cause `.XCompose` to be reloaded and entering APL symbols should be possible. If that fails, try restarting your session (log out and log in again).

For these layouts to appear in the keyboard settings in GNOME Wayland:

1. An additional `<layout>` item must be added to `/usr/share/X11/xkb/rules/evdev.extras.xml`.
1. Additional keyboard layouts must be enabled, either through GNOME Tweaks, or using `gsettings` in the terminal.

     `gsettings set org.gnome.desktop.input-sources show-all-sources true`

## Available layouts
|Language|Layout|Prefix Key|setxkbmap Variant|XCompose file|
|---|---|---|---|---|
|English|APL Prefix Backtick (UK)|<kbd>\`</kbd>|basic|[XComposeUK](https://raw.githubusercontent.com/rikedyp/Kbd/prefix_linux/XComposeUK)|
|English|APL Prefix Backslash (UK)|<kbd>\\</kbd>|ukbackslash|[XComposeUK](https://raw.githubusercontent.com/rikedyp/Kbd/prefix_linux/XComposeUK)|
|Danish|APL Prefix OneHalf (DK)|<kbd>½</kbd>|dkonehalf|[XComposeDK](https://raw.githubusercontent.com/rikedyp/Kbd/prefix_linux/XComposeDK)|
|Danish|APL Prefix LessThan (DK)|<kbd>\<</kbd>|dkonehalf|[XComposeDK](https://raw.githubusercontent.com/rikedyp/Kbd/prefix_linux/XComposeDK)|

## TODO
- KDE

