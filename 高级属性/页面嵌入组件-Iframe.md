# schema
```
{
    "type": "iframe",
    "name": "1call聊天",
    "frontendId": "ka3sakwg4rod41",
    "width": 500,
    "height": 600,
    "config": {
        "url": "https://...",
    }
  }
```

#### 数据说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| type | 组件类型 | 是 | string | 前端根据schema的type识别组件 |
| name | 组件名称 | 否 | string |  |
| frontendId | 组件id | 是 | string | 唯一的key值 |
| width | 组件宽度 | 否 | string \ number | 10% \ 10 |
| height | 组件高度 | 否 | string \ number | 10% \ 10 |
| config | 组件配置 | 否 | object | 参考Schema.config |

## Schema.config
| url | 页面地址 | 是 | string |  |
