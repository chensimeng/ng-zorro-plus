# nz-resize

> Resize 组件

调整使用`position`位置，确保容器的位置是`fixed`或`relative`

## API

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
| `[nzBaseElement]` | 容器元素 | `HTMLElement` | - |
| `[nzShowBorder]` | 显示边框 | `boolean` | false |
| `[nzNode]` | 垂直或水平 | `NzResizeModeEnum` | `NzResizeModeEnum.Vertical` | 
| `[nzHidden]` | 隐藏 | `boolean` | false |
| `[nzMin]` | `nzLeft`或`nzTop`的最小值 | `number` | 0 |
| `[nzLazy]` | 是否开启延迟模式 | `boolean` | false |
| `(nzResizeStart)` | 当触发resize时，发射一个位置 | `NzResizePosition` | - |
| `(nzResizeChange)` | 当改变resize时，发射一个位置  | `NzResizePosition` | - |
| `(nzResizeEnd)` | 当结束resize时，发射一个位置  | `NzResizePosition` | - |

### Horizontal

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
| `[nzTop]` | 距离顶部距离 | `number` | - |
| `[nzVerticalMaxResize]`  | 垂直方向的最大调整大小限制 | `number` | 560 |

### Vertical

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
| `[nzLeft]` | 距离左边距离 | `number` | - |
| `[nzMinMargin]` | 其容器右边的最小边距| `number` | 200 |

### NzResizePosition

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
| `left` | 距离左边 | `number` | - |
| `top` | 距离顶部 | `number` | - |

### Lazy mode

在延迟模式下，当用户拖动它但显示虚线边框时，此组件不会发出`nzResizeChange`事件。它只会在用户停止拖动时发出该事件。


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
