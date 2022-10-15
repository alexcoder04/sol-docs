
# Components Writing Reference

## Default components and their available keys

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
 - `Color`

### Rectangle

Just a rectangle.

`Components.Base.Rectangle`

 - `PosX`
 - `PosY`
 - `Width`
 - `Height`
 - `Fill`
 - `Color`

### TextField

Text box, can be used as a button as well.

`Components.Base.Rectangle`

 - `PosX`
 - `PosY`
 - `Label`
 - `Border`
 - `Color`

## Defining / Overwriting draw and update functions

*Example:*

```yaml
Update: |
    if self.Label == "Hello" then
        self.Label = "Hello World"
    end
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
