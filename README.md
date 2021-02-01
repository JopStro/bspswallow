# bspswallow
Adds functionality provided by the dwm "swallow" patch to bspwm.

# Dependencies

* bspwm (obviously)
* xprop

# Installation
Add two files to ~/.config/bspwm

* noswallow - list of classes of windows that you don't want to swallow the terminal

* terminals - list of classes of terminals that you want to be swallowed

If a class isn't available (such as with xev) then the command of origin can be used.

(example files are included in "examples")

Place bspswallow into your PATH and add the following line to your bspwmrc.

```
pgrep bspswallow || bspswallow &
```

Now just restart bspwm and you're good to go.

# Known Issues

* Incompatability with LibreOffice due to it having a splash screen and spawning multiple windows, use --no-logo when launching and turn off "Tip of the day" in order to avoid this issue.
* ~~Due to the way the script works, programs opened with dmenu_run will still swallow the teminal. This issue can be avoided by using the script noswallow_dmenu in examples/scripts instead of dmenu_run.~~ this is now only an issue with windows without the \_NET\_WM\_PID xproperty (for example sxiv)
