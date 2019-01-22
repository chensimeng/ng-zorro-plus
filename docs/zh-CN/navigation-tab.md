# nz-navigation-tab

> Tab链接到路由

导航选项卡支持子路由模式和查询参数模式。

在子路由模式下，配置这样的路由（使用`data.path`）：

```ts
const routes: Routes = [
  {
    path: '', component: NavigationTabComponent, children: [
      { path: 'apple', component: AppleComponent, data: { path: 'apple' } },
      { path: 'banana', component: AppleComponent, data: { path: 'banana' } },
      { path: 'cucumber', component: AppleComponent, data: { path: 'cucumber' } },
      { path: '', component: AppleComponent }
    ]
  }
];
```

导航项不会呈现任何用户内容。用户应使用`<router-outlet>`来控制逻辑。

## API

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `[nzShowDot]` | Show a `NzBadge` dot in the tab headers | `boolean` | false |
| `[nzNavigationItems]` | Navigation items | `NzNavigationItem` | [] |
| `nzQueryParam` | Enable query param mode with the key | `string` | '' |
| `[nzMin]` | The minimum value of `nzLeft` or `nzTop` | `number` | 0 |

### To nz-tabs

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
| `[nzSize]` | Size | `small` \| `default` \| `large` | `default` | 
| `[nzTabBarGutter]` | Gutter | `number` | 8 |
| `[nzTabBarExtraContent]` | Extra content | `TemplateRef<void>` | - |

### NzNavigationItem

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
| `title` | Title | `string` | - | 
| `pathOrParam` | A unique identifier | `string` | - |
| `status` | When you set `nzShowDot` true, use this property to control the dot's status | `NzBadgeStatusType` | - |
