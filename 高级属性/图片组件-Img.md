# schema
```
{
  "type": "img",
  "frontendId": "ka2223sa33f2222asf33kwg4rod4",
  "width": 14,
  "height": 24,
  "config": {
    "url": "https://control.hzxc.gov.cn/dxx/static/basic_man.png",
    "action": "special",
      "actionData": {
      "specialType": "createOneDo",
      "specialData": {
        "id": "id",
        "title": "title",
        "content": "content"
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
| width | 图片宽度 | 否 | string \ number | 10% \ 10 |
| height | 图片高度 | 否 | string \ number | 10% \ 10 |
| top | 图片基于父组件的top值 | 否 | string \ number | 10% \ 10 |
| left | 图片基于父组件的left值 | 否 | string \ number | 10% \ 10 |
| zIndex | 图片堆叠顺序 | 否 | number |  |
| config | 组件配置 | Object | 否 | 参考Schema.config |

## Schema.config
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| name | 图片名称 | 否 | string |  |
| url | 图片地址 | 否 | string | 支持外链、base64、路径 |
| style | css样式 | 否 | Object | react-css |
| action | 点击事件 | 否 | string | 详见 [事件](/事件) |
| actionData | 点击事件所需参数 | 否 | object | 详见 [事件](/事件) |
