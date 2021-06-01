# schema
```
{
  "type": "customerService",
  "frontendId": "ka3sakwg4rod41",
  "width": 120,
  "height": 120,
  "left": 0,
  "top": 50,
  "config": {
    "name": "1call聊天",
    "style": {
      "fontSize": 18,
      "fontWeight": 500,
      "background": "red"
    },
    "isDrag": true,
    "action": "popupComponent",
    "actionData": {
      "popupType": "modal",
      "popupData": {
        "schema": {
          "type": "modal",
          "key": "ka3s232454a33wg4rod4",
          "title": "1call客服",
          "width": 502,
          "marginTop": -200,
          "childComponents": [
            {
              "type": "iframe",
              "frontendId": "ka3a3333kwg4rod432",
              "width": 500,
              "height": 650,
              "url": "https://tyhy.hzxc.gov.cn:16001/public/index.html?videoConf=1&LoginToken=EIbNqvFOO0pXN7bhc7B3uW%252FPxLk%253D&UserName=liutao",
            }
          ]
        }
      }
    }
  }
}
```

#### 数据说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| type | 组件类型 | 是 | string | 前端根据schema的type识别组件 |
| frontendId | 组件id | 是 | string | 唯一的key值 |
| width | 组件宽度 | 否 | string \ number | 10% \ 10 |
| height | 组件高度 | 否 | string \ number | 10% \ 10 |
| top | 组件基于父组件的top值 | 否 | string \ number | 10% \ 10 |
| left | 组件基于父组件的left值 | 否 | string \ number | 10% \ 10 |
| config | 组件配置 | 否 | object | 参考Schema.config |

####schema.config
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--| -- |
| name | 组件名称 | 否 | string |  |
| isDrag | 是否可以拖拽 | 否 | bool |  |
| style | 样式 | 否 | object |  |
| action | 事件类型 | 是 | string | popupComponent、updateComponent、openUrl |
| actionData | 事件所需数据 | 否 | object | 对应事件所需数据，详见schema.actionData |

#### schema.config.actionData:
| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| popupType | 弹出组件的组件类型 | 否 | string | popupComponent需要传递 |
| popupData | 需要传入弹出组件的数据| 否 | object | popupComponent需要传递，传入组件的schema({schema: ...}) |
| isClearAll | 是否需要清除其他弹出的组件 | 否 | bool | popupComponent需要传递，用于弹出层的逐级关闭\打开交互 |
| updateIds | 组件ids | 否 | array | updateComponent需要传递，需要更新的组件frontendId、可同时更新多个组件 |
| url | url | 否 | string | openUrl需要传递，弹出的url地址 |
