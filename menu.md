
# Menu

*Example:*

```yaml
 - Id: edit                 # unique identifier
   Name: Edit               # display name
   Submenues:               # list of submenues
    - Id: clear             # unique identifier
      Name: Clear inputs    # display name
      Function: |           # Lua code to run on click
        Lib.Debug.FlashRedraws = not Lib.Debug.FlashRedraws
    - Id: ...
      ...
 - Id: ...
   ...
```
