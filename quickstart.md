
# Quickstart guide

## 1. Install `sol-tools`

 - Go to [sol-tools release page](https://github.com/alexcoder04/sol-tools/releases/latest) and download the program for your system

## 2. Create new project

 - Start `sol`
 - Type `new` for the command and follow the instructions for creating a new project

## 3. Look around

 - I recommend using VS Cod(e/ium) for working on your project
 - Your main Lua code, like app logic, GUI components etc., is in `app.lua`
 - See [here](./files.html) for other optional files
 - Your GUI components are inside the `components/` folder
   - Every component has its own file
   - They are written in YAML (easy-to-learn key-value language)
   - You can access you components directly from Lua code
   - see [components](./components.html) for more info
 - App metadata, like developer name, license, etc is in `solproj.yml`
 - Other data is located in the `res/` folder
   - `res/img/` for images (they are compiled into the project and can be also accessed directly from Lua and components)
   - `res/data` for YAML-based static application data

## 4. Compile your project

Use either the interactive dialog (start `sol`, type `build` and follow the instructions) or the automated mode (`sol -a build <project-folder>`).

Use [Luna](https://github.com/ndless-nspire/Luna) to create a `.tns` file or copy `out.lua` into the official TI software.

You can also use make on Linux (`make build` creates a `.tns` file assuming you have Luna installed).

## 5. Try it out!

Load the `.tns` file onto you calculator, either using the official TI software or other tools.
