# Schema

```json
{
  "type": "block",
  "frontendId": "xxdffsdfdsfsx",
  "width": 488,
  "height": 300,
  "left": 0,
  "top": 0,
  "zIndex": 1,
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
      "numberDirection": 'row', // row | row-reverse | column | column-reverse;
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
  ]，
  "config": {
    "name": "区块",
    "align": "left",
    "iconType": "img",
    "icon": "https://control.hzxc.gov.cn/dxx/static/camera.png",
    "iconStyle": {},
    "blockType": "square",
  }
}
```
# Schema说明

## Schema
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| type | 组件类型 |  String | 是 | 固定：block |
| frontendId |  组件id，后端自动生成 | String | 是 |  |
| width | 组件宽度 | String/Number | 否 | 100 |
| height | 组件高度 | String/Number | 否 | 100 |
| left | 组件离父极左边距离 | String/Number | 否 | 0 |
| top | 组件离父极顶部距离 | String/Number | 否 | 0 |
| zIndex | 组件层级 | Number | 否 | 99 |
| childComponents | 子组件 | Array | 是 | 参考其它组件的 |
| postData | 子组件请求时的特定数据 | Object | 否 | 自定义 |
| config | 组件配置 | Object | 否 | 参考Schema.config |

## Schema.config
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| name | 区块标题名称 | String| 否 |  |
| align | 对其方式 left bottom right | String| 否 |  |
| blockType | block类型 square、rectangle | String | 否 | square |
| icon | 图片url |  String | 否 |  |
| iconStyle | 图标样式 | Object | 否 |  |
| backgroundImage | 背景图片 - 需要传图片url |  String | 否 |  |

## 常规样式
![image.png](/.attachments/image-6d90990f-8644-49a8-8861-f7985b4948ab.png)
