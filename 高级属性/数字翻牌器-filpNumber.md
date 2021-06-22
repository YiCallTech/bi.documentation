# schema
```
{
  "rotateDirection": "rotateX",
  "numberToThousands": true,
  "fontSize": 30,
  "numberWidth": 30,
  "numberStyle": {},
  "refreshIntervel": 0,
  "number": 45,
  "backgroundImage": "http://172.16.8.7:8999/Annex/2021/05/21/tr4nerb4lf5s.png",
  "prefixText": "动员人员（人数）",
  "prefixFontSize": 12,
  "prefixMargin": 1
}
```

# 返回数据
```
{
    "number": 19993,
}
```

## schema说明:
| 名称 | 描述 | 必填 | 类型 | 默认值 | 备注 |
|--|--|--|--|--|--|
| number | 默认数字 | 否 | number |  |  |
| placeholder | 占位符 | 否 | string |  |  |
| align | 对齐 | 否 | string | center | "left"左, "center"中, "right"右 |
| fontSize | 字号 | 否 | number | 30 |  |
| backgroundColor | 数字背景颜色 | 否 | string |  |  |
| backgroundImage | 数字背景图片 | 否 | string |  |  |
| numberWidth | 单个数字宽度 | 否 | number | 30 |  |
| numberHeight | numberHeight | 否 | number |  |  |
| numberHeight | numberHeight | 否 | number |  |  |
| numberStyle | 单个数字样式 | 否 | object |  | react-css |
| prefixText | 前缀内容 | 否 | string |  |  |
| prefixFontSize | 前缀字号 | 否 | number |  |  |
| prefixColor | 前缀颜色 | 否 | string |  |  |
| prefixMargin | 前缀与主体距离 | 否 | number |  |  |
| suffixText | 后缀内容 | 否 | string |  |  |
| suffixFontSize | 后缀字号 | 否 | number |  |  |
| suffixColor | 后缀颜色 | 否 | string |  |  |
| suffixMargin | 后缀与主体距离 | 否 | number |  |  |

## 返回数据说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| number | 默认数字 | 否 | number |  |
