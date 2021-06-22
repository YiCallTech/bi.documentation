# schema
```
{
  "startTimeKey": "startTime",
  "endTimeKey": "endTime",
  "width": "endTime",
  "isUnix": true
}
```

## schema说明:
| 名称 | 描述 | 必填 | 类型 | 默认值 | 备注 |
|--|--|--|--|--|--|
| isUnix | 是否单位为秒的时间戳 | 否 | boolean |  |  |
| showTime | 是否显示时间选择 | 否 | boolean |  |  |
| startTimeKey | 开始时间key值 | 是 | string | startTime |  |
| endTimeKey | 结束时间key值 | 是 | string | endTime |  |
| width | 选择器宽度 | 否 | number |  |  |
| color | 字体颜色 | 否 | string | | |
| borderColor | 边框颜色 | 否 | string | | |
| prefixText | 前缀内容 | 否 | string |  |  |
| prefixFontSize | 前缀字号 | 否 | number |  |  |
| prefixColor | 前缀颜色 | 否 | string |  |  |
| prefixMargin | 前缀与主体距离 | 否 | number |  |  |
