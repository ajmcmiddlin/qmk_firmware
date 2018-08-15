# HOWTO

## Edit keymap

Either edit `keymap.c` directly, or download from the [online
configurator](https://configure.ergodox-ez.com). **If you download from the configurator you need to
do s/KEYMAP/LAYOUT_ergodox in the downloaded C**.

## Load keymap

On NixOS:

```
$ cd $QMK_ROOT
$ nix-shell
(nix-shell) $ make ergodox_eq:ajmcmiddlin
(nix-shell) $ sudo teensy-loader-cli -mmcu=atmega32u4 -w ergodox_ez_ajmcmiddlin.hex
(nix-shell) $ # use paperclip to hit reset button (top right of right half)
```
