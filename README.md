<h1 align="center">VS Code Setting for LAB PC</h1>

```JSONC
{
   // explorer
   "explorer.autoReveal": false,
   "explorer.compactFolders": false,
   "explorer.confirmDelete": false,
   "explorer.confirmDragAndDrop": false,

   // editor
   "editor.wordWrap": "on",
   "editor.tabSize": 3,
   "editor.minimap.enabled": false,
   "editor.cursorBlinking": "expand",
   "editor.formatOnSave": true,
   "editor.bracketPairColorization.enabled": true,
   "editor.defaultFormatter": "esbenp.prettier-vscode",
   "prettier.tabWidth": 3,
   "breadcrumbs.enabled": false,

   // code runner
   "code-runner.saveAllFilesBeforeRun": true,
   "code-runner.runInTerminal": true,
   "code-runner.ignoreSelection": true,
   "code-runner.showExecutionMessage": false,

   // Language specific setting
   "[c]": {
      "editor.defaultFormatter": "ms-vscode.cpptools"
   },
   "[cpp]": {
      "editor.defaultFormatter": "ms-vscode.cpptools"
   },
   "[python]": {
      "editor.defaultFormatter": "ms-python.python",
      "autopep8.args": ["--ignore=E121"]
   },
   "[java]": {
      "editor.defaultFormatter": "redhat.java",
      "redhat.telemetry.enabled": false
   }
}
```
