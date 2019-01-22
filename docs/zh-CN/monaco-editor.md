# Monaco Editor

可配置的组件将monaco编辑器带入您的页面。

## Setup

如果你想使用`NzMonacoEditor`组件，你应该使用这个命令`npm i monaco-editor`安装monaco编辑器，然后编辑你`angular.json`文件以包含资源：

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

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
| `[nzValue]` | 显示的代码 | `string` | - |
| `[nzEditorOptions]` | 代理 `monaco.editor.IEditorOptions`. | `` | - |
| `[nzTheme]` | 主题 | `string` | - |
| `(nzEditorInitialized)` | 一旦初始化，它就会发出一个monaco编辑器实例。 | `event` | - |
