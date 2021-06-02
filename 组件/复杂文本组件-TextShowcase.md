# Schema

```json
{
  "type": "textShowcase",
  "frontendId": "ka3sa345wg4rod4",
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/Rzhs",
  "postData": {},
  "refreshInterval": 5000,
  "width": 100,
  "height": 50,
  "left": 140,
  "top": 90,
  "config": {
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
}
```

# Schema说明

## Schema
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| type | 组件类型 |  String | 是 | 固定：textShowcase |
| frontendId |  组件id，后端自动生成 | String | 是 |  |
| dataUrl | 接口地址 | string | 否 | |
| postData | 请求时的特定数据 | Object | 否 | 自定义 |
| refreshInterval | 定时刷新时间 毫秒，大于999 | Number | 否 | 0 |
| width | 组件宽度 | String/Number | 否 | 100 |
| height | 组件高度 | String/Number | 否 | 100 |
| left | 组件离父极左边距离 | String/Number | 否 | 0 |
| top | 组件离父极顶部距离 | String/Number | 否 | 0 |
| zIndex | 组件层级 | Number | 否 | 99 |
| config | 组件配置 | Object | 否 | 参考Schema.config |

## Schema.config
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| direction | 文字，数字排布 row，column | String | 否 | row |
| toogleActive | 是否开启点击切换高亮状态 | Boolean | 否 | false |
| textShowcaseType | textShowcase类型 type1，type2，type3，type4，type5 详情见type示例 | String | 否 | type1 |
| text | 文本标题 | String | 是 |  |
| textStyle | 文本样式 | Object | 否 |  |
| textStyle1 | 第二种文本样式 | Object | 否 |  |
| showNumber | 是否展示数量 | Boolean | 否 | false |
| numberToThousands | 格式化数字(每三位加逗号) | Boolean | 否 | true |
| number | 数量 | Number | 否 |  |
| numberStyle | 数量样式 | Object | 否 |  |
| numberStyle1 | 第二种数量样式 | Object | 否 |  |
| showSign | 是否展示正号 | Boolean | 否 | false |
| showUnit | 是否展示单位 | Boolean | 否 | false |
| showTooltip | 是否展示Tooptip | Boolean | 否 | false |
| tooltipStyle | Tooptip样式 | Object | 否 | false |
| unit | 单位 | String | 否 |  |
| unitStyle | 单位样式 | Object | 否 |  |
| unitStyle1 | 第二种单位样式 | Object | 否 |  |
| showPercentage | 是否展示百分比 | Boolean | 否 | false |
| percentage | 百分比 | Number | 否 |  |
| percentageDigits | 百分比小数点 | Number | 否 | 2 |
| percentageStyle | 文本样式 | Object | 否 |  |
| percentageStyle1 | 文本样式 | Object | 否 |  |
| showIcon | 是否展示图标 | Boolean | 否 | false |
| iconType | 图标类型 img，antd | String | 否 | img |
| iconType1 | 第二种图标类型 img，antd | String | 否 | img |
| icon | iconType - img：需要传图片url；antd：antd的icon type |  String | 否 |  |
| activeIcon | 高亮的icon iconType - img：需要传图片url；antd：antd的icon type |  String | 否 |  |
| icon1 | 第二种iconType - img：需要传图片url；antd：antd的icon type |  String | 否 |  |
| iconStyle | 图标样式 | Object | 否 |  |
| iconStyle1 | 第二种图标样式 | Object | 否 |  |
| action | 点击事件类型 详见 [事件](/事件)  | String | 否 |  |
| actionData | 点击事件类型参数 详见 [事件](/事件) | Object | 否 |  |

## schema.actionData:
| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| frontendId | 组件id | 否 | string | popupComponent需要传递，用于弹出组件获取schema |
| isClearAll | 是否需要清除其他弹出的组件 | 否 | bool | popupComponent需要传递，用于弹出层的逐级关闭\打开交互 |
| updateIds | 组件ids | 否 | array | updateComponent需要传递，需要更新的组件frontendId、可同时更新多个组件 |
| url | url | 否 | string | openUrl需要传递，弹出的url地址 |

# type示例

