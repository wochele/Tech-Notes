# Build

`CTL + SHIFT + B` - Build keyboard shortcut

### Typescript

- Configure Task Runner for `TypeScript - tsconfig.json`
  - Puts `tasks.json` into `.vscode` folder
  - Looks at "ts" folder for tsconfig.json

```
--- tasks.json ---

{
    // See https://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    "version": "0.1.0",
    "command": "tsc",
    "isShellCommand": true,
    "args": ["-p", "ts"], // -p is the project, and the other is the folder "ts"
    "showOutput": "silent",
    "problemMatcher": "$tsc"
}
```

- Create `tsconfig.json` file in /ts folder for additional transpiler options

```
{
    "compilerOptions": {
        "target": "es5",           // Target es5 JavaScript
        "outFile": "../js/app.js", // Put all output into one file
        "sourceMap": true          // Create a sourcemap file for each JavaScript file generated, maps TS to transpiled JS
    }
}
```

- Install extension "View In Browser"
