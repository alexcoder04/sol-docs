
# Components

## Add components to the app

`/app.lua`:

```lua
App:AddElement(Components.Base.Rectangle:new())
App:AddElement(Components.Custom.HelloWorld:new())
```

## Default components and their keys

### Canvas

**Canvas component is a work in progress**

`Components.Base.Canvas`

A canvas to draw on.

 - `PosX`
 - `PosY`
 - `Width`
 - `Height`

### InputField

Text input box (with blinking cursor).

`Components.Base.InputField`

 - `PosX`
 - `PosY`
 - `Width`
 - `Value` (updated as you type)
 - `Color` (as three-value-array or library reference (`Lib.Colors.*`))

### Rectangle

Just a rectangle.

`Components.Base.Rectangle`

 - `PosX`
 - `PosY`
 - `Width`
 - `Height`
 - `Fill` (boolean, whether to fill the rectangle)
 - `Color` (as three-value-array or library reference (`Lib.Colors.*`))

### TextField

Text box, can be used as a button as well.

`Components.Base.Rectangle`

 - `PosX`
 - `PosY`
 - `Label` (actual text)
 - `Border` (boolean, whether to draw a border)
 - `Color` (as three-value-array or library reference (`Lib.Colors.*`))

## Defining / Overwriting draw and update functions

The `Update()` function should return a boolean. The screen is only redrawn on update if at least one component's `Update()` function returns `true`.

*Example:*

```yaml
Update: |
    if self.Label == "Hello" then
        self.Label = "Hello World"
    end
    return true
```

## Defining own keys in custom components

Supported data types: `string`, `int`, `function`

You can access all keys in your functions using `self.<key>`.

*Example:*

```yaml
MyKey1: "MyValue"
MyKey2: 30
MyFunc1: |
    if self.MyKey2 == 30 then
        self.MyKey1 = "Hello World"
    end
```

## Useful resources

 - [YML tutorial (external link)](https://www.educative.io/blog/yaml-tutorial)
