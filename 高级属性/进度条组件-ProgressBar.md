# schema
```json
{
  "progressBarType": "",
  "direction": "",
  "styles": {},
  "progressBgStyles": {},
  "nameStyles":{},
  "titleStyles": {},
  "progressBarBackground": "",
  "progressBarColor": "",
  "isTitleOnRight": false,
  "noPercentSign": false,
  "decimalPlace": 1,
}
```

# 返回数据
```json
{
    "percentage": .8,
    "title": "80%",
}
```

#### Schema说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--| -- |
| progressBarType | 进度条类型 | 否| string | 可选值：fillet、skew、lattice、circular，不传则正常显示 |
| direction | 进度条方向 | 否 | string | 只当progressBarType为fillet、skew有效  |
| styles | 进度条样式 | 否 | object |
| progressBgStyles | 进度条背景·样式 | 否 | object |
| nameStyles | 进度条名称样式 | 否 | object | react-css |
| titleStyles | 进度条标题名称样式 | 否 | object | react-css，progressBarType=circular时无效 |
| progressBarBackground | 进度条背景 | 否 | string | |
| isTitleOnRight | 文字是否在右侧 | 否 | bool | progressBarType=circular时无效 |
| noPercentSign | 是否隐藏百分号 | 否 | bool |  |
| decimalPlace | 保留小数位数 | 否 | bool |  |

## 返回数据说明:

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| percentage | 进度条进度 | 是 | number | 小数点，不超过1 |
| title | 进度条的标题文本 | 否 | string | progressBarType=circular时为圆形进度条中间的文本 |
