# Ant + NextJS
- Ant with custom theme and sass variables for reuse
- this setup does not require customization of webpack, hence you can leverage out the built-in features like css modules, sass support without any extra configuration
- this setup can be used for react-cra too

## Setup Instructions

1. npm install -g less

2. install filewatcher vscode extension
https://marketplace.visualstudio.com/items?itemName=appulate.filewatcher#:~:text=File%20%26%20Folder%20Watcher,folder%20is%20changed%20in%20vscode

3. add less-styles-script.js at the root
  - creates and outputs compiled css to result.css file in styles folder
  - creates and outputs sass variables to sass-vars.scss file

4. open project at the workspace level (see the cmd in script) and generate settings.json if not present
(ctrl + shift + P > type workspace settings and add the below script)

"filewatcher.commands": [
    {
      "match": "\\.less",
      "isAsync": false,
      "cmd": "cd ${workspaceRoot} && node less-styles-script.js",
      "event": "onFileChange"
    }
  ],

4. disable autosave in vscode
( ctrl + , )
or
File > Preferences > Settings
- Files : Auto Save > off

5. clone the repo and run
