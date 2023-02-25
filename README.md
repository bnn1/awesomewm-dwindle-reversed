# Reversed `Dwindle` layout
This layout arranges windows in a recursive grid on the right side of the screen, with master window being spawned last.  

It uses slightly modified code of AwesomeWM's `spiral` layout.  

![image.png](https://i.imgur.com/tIZ5l09.png)

## Installation
Place `dwindle_reversed.lua` to `~/.config/awesome/layouts`

## Usage
Import `dwindle_reversed` and place it into `awful.layout.layouts`

```lua
awful.layout.layouts = {
    --- Native layouts
    --- ....
    require("layouts.dwindle_reversed")
}
```

## Uninstallation
Remove the file and layout import.
