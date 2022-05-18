# How to contribute

For the VS Code template, we use this tutorial to generate it.

[Your First Extension.](https://code.visualstudio.com/api/get-started/your-first-extension)

## How to run the extension

`Ctrl + F5` to run the debugger. This runs our extension.

`npm run watch` is going to compile our extension.ts to the /dist folder. Webpack transpiles your code. It takes our extension.ts and turns it to extension.js.

`ctrl + shift + p` on our extension window, you can run a command of the extension.

![The Extension window](https://user-images.githubusercontent.com/33565767/167600372-b7edae25-2b78-40de-a86e-c801fdf54527.png)

Every time you make a change to the extension code, you need to reload the `[Extension Development Host]`

To reload, you open the command pallette, `ctrl + shift +p` then you type `reload` then select the reload command.
Alternatively, `ctrl + R`

VS Code API documentation contains all the APIs you need to create an extension.
<!-- Learn more from the VS Code APIs documentation: https://code.visualstudio.com/api/references/vscode-api -->

### Adding a command to extension.ts

After adding a command in `extension.ts` file, you need to tell VS Code that you have added the command in the package.json.

For example, the command

```ts
    context.subscriptions.push(
    vscode.commands.registerCommand('vstodo.askQuestion', () => {
        // This is the logic that is going to be run
        // Whenever this, vstodo.askQuestion, command gets called.
        vscode.window.showInformationMessage("How was your day?", "good", "bad");
        })
);
```

### Adding the command to the package.json

I will add the command, askQuestion, to the package.json.

```json
    "contributes": {
        "commands": [{
                "command": "vstodo.helloWorld",
                "title": "Hello World"
            },
            {
                "command": "vstodo.askQuestion",
                "title": "Ask Question"
            }
        ]
    }
```

The string in the command, should match what is in the extension. For example, `vstodo.AskQuestion`.

