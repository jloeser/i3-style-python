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

## Behaviour

The script parses every line of the specified (i3) configuration file and looks for corresponding "keys" using regular expressions which are setting the colors for i3's appearance. There are basically two units which can be configured: windows and taskbar(s).

If no keys are found at all they get added at the end of the configuration file by the script. This is quite useful if you start with a fresh i3 configuration and don't have any color configuration set at all. The only flaw is to end up with multiple taskbars due to the nested (task)bar data structure. This would require a one-time manual merge.

Feel free to move and rearrange the keys/lines in your configuration file. The inplace substitution allows a smooth change of i3's appearance with no additional artifacts as long as all keys are present -- even multiple times -- somewhere in the configuration file.

Using the approach of parsing line by line with regular expressions is rather sufficient for this task, however it has some drawbacks towards a lexical analysis (e.g. nested (task)bar data structure). It may happen that the result will not be as expected under some circumstances - anyway using default backup options should save you from ending up with broken, modified i3 configuration. You use this script at your own risk!

A nice tool for creating custom colorschemes is https://thomashunter.name/i3-configurator/.
