
# Hooks

|Name|Underlying Event|Description|
|---|---|---|
|`Hooks:Backspace()`|`on.backspaceKey()`|Runs when the backspace key is pressed|
|`Hooks:CharIn(c)`|`on.charIn(c)`|Runs on character input, only when no component is focused|
|`Hooks:Paint(gc)`|`on.paint(gc)`|Runs when the screen is re-drawn, use raw nspire draw api|

## How to define a hook

`/hooks.lua`:

```lua
function Hooks:CharIn(c)
    Lib.Debug.Print("pressed " .. tostring(c))
end
```
