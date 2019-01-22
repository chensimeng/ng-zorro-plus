# [nz-file-read], [nzFileRead]

> 增加一个指令渲染文件元素

它支持单选和多选。

## API

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
| `[nzSizeLimit]` | 单个文件的大小限制，不能在多个模式下工作 | `number` | - |
| `(fileRead)` | 发射文件或者多个文件 | `File` | `FileList` | - |
| `(fileError)` | 当有错误时触发 | `{ reason: string }` | - |


##DEMO

```bash 
<input nz-file-read type="file" (fileRead)="onFileRead($event)">
<input nz-file-read type="file" multiple (fileRead)="onMultipleFileRead($event)">
```
