# Reversed `Dwindle` layout
This layout arranges windows in a recursive grid on the right side of the screen, with master window being spawned last.  

It uses slightly modified code of AwesomeWM's `spiral` layout.  

![image.png](https://i.imgur.com/HcnrUTB.gif)

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

You can replace native dwindle's arrange func with this one:

```lua
awful.layout.suit.spiral.dwindle.arrange = require("layouts.dwindle_reversed").arrange
```
and then use modified dwindle layout as usual 
```lua
awful.layout.layouts = {
    --- Native layouts
    --- ....
    awful.layout.suit.spiral.dwindle
}
```

## Uninstallation
Remove the file and layout import.

## Alternative solution
Or you can just add this line
```lua
if not awesome.startup then awful.client.setslave(c) end
``` 
to the `"manage"` signal handler :D
