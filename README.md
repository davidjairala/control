# control

Shell script to control your window via `wmctrl` and `xbindkeys`.
Basically, some functionality I was missing when moving over from Mac
OS over to Ubuntu this past week offered by [Spectacle](http://spectacleapp.com/)

## Install dependencies

```bash
sudo apt-get install wmctrl xbindkeys
```

## Get the code

```bash
git clone git@github.com:davidjairala/control.git
```

## Usage

You can use the following options to resize the active window:

* `qtl` - quarter top left
* `qtr` - quarter top right
* `qbl` - quarter bottom left
* `qbr` - quarter bottom righ
* `mt` - mid top
* `mb` - mid bottom
* `ml` - mid left
* `mr` - mid right
* `f` - full

```bash
./control qtl
./control ml
./control f
```

The real usefulness of the script comes when combined with `xbindkeys`
tho, explained below.

## Edit ~/.xbindkeysrc

Mine looks something like:

```bash
##################################
# End of xbindkeys configuration #
##################################

##########
# wmctrl #
##########

"/home/davidjairala/projects/wmctrl/control qtl"
  control + alt + Left

"/home/davidjairala/projects/wmctrl/control qtr"
  control + alt + Right

"/home/davidjairala/projects/wmctrl/control qbl"
  control + shift + alt + Left

"/home/davidjairala/projects/wmctrl/control qbr"
  control + shift + alt + Right

"/home/davidjairala/projects/wmctrl/control f"
  control + alt + Mod4 + f

"/home/davidjairala/projects/wmctrl/control mt"
  control + alt + Mod4 + Up

"/home/davidjairala/projects/wmctrl/control mb"
  control + alt + Mod4 + Down

"/home/davidjairala/projects/wmctrl/control ml"
  control + alt + Mod4 + Left

"/home/davidjairala/projects/wmctrl/control mr"
  control + alt + Mod4 + Right

```

## Enjoy!

Next time you log in, you'll be able to control your active window's
position via the keyboard thanks to wmctrl and xbindkeys!

