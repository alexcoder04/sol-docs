
# Library

## Colors

`Lib.Colors` is a table containing some useful color values.

*Example:*

```lua
local color = Lib.Colors.Magenta
```

`Lib.Colors.UpdateColorscheme()` applies the current colorscheme.

`Lib.Colors.DarkModeOn()` and `Lib.Colors.DarkModeOff()` switch to dark and light mode respectively.

`Lib.Colors.DarkModeToggle()` toggles the dark mode.

`Lib.Colors.Parse(c)` returns three values for RGB. Argument can be an array with three numbers or a string as color name found in `Lib.Colors.*`.

## Debug

You can print debug messages using `Lib.Debug.Print("test")`.

The message can be cleared using `Lib.Debug.UnPrint()`.

## GUI

`Lib.Gui.GetStringSize(str)` gives you the width and height of a string if it would be drawn on the screen.

`Lib.Gui.DrawFocusBox(x, y, w, h, gc)` draws a box for a focused component (useful if you are writing custom `component._draw()` functions).

`Lib.Gui.GenTextField(label, x, y)` generates a TextField component with given arguments, for quicker creation of just-labels.

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

```lua
App:AddElement(Lib.Gui.GenTextField("Hello World", 10, 10))
```

## Internal

Library functions meant for internal use in sol, which are exposed to the app developer as well.

`Lib.Internal.ShowAboutDialog()` shows the about dialog box.

`Lib.Internal.IsRunnable(var)` checks whether given variable is function and can be executed.

`Lib.Internal.ArrayContains(array, element)` checks whether array contains a given element.

`Lib.Internal.IsDigit(char)` checks whether a string is a digit (1234567890).

`Lib.Internal.NormalizeNumber(num)` brings a string which represents a number in normal form (remove trailing zeros, replace "" with "0", etc).

## Timeout

Allows you to schedule executing of a function.

*Examples:*

To execute a function at next update cycle:

```lua
local myfun = function() Lib.Debug.Print("Hello") end
Lib.Timeout.Next = myfun
```
