# wmcalc
Small utility to calculate windows geometry in multi-display/multu workspace environment

This is helper utility to be used together with `wmctrl(1)` or similar to calculate window geometry in presence of multiple monitors and workspaces.

For example, imagine you have 2 monitors with workspaces organized into 2x2 grid.
You can move 'emacs' to (1,1) workspace grid location on 2nd monitor with:

```
 wmctrl -r "Home" -e `wmcalc -m 1 -c 1 -r 1` 
```

Or you can move it to the same workspace, but on 1st monitor:

```
 wmctrl -r "Home" -e `wmcalc -m 0 -c 1 -r 1` 
```

Now you can move it to the upper left workspace on the 1st monitor:

```
 wmctrl -r "Home" -e `wmcalc -m 0 -c 1 -r 1` 
```

## Limitations ##

  * Only tested on Ubuntu 16.04 with Compiz
  * Windows are always sized to occupy full workspace on given monitor (TODO: add additional options for that)
  
  
## Contact ##

Vadim Zaliva <lord@crocodile.org>




