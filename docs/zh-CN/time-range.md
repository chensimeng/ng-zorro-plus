# Time-range

> Time Range 组件

支持快捷时间，自定义时间，刷新和自动刷新。


## API

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
| `[startTime]` | 开始时间 | `number` | 一小时前 |
| `[endTime]` | 结束时间 | `number` | 现在 |
| `[nzAutoRefresh]` | 是否开启自动刷新 | `boolean` | false |
| `[nzShowAutoRefresh]` | 是否显示自动刷新按钮 | `boolean` | true |
| `[nzRangeOptions]` | 时间快捷键配置 | `number[]` | [600000,3600000,21600000,86400000,604800000] |
| `(nzAutoRefreshChange)` | 自动刷新开启事件 | `event` | - | - |
| `(nzRangeChange)` | 更改快捷时间触发器 | `event` | - |


## DEMO
```bash 
<nz-time-range [startTime]="" [endTime]="" [nzRangeOptions]="options" (nzRangeChange)="onRangeChange($event)" (nzAutoRefreshChange)="onAutoRefreshChange($event)"></nz-time-range>

```
