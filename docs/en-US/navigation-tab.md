# nz-navigation-tab

> Tab linked to router.

The navigation tab supports child route mode and query parameter mode. 

In child route mode, config a route like this (with `data.path`):

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

The navigation items doesn't render any user contents. User should use a `<router-outlet>` to control the logic.

## API

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `[nzShowDot]` | Show a `NzBadge` dot in the tab headers | `boolean` | false |
| `[nzNavigationItems]` | Navigation items | `NzNavigationItem` | [] |
| `nzQueryParam` | Enable query param mode with the key | `string` | '' |
| `[nzMin]` | The minimum value of `nzLeft` or `nzTop` | `number` | 0 |

### To nz-tabs

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `[nzSize]` | Size | `small` \| `default` \| `large` | `default` | 
| `[nzTabBarGutter]` | Gutter | `number` | 8 |
| `[nzTabBarExtraContent]` | Extra content | `TemplateRef<void>` | - |

### NzNavigationItem

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| `title` | Title | `string` | - | 
| `pathOrParam` | A unique identifier | `string` | - |
| `status` | When you set `nzShowDot` true, use this property to control the dot's status | `NzBadgeStatusType` | - |
