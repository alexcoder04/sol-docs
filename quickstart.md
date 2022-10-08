
# Quickstart guide

## 1. Install `sol-tools`

 - Go to [sol-tools release page](https://github.com/alexcoder04/sol-tools/releases/latest) and download the program for your system

## 2. Create new project

 - Create new project with `sol new <project-name>`

## 3. Look around

 - I recommend using VS Cod(e/ium) for working on your project
 - Your Lua code goes into two files:
   - `main.lua`: main app code, all GUI components, etc
   - `init.lua`: runs at app start
 - Your GUI components are inside the `components/` folder
   - Every component has its own file
   - They are written in YAML (easy-to-learn key-value language)
   - You can access you components directly from Lua code
 - Other data is located in the `res/` folder
   - `res/img/` for images (they are compiled into the project and can be also accessed directly from Lua and components)
   - `res/data` for YAML-based static application data
 - ...

__**This is a work in progress**__
