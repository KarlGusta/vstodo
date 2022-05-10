# How to contribute

For the VS Code template, we use this tutorial to generate it.

[Your First Extension.](https://code.visualstudio.com/api/get-started/your-first-extension)

`Ctrl + F5` to run the debugger. This runs our extension.

`npm run watch` is going to compile our extension.ts to the /dist folder. Webpack transpiles your code. It takes our extension.ts and turns it to extension.js.

`ctrl + shift + p` on our extension window, you can run a command of the extension.

![The Extension window](https://user-images.githubusercontent.com/33565767/167600372-b7edae25-2b78-40de-a86e-c801fdf54527.png)


Every time you make a change to the extension code, you need to reload the `[Extension Development Host]`

To reload, you open the command pallette, `ctrl + shift +p` then you type `reload` then select the reload command.
Alternatively, `ctrl + R`

