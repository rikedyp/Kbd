# APL Prefix Keyboard Layouts for Linux
These files enable typing APL symbols on Linux in X11 using the prefix (A.K.A. *introducer* or *dead*) key method.

For example, in the UK layout, typing <kbd>\`</kbd> (backquote/backtick) followed by <kbd>a</kbd> produces `⍺` (APL symbol alpha).

## Install
Copy the file `apl_prefix` into the `xkb/symbols` folder for your distribution. This is usually `/usr/share/X11/xkb/symbols`.

Save the file `XComposeUK` as `/home/user/.XCompose`.

In X11 environments, run `setxkbmap`:

```
setxkbmap apl_prefix
```

Finally, restarting an application should cause `.XCompose` to be reloaded and entering APL symbols should be possible. If that fails, try restarting your session (log out and log in again).