## tyep1
图示：
![image.png](/.attachments/image-f4235348-0a8e-4af8-b030-a09313acd0a2.png)
schema
```Json
{
  "type": "textShowcase",
  "frontendId": "ka3a3333kwg4rod4",
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/Jmfw",
  "postData": {},
  "refreshInterval": 5000,
  "width": 100,
  "height": 80,
  "left": 0,
  "top": 0,
  "config": {
    "direction": "column",
    "textShowcaseType": "type1",
    "text": "居民房屋套数",
    "textStyle": {},
    "showNumber": true,
    "number": 0,
    "numberDirection": "row",
    "numberStyle": {},
    "showUnit": true,
    "unit": "套",
    "unitStyle": {},
  },
  "action": "popupComponent",
  "actionData": {
    "popupType": "",
    "popupData": "",
    "isClearAll": true
  }
}
```

## tyep2
图示：
![image.png](/.attachments/image-8622d21a-33b0-406d-8b54-e0631378593b.png)
schema
```Json
{
  "type": "textShowcase",
  "frontendId": "ka3sa3455245fdfswg4rod4",
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/Czrk",
  "postData": {},
  "width": 100,
  "height": 50,
  "left": 150,
  "top": 0,
  "config": {
    "direction": "column",
    "textShowcaseType": "type2",
    "text": "常住人口",
    "textStyle": {},
    "showNumber": true,
    "numberDirection": "row",
    "numberStyle": {
      "paddingLeft": "2em",
      "color": "#01ffff",
    },
    "showUnit": true,
    "unit": "人",
    "unitStyle": {
      "color": "#01ffff",
    },
    "showPercentage": true,
    "percentage": 88,
    "percentageStyle": {},
    "showIcon": true,
    "iconType": "img",
    "icon": "https://control.hzxc.gov.cn/dxx/static/basic_man.png",
    "iconStyle": {
      "width": 12,
      "height": 32,
    },
  },
  "action": "popupComponent",
  "actionData": {
    "popupType": "",
    "popupData": "",
    "isClearAll": true
  }
}
```

## tyep3
图示：
![image.png](/.attachments/image-b775cf45-0e81-4178-bd6b-944bdbe54d1a.png)
schema
```Json
{
  "type": "textShowcase",
  "frontendId": "ka3sa34552454365654333kwg4rod4",
  "postData": {},
  "height": 30,
  "left": 20,
  "top": 100,
  "config": {
    "direction": "row",
    "textShowcaseType": "type3",
    "text": "商务楼宇",
    "textStyle": {},
    "showNumber": true,
    "numberDirection": "row",
    "numberStyle": {
      "fontSize": 18,
    },
    "showUnit": true,
    "unit": "幢",
    "unitStyle": {},
  },
  "action": "popupComponent",
  "actionData": {
    "popupType": "",
    "popupData": {},
    "isClearAll": true
  }
}
```

## tyep4
图示：
![image.png](/.attachments/image-fb05cfae-5c19-445a-9f06-de85fe94698a.png)
schema
```Json
{
  "type": "textShowcase",
  "frontendId": "ka3a3333kwg4rod4",
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/Jmxxbd",
  "postData": {},
  "refreshInterval": 5000,
  "width": 100,
  "height": 40,
  "left": 0,
  "top": 0,
  "config": {
    "direction": "row",
    "textShowcaseType": "type4",
    "text": "居民信息变动",
    "textStyle": {},
    "showNumber": true,
    "number": 0,
    "numberDirection": "row",
    "numberStyle": {},
    "showNumberSign": true,
    "showUnit": true,
    "unit": "人",
    "unitStyle": {},
  }
}
```

## tyep5
图示：
![image.png](/.attachments/image-f6cad4c8-0c80-46fd-a2d0-88d23d1ebb76.png)
schema
```Json
{
  "type": "textShowcase",
  "frontendId": "ka3sa345524543ffs4rod4",
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/Zrks",
  "postData": {},
  "width": 180,
  "height": 60,
  "left": 20,
  "top": 170,
  "config": {
    "direction": "row",
    "toogleActive": true,
    "textShowcaseType": "type5",
    "text": "监控",
    "textStyle": {},
    "showIcon": true,
    "iconType": "img",
    "icon": "https://control.hzxc.gov.cn/dxx/static/turn_close.png",
    "activeIcon": "https://control.hzxc.gov.cn/dxx/static/turn_open.png",
  },
  "action": "postMessage",
  "actionData": {
    "componentId": "map",
    "type": ["camera"]
  }
}
```

# 请求结果
```Json
{
  "text": "text接口返回",
  "number": 1000,
  "percentage": 88,
  "configType": 1 // 配置类型可空 比如返回1 则会优先使用icon1；
}
```
