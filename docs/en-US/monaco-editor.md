# Monaco Editor

A configurable component bring monaco editor into your page.

## Setup

If you want to use `NzMonacoEditor` component, you should install monaco editor using this command `npm i monaco-editor`, and then edit you `angular.json` file to include resources:

```diff
{
  "assets": [
    "src/favicon.ico",
    "src/assets",
    {
      "glob": "**/*",
      "input": "./node_modules/@ant-design/icons-angular/src/inline-svg/",
      "output": "/assets/"
    },
+   {
+     "glob": "**/*",
+     "input": "./node_modules/monaco-editor/min/vs",
+     "output": "/assets/vs"
+   }
  ],
}
```

## API

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `[nzValue]` | the code you want to display in monaco editor. | `string` | - |
| `[nzEditorOptions]` | proxy to  `monaco.editor.IEditorOptions`. |  | - |
| `[nzTheme]` | to change the theme of **all monaco editors**. | `string` | - |
| `(nzEditorInitialized)` | this emits a monaco editor instance once its initialized.| `event` | - |
