# Mailspring Theming

Mailspring theme that adapts to your wallpaper using pywal

## Prerequisites

- Install [pywal](https://github.com/dylanaraps/pywal) using one of the [provided methods](https://github.com/dylanaraps/pywal/wiki/Installation).

## Steps

- Clone this repo `git clone https://github.com/SoulEater45/mailspring-pywal-theming.git`
- Put the `templates/colors.less` file into your pywal templates folder `~/.config/wal/templates/`
- Execute the Pywal command using your wallpaper `wal -i $WALLPAPER`
- Link the generated pywal file to this folder `ln -s ~/.cache/wal/colors.less ./colors.less`
- In Mailspring go to Edit -> Install Theme -> choose this folder
- You should have now a matching theme with your wallpaper

## Lazy way
You can use the provided script `lazy.sh` which does the steps 2-4 for you. Just set the wallpaper path!

The `lazy.sh` script:
```sh
#!/usr/bin/bash
export WALLPAPER="~/Pictures/wallpaper.jpg"
wal -i $WALLPAPER
ln -s ~/.cache/wal/colors.less ./colors.less
```

## Problems
Applying pywal does not automatically change the theme!
You need to change it to another (light, dark, etc.) and install it again to change the theme.

## Suggestions
If someone can automate the theme change directly, make a pull request. I am also happy to see different variants of applying the pywal theme to mailspring.