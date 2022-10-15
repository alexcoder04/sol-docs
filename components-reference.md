
# Components Writing Reference

## Default components and their available keys

### Canvas

**Canvas component is a work in progress**

`Components.Base.Canvas`

 - `PosX`
 - `PosY`
 - `Width`
 - `Height`

### Rectangle

`Components.Base.Rectangle`

 - `PosX`
 - `PosY`
 - `Width`
 - `Height`
 - `Fill`
 - `Color`

### TextField

`Component.Base.Rectangle`

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
