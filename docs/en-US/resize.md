# nz-resize

> Resize it's sibling elements.

Resize use `absolute` position, so you should make sure it's container's position is `fixed` or `relative`

## API

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `[nzBaseElement]` | It's container element | `HTMLElement` | - |
| `[nzShowBorder]` | Show a strike through line | `boolean` | false |
| `[nzNode]` | Vertical or horizontal | `NzResizeModeEnum` | `NzResizeModeEnum.Vertical` | 
| `[nzHidden]` | Hide itself | `boolean` | false |
| `[nzMin]` | The minimum value of `nzLeft` or `nzTop` | `number` | 0 |
| `[nzLazy]` | Enable lazy mode | `boolean` | false |
| `(nzResizeStart)` | Emit the position when resizing starts  | `NzResizePosition` | - |
| `(nzResizeChange)` | Emit the position when resizing changes  | `NzResizePosition` | - |
| `(nzResizeEnd)` | Emit the position when resizing ends  | `NzResizePosition` | - |

### Horizontal

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `[nzTop]` | Top to its container element | `number` | - |
| `[nzVerticalMaxResize]`  | The maximum resize limit in vertical direction | `number` | 560 |

### Vertical

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `[nzLeft]` | Left to its container element | `number` | - |
| `[nzMinMargin]` | The minimum margin to its container's right | `number` | 200 |

### NzResizePosition

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `left` | Left | `number` | - |
| `top` | Top | `number` | - |

### Lazy mode

In lazy mode, this component wouldn't emit `nzResizeChange` event when user is dragging it but display a dotted border. And it only emits that event when user stops dragging.


## DEMO
```bash 
<div class="horizontal-box" #horizontal>
  <div class="top-content" [style.height.px]="top"></div>
  <div class="bottom-content"></div>
  <nz-resize
    [nzTop]="top"
    [nzMode]="'horizontal'"
    [nzVerticalMaxResize]="200"
    [nzBaseElement]="horizontal"
    (nzResizeChange)="onResizeChange($event)">
  </nz-resize>
</div>
<div class="vertical-box" #vertical>
  <div class="left-content" [style.width.px]="left"></div>
  <div class="right-content"></div>
  <nz-resize
    [nzLeft]="left"
    [nzMode]="'vertical'"
    [nzBaseElement]="vertical"
    [nzLazy]="true"
    [nzShowBorder]="true"
    (nzResizeChange)="onResizeChange2($event)">
  </nz-resize>
</div>

```
