# geany-crystal

Crystal support for the [Geany editor](https://www.geany.org/).

See also the [Crystal page of the Geany Wiki](https://wiki.geany.org/config/crystal).

# Installation

- Copy the filetype

`cp filetypes.Crystal.conf ~/.config/geany/filedefs`

- In the menu `Tools` > `Configuration Files` > `filetype_extensions.conf`
  - In `[Extensions]`, add `Crystal=*.cr;*.ecr;`
  - In `[Groups]` then `Programming=`, add `Crystal;` to the line

# Shortcuts

- <kbd>F5</kbd>: Run
- <kbd>F8</kbd>: Build
- <kbd>F9</kbd>: Format

Don't forget to reload after formatting (<kbd>Ctrl</kbd> + <kbd>R</kbd> by default).

# Language issues

Crystal isn't supported officially by Geany, so another close language has to be chosen instead.
We have the choice of either `Ruby` or `CoffeeScript`, here are their pros/cons.
You can switch from one to another by modifying `~/.config/geany/filedefs/filetypes.Crystal.conf`.

## CoffeeScript (default)

Configuration: `[styling=Coffeescript]` and `lexer_filetype=CoffeeScript`

- structs and enums can be collapsed
- heredocs are not highlighted (because JavaScript doesn't)
- macros syntax are OK
- methods and symbols aren't highlighted
- blue color for common methods and related keywords

## Ruby

Configuration: `[styling=Ruby]` and `lexer_filetype=Ruby`

- supports heredocs
- macro syntax not well supported, and usually mess up the rest of the file
- struct can't be collapsed
- standard and custom types are highlighted the same

See the [Geany Wiki](https://wiki.geany.org/config/crystal) for more information about this configuration.
