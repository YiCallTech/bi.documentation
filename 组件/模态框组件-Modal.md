# Schema

```json
{
  "type": "modal",
  "frontendId": "ka3s2324542a333wg4rod411",
  "width": 888,
  "config": {
    "title": "人口信息",
    "marginTop": -100,
    "autoHeight": true,
    "contentStyle": {
      "padding": "0 20px 20px"
    },
  },
  "childComponents": [
    {
      "type": "textShowcase",
      "frontendId": "ka3sa3333kwg4rod4",
      "direction": "column",
      "refreshInterval": 1000,
      "width": 100,
      "height": 200,
      "left": 0,
      "top": 0,
      "textShowcaseType": "type1",
      "text": "总人口数",
      "textStyle": {},
      "showNumber": true,
      "number": 2000,
      "numberDirection": "row",
      "numberStyle": {},
      "showUnit": true,
      "unit": "个",
      "unitStyle": {},
      "action": "popupComponent",
      "actionData": {
        "popupType": '',
        "popupData": '',
        "isClearAll": true
      },
    },
  ]
}
```

# Schema说明

## Schema
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| type | 组件类型 |  String | 是 | 固定：modal |
| frontendId |  组件id，后端自动生成 | String | 是 |  |
| title | modal标题 | String| 否 |  |
| width | 组件宽度 | String/Number | 否 | 900 |
| height | 组件高度 | String/Number | 否 | auto |
| childComponents | 子组件 | Array | 是 | 参考其它组件的 |
| config | 组件配置 | Object | 否 | 参考Schema.config |

## Schema.config
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| marginTop | 组件外边距 | String/Number | 否 | 0 |
| autoHeight | 是否取消子组件的定位 | bool | 否 | true |
| themeColor | 主题颜色 | string | 否 | 默认：#01ffff |
| headerStyle | header样式自定义 | object | 否 | react-css|
| contentStyle | content样式自定义 | object | 否 | react-css|
| filterFrontendId | 列表筛选项配置属性 | Array | 否 | 需要拿到filterData的组件id |
| filter | 列表筛选项配置属性 | Array | 否 | 详见[schema.filter](http://59.202.68.89/Default/1Call%E6%A0%B8%E5%BF%83-%E5%8F%AF%E8%A7%86%E5%8C%96%E6%95%B0%E5%AD%97%E9%A9%BE%E9%A9%B6%E8%88%B1%E7%AE%A1%E7%90%86/_wiki/wikis/Project-Overview?wikiVersion=GBwikiMaster&pagePath=%2F%E7%BB%84%E4%BB%B6%2F%E5%88%97%E8%A1%A8%E7%BB%84%E4%BB%B6%20%252D%20List&pageId=51&anchor=schema.filter%3A) |
| actionName | 点击按钮名称  | String | 否 |  |
| action | 点击事件类型 详见 [事件](/事件)  | String | 否 |  |
| actionData | 点击事件类型参数 详见 [事件](/事件) | Object | 否 |  |

# 备注
如果传入filterFrontendId，filterFrontendId对应的基础组件会在postData里面拿到filterData

如果有filter传入，则所有的childComponent都可以从props拿到additionalData，
additionalData包含filterData
