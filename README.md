# bspswallow
Adds functionality provided by the dwm "swallow" patch to bspwm.

# Dependencies

* bspwm (obviously)
* xprop

# Installation
Add two files to ~/.config/bspwm

* noswallow - list of classes of windows that you dont't to swallow the terminal

* terminals - list of classes of terminals that you want to be swallowed

If a class isn't available (such as with xev) then the command of origin can be used.

(example files are included in "examples")

Place bspswallow into your PATH and add the following line to your bspwmrc.

```
pidof bspswallow || bspswallow &
```

Now just restart bspwm and you're good to go.
