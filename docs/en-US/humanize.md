# Humanize

> Extend the angular base pipe

## pipes

### nzHumanizeBytes
Format the storage size, when the bytes are empty or not present, return null, which is beneficial to the syntactic sugar of multiple pipes;
> value_expression | nzHumanizeBytes [ : decimals [ : scaledDecimals ] ]

| Property | Description | Type | Default |
| --- | --- | --- | --- |
|decimals|Reserved decimal places, optional. |number|2
|scaledDecimals|Decimal scale, optional. |number|undefined
  
- - - -
  
### nzHumanizeCheckNull
Returns nullReplace replacement value when the value is null (default '-'); when the value is not empty, returns the original value;
> value_expression | nzHumanizeCheckNull [ : nullReplace ]

| Property | Description | Type | Default |
| --- | --- | --- | --- |
|nullReplace|Replacement copy of null value, optional. |string| '-'

- - - -
  
### nzHumanizeDate
Format the date value according to the locale rule, similar to the DatePipe that comes with angular. The difference is that if the date is empty or does not exist, it returns null, which is beneficial to the syntactic sugar of multiple pipes;
> value_expression | nzHumanizeDate [ : format [ : locale ] ]

| Property | Description | Type | Default |
| --- | --- | --- | --- |
|format|Use the predefined options or custom format strings to include the format of the date and time sections. Optional. |string|'mediumDate'.
|locale|The area code of the region format rule to use. If not provided, the value of LOCALE_ID is used, the default is en-US. See the area where you set up your app. Optional. |string|undefined.
  
- - - -
  
### nzHumanizeDuration
According to the locale formatting time interval, when the value (default millisecond) is empty or does not exist, it returns null, which is beneficial to the syntactic sugar of multiple pipes;
> value_expression | nzHumanizeDuration [ : targetUnit [ : locale ] ]

| Property | Description | Type | Default |
| --- | --- | --- | --- |
|targetUnit|When formatting, the target unit is optional. |string| 's'.
|locale|The area code of the region format rule to use. If not provided, the value of LOCALE_ID is used, the default is en-US. See the area where you set up your app. Optional. |string|undefined.
