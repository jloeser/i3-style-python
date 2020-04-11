# i3-style-python
Make your [i3](http://i3wm.org) config a little more stylish.

## About

i3-style-python (inspired by [acrisci/i3-style](https://github.com/acrisci/i3-style)) applies a theme to your i3 config file to change the colorscheme of the window decorations and the different parts of i3bar. It's designed especially for people who make frequent changes to their colorscheme to get things just right.


* Easy to try out new themes right after you install.
* Modifies your theme in place - extra template files are not needed.
* Allows to apply the theme also to:
  * dmenu (program launcher)
  * passmenu (dmenu interface to password-store, a password manager)

## Installing

You need to install the 'PyYAML' package:

    sudo pip3 install PyYAML

Just download/clone [i3-style-python](https://raw.githubusercontent.com/jloeser/i3-style-python/master/i3-style-python) file.

## Usage

Just call `i3-style-python` with the name of the theme you want to try and where you want to write the config file to. i3-style-python will look for your config in the default place and apply the theme.

    ./i3-style-python -t solarized -c ~/.i3/config --reload

Check the `themes` directory for the list of built-in themes.

## TODO:

* generate yaml theme file out of current i3 config
