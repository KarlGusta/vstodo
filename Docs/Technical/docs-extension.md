# Documentation for the extension file

To register a command, we use

```ts
vscode.commands.registerCommand('')
```

The command has to be prefixed with `vstodo.THE_COMMAND` which is the name of the extension you are creating.

`vstodo.AskQuestion`

```ts
vscode.commands.registerCommand('vstodo.AskQuestion', () => {
    
})
```