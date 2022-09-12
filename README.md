### CfxLua support for VSCode (and FXCode)

-   Install the [Lua Language Server](https://marketplace.visualstudio.com/items?itemName=sumneko.lua) extension
-   Press `Ctrl + Shift + P` and click `Preferences: Open Settings (JSON)
-   Add the following settings to the object, and set the plugin and library paths

```json
  "Lua.diagnostics.enable": true,
  "Lua.runtime.nonstandardSymbol": ["/**/", "`", "+=", "-=", "*=", "/="],
  "Lua.runtime.plugin": "path-to-this-directory/plugin.lua",
  "Lua.runtime.version": "Lua 5.4",
  "Lua.completion.autoRequire": false,
  "Lua.IntelliSense.traceBeSetted": true,
  "Lua.IntelliSense.traceLocalSet": true,
  "Lua.IntelliSense.traceFieldInject": true,
  "Lua.IntelliSense.traceReturn": true,
  "Lua.workspace.preloadFileSize": 2000,
  "Lua.workspace.ignoreDir": [".vscode", ".github", ".git", "**/node_modules"],
  "Lua.workspace.library": [
    "path-to-this-directory/library",
    "path-to-natives"
  ],
  "Lua.workspace.useGitIgnore": true,
  "Lua.diagnostics.disable": [
    "lowercase-global",
    "undefined-field",
    "missing-parameter"
  ],
  "Lua.workspace.checkThirdParty": false,
  "Lua.telemetry.enable": true,
```

### Native declarations

-   Install [NodeJS](https://nodejs.org/en/)
-   Download [JetbrainIDE-CFX.RE](https://github.com/thelindat/JetbrainIDE-CFX.RE)
-   Open a terminal in the folder containing `JetbrainIDE-CFX.RE`
-   Execute the following commands, in order
    -   `npm i`
    -   `npm install -g ts-node`
    -   `npm install -g typescript`
-   Once all dependencies have been installed, execute `npm run start` and follow the prompts
-   You will want to build CFX as well as game natives
-   Change `path-to-natives` to the newly build directory (i.e. C:/GitHub/JetbrainIDE-CFX.RE/build/cfx)

![image](https://user-images.githubusercontent.com/65407488/141656446-21f9105a-9371-4bb3-9089-ab672930f830.png)
![image](https://user-images.githubusercontent.com/65407488/141656539-77221fb4-6ed7-4352-8a5b-cdc1c02de8fd.png)

### WIP support for non-standard functions and types from [LuaGLM](https://github.com/citizenfx/lua/blob/luaglm-dev/cfx/README.md)

**Thanks to CitizenFX, and gottfriedleibniz**

-   [x] vectors
-   [x] quat (partial)
-   [x] matrix (partial)
-   [x] safe navigation
-   [x] extended API
-   [x] extended string

**Thanks to CitizenFX, alloc8or, iTexZoz, and TasoOneAsia**
