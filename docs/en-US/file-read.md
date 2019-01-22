# [nz-file-read], [nzFileRead]

> Add a interface to file reader input elements.

It supports single selection and multiple selection.

## API

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `[nzSizeLimit]` | The size limit of a single file, not working in multiple mode | `number` | - |
| `(fileRead)` | Emit file or files | `File` \| `FileList` | - |
| `(fileError)` | When there is an error | `{ reason: string }` | - |


## DEMO

```bash 
<input nz-file-read type="file" (fileRead)="onFileRead($event)">
<input nz-file-read type="file" multiple (fileRead)="onMultipleFileRead($event)">
```
