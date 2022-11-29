
# Components

## Add components to the app

`/app.lua`:

```lua
-- create and add components directly
App:AddElement(Components.Base.Rectangle:new()) -- base components
App:AddElement(Components.Custom.HelloWorld:new()) -- custom components

-- OR
-- customize components before registering
hello_world_component = Components.Base.TextField:new()
hello_world_component.Label = "Hello World"
hello_world_component.PosX = 10
hello_world_component.PosY = 10
App:AddElement(hello_world_component)
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
 - `Type` (string/number)
 - `Label` (optional)
 - `LabelWidth` (optional, 0 means auto)
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
 - `FontSize` (7, 9, 10, 11, 12, 16, or 24)
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

Supported data types: `string`, `int`, `function`, `array`, `bool`

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

## Data types behaviour

If a key is detected to be `int`, `bool` or `array`, it is translated to the same type in Lua.

If you want to keep it a string (e. g. `"0"`), you have to define a `*PreserveString` key.

*Example:*

```yaml
MyKey: "0"
MyKeyPreserveString: true
```

## Writing custom components

```yml
Inherit: Base.InputField # which component to base on, either base or custom

Value: "0" # default values
Coordinate: "X1" # custom fields
Update: | # custom update function
    App.Data.Var[self.Coordinate] = Value
    return true
```

## Useful resources

 - [YML tutorial (external link)](https://www.educative.io/blog/yaml-tutorial)
