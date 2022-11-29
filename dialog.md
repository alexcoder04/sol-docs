
# Dialog

## TODO docs coming

```lua
function Lib.Dialog.ErrorMessage(errorText) end

function Lib.Dialog.AddTextWindow(title,text) end

function Lib.Dialog.AddCustomWindow(title,width,height) end

function Lib.Dialog.AddButton(text,buttonFunction) end

function Lib.Dialog.AddTextBox(xPos,yPos,width,initialText,textBoxFunction) end

function Lib.Dialog.AddLabel(xPos,yPos,labelText,labelColor) end

function Lib.Dialog.AddSlider(xPos,yPos,sliderColor,initialValue,sliderFunction) end

function Lib.Dialog.AddList(xPos,yPos,width,height,listElements,listFunction) end

function Lib.Dialog.CloseWindow() end

function Lib.Dialog.NbWindows() end

function Lib.Dialog.AreWinsOpen() end

function Lib.Dialog.DefaultFocus() end
```
