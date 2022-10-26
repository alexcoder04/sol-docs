
# Library

## Colors

`Lib.Colors` is a table containing some useful color values.

*Example:*

```lua
local color = Lib.Colors.Magenta
```

## Debug

You can print debug messages using `Lib.Debug.Print("test")`.

The message can be cleared using `Lib.Debug.UnPrint()`.

## GUI

`Lib.Gui.GetStringSize(str)` gives you the width and height of a string if it would be drawn on the screen.

`Lib.Gui.DrawFocusBox(x, y, w, h, gc)` draws a box for a focused component (useful if you are writing custom `component._draw()` functions).

*Examples:*

```lua
function Components.Custom.HelloWorld:_draw(gc, focused)
    gc:drawString("hello world", self.PosX, self.PosY, "top")
    local width, height = Lib.Gui.GetStringSize("hello world")
    if focused then
        Lib.Gui.DrawFocusBox(self.PosX, self.PosY, width, height)
    end
end
```

## Internal

Library functions meant for internal use in sol, which are exposed to the app developer as well.

`Lib.Internal.ShowAboutDialog()` shows the about dialog box.

## Timeout

Allows you to schedule executing of a function.

*Examples:*

To execute a function at next update cycle:

```lua
local myfun = function() Lib.Debug.Print("Hello") end
Lib.Timeout.Next = myfun
```
