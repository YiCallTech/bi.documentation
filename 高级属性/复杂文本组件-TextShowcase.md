# Schema
```
"structure":{
	"direction": "column",
    "textShowcaseType": "type2",
    "text": "入住户数",
    "textStyle": {
      "order": 2
    },
    "showNumber": true,
    "numberDirection": "row",
    "numberStyle": {
      "order": 1,
      "paddingLeft": "2em",
      "color": "#fff"
    },
    "showUnit": true,
    "unit": "人",
    "unitStyle": {
      "color": "#fff"
    },
    "showPercentage": true,
    "percentage": 88,
    "percentageStyle": {},
    "showIcon": true,
    "iconType": "dot",
    "iconStyle": {
      "width": 12,
      "height": 12,
      "left": 90,
      "top": 23,
      "borderRadius": "50%",
      "backgroundColor": "#01ffff"
    }
}
```

# 返回数据
```
{
    "number": 14,
    "percentage": 0.5
}
```

## Schema说明:
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| direction | 文字，数字排布（可选值：row、column） | string | 否 | row |
| textShowcaseType | textShowcase类型（可选值：type1、type2、type3、type4、type5） | string | 否 | type1 |
| text | 文本 | string | 否 |  |
| textStyle | 文本样式 | object | 否 |  |
| showNumber | 是否展示数量 | boolean | 否 |  |
| numberToThousands | 格式化数字(每三位加逗号) | boolean | 否 | true |
| number | 数量 | number | 否 |  |
| numberStyle | 数量样式 | object | 否 |  |
| showSign | 是否展示正负号 | boolean | 否 |  |
| showUnit | 是否展示单位 | boolean | 否 |  |
| unit | 单位 | string | 否 |  |
| unitStyle | 单位样式 | object | 否 |  |
| showPercentage | 是否展示百分比 | boolean | 否 |  |
| percentage | 百分比 | number | 否 |  |
| percentageDigits | 百分比小数点 | number | 否 | 2 |
| percentageStyle | 百分比样式 | object | 否 |  |
| showIcon | 是否展示图标 | boolean | 否 |  |
| toogleActive | 是否开启点击切换高亮状态 | boolean | 否 |  |
| iconType | 图标类型 | string | 否 |  |
| icon | 图标 - img：需要传图片url；antd：antd的icon type | string | 否 |  |
| activeIcon | 高亮的图标（可选值：img：需要传图片url；antd：antd的icon type） | string | 否 |  |
| iconStyle | 图标样式 | object | 否 |  |

## 返回数据说明:
接口返回为对象，返回模型请参考：[数据来源](/数据来源.md)

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| number | 数量 | 否 | number |  |
| percentage | 百分比 | 否 | number | 1=100% |