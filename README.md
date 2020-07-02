# bspswallow
Adds functionality provided by the dwm "swallow" patch to bspwm.

This branch uses baskerville's xwinfo instead of xprop and sed, possibly increasing the speed.

# Dependencies

* bspwm (obviously)
* xwinfo (https://github.com/baskerville/xwinfo or on AUR as xwinfo-git)

# Installation
Add two files to ~/.config/bspwm

* noswallow - list of classes of windows that you don't want to swallow the terminal

* terminals - list of classes of terminals that you want to be swallowed

If a class isn't available (such as with xev) use 'N/A' to set for all (this shouldn't be an issue as xev is most likely the only case)

(example files are included in "examples")

Place bspswallow into your PATH and add the following line to your bspwmrc.

```
(ps x | grep bspswallow | grep -v grep) || bspswallow &
```

Now just restart bspwm and you're good to go.

# Known Issues

* Incompatability with LibreOffice due to it having a splash screen and spawning multiple windows, use --no-logo when launching and turn off "Tip of the day" in order to avoid this issue.
* Due to the way the script works, programs opened with dmenu_run will still swallow the teminal. This issue can be avoided by using the script noswallow_dmenu in examples/scripts instead of dmenu_run.
