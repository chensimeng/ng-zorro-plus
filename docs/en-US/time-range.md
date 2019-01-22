# Time-range

> Time Range it's sibling elements.

Support for shortcut time, custom time, refresh and auto refresh.


## API

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `[startTime]` | start time | `number` | one hour before |
| `[endTime]` | end time | `number` | now |
| `[nzAutoRefresh]` | whether to refresh | `boolean` | false |
| `[nzShowAutoRefresh]` | whether to display the auto refresh button | `boolean` | true |
| `[nzRangeOptions]` | time range in milliseconds | `number[]` | [600000,3600000,21600000,86400000,604800000] |
| `(nzAutoRefreshChange)` | auto refresh event | `event` | - | - |
| `(nzRangeChange)` | change the quick time trigger | `event` | - |


## DEMO
```bash 
<nz-time-range [startTime]="" [endTime]="" [nzRangeOptions]="options" (nzRangeChange)="onRangeChange($event)" (nzAutoRefreshChange)="onAutoRefreshChange($event)"></nz-time-range>

```
