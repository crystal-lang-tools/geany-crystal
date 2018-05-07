# geany-crystal

Crystal support for the [Geany editor](https://www.geany.org/).

# Installation

- puts `filetypes.Crystal.conf` to `~/.config/geany/filedefs`

- In the menu `Tools` > `Configuration Files` > `filetype_externsions.conf`
  - In `[Extensions]`, add `Crystal=*.cr;*.ecr;*.crystal;`
  - In `[Groups]` then `Programming=`, add `Crystal;` to the line

# Shortcuts

- <kbd>F5</kbd>: Run
- <kbd>F8</kbd>: Build
- <kbd>F9</kbd>: Format

Don't forget to reload after formatting (<kbd>Ctrl</kbd> + <kbd>R</kbd> by default).

# Language issues

Crystal isn't supported officially by Geany, so another close languages has to be chosen instead.
We have the choice of either `Ruby` or `CoffeeScript`, here are their pros/cons.
You can switch from one to another by modifying `~/.config/geany/filedefs/filetypes.Crystal.conf`.

## CoffeeScript (default)

Configuration: `[styling=Coffeescript]` and `lexer_filetype=CoffeeScript`

- structs and enums can be collapsed
- heredocs aren't supported (because JavaScript doesn't)
- macros syntax are OK
- method and symbols aren't highlighted

## Ruby

Configuration: `[styling=Ruby]` and `lexer_filetype=Ruby`

- support heredocs
- macro syntax not well supported
- struct can't be collapsed
- standard types aren't highlighted

## Common

Some non exhaustive features not supported when choosing either `Ruby` or `CoffeeScript`:

- structs
- enums
- class and instance variables (including getter, setter etc)
