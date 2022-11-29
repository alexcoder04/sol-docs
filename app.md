
# App

## Functions

|Function|Description|
|---|---|
|`App:AddElement(element) -> id`|Registeres a component and returns its id|
|`App:ElementExec(id, callback) -> callback_result`|Runs a function on the element with given id as if this function was defined on this element and returns its result; `callback(self) -> any`|
|`App:ElValGet(id, key) -> val`|Gets value of the given key on element of provided id|
|`function App:ElValSet(id, key, val) -> nil`|Sets value of given key on element of provided id|

## Copy/Paste

You can define following functions to implement the Ctrl-C/Ctrl-X/Ctrl-V functionality; you have to handle finding and inserting the text yourself.

These are called when the user presses the corresponding keys.

|Function|Desription|
|---|---|
|`App.Integrations.Copy() -> text`|The returned text is placed into the clipboard|
|`App.Integrations.Cut() -> text`|The returned text is placed into the clipboard|
|`App.Integrations.Paste(text)`|The argument is the text from the clipboard|
