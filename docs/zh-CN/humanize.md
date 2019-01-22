# Humanize

> 扩展angular自带pipe

# pipes

#### nzHumanizeBytes
***格式化存储大小，bytes为空或者不存在时，返回null，有利于多个pipe的语法糖；***
> value_expression | nzHumanizeBytes [ : decimals [ : scaledDecimals ] ]

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
decimals| 保留的小数位数，可选. | number | 2
scaledDecimals|小数位缩放比例，可选. |number|undefined
  
  
#### nzHumanizeCheckNull
***当值为空时，返回nullReplace替换值（默认'-'）；当值不为空，返回原始值；***
> value_expression | nzHumanizeCheckNull [ : nullReplace ]

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
nullReplace|空值的替换文案，可选. |string| '-'
  
  
#### nzHumanizeDate
***根据区域设置规则格式化日期值，类似angular自带的DatePipe，区别在于date为空或者不存在时，返回null，有利于多个pipe的语法糖；***
> value_expression | nzHumanizeDate [ : format [ : locale ] ]

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
format|要包含的日期、时间部分的格式，使用预定义选项或自定义格式字符串。可选. |string| 'mediumDate'.
locale|要使用的区域格式规则的区域代码。 如果不提供，就使用 LOCALE_ID 的值，默认为 en-US。 参见设置应用的区域。可选. |string| undefined.
  
  
- - - -
  
  
#### nzHumanizeDuration
***根据区域设置格式化时间间隔，value（默认毫秒）为空或者不存在时，返回null，有利于多个pipe的语法糖；**
> value_expression | nzHumanizeDuration [ : targetUnit [ : locale ] ]

| 属性 | 说明 | 类型 | 默认 |
| --- | --- | --- | --- |
targetUnit|格式化后当目标单位，可选. | string | 's'.
locale|要使用的区域格式规则的区域代码。 如果不提供，就使用 LOCALE_ID 的值，默认为 en-US。 参见设置应用的区域。可选.| string | undefined.

