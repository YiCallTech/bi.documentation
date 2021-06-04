# schema
```
{
  "type": "video",
  "frontendId": "asfljwepuhasdas",
  "width": 800,
  "height": 300,
  "left": 0,
  "top": 50,
  "zIndex": 1,
  "config": {
    "showSelect": false,
    "style": {"width": "40%"}
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
| zIndex | 组件堆叠顺序 | 否 | number |  |
| config | 组件配置 | 否 | object | 详见Schema.config |

#### schema.config：

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| showSelect | 是否显示视频筛选功能 | 否 | bool |  |
| selects | 筛选组件数组 | 否 | array | 组件schema，暂只支持select，其他筛选功能有需要后续增加|
| style | 组件样式 | 否 | object | react-css |
| selectStyle | 筛选框样式 | 否 | object | react-css |
| videoStyle | 视频样式 | 否 | object | react-css |
| action | 点击事件 | 否 | string | 详见 [事件](/事件) |
| actionData | 点击事件所需参数 | 否 | object | 详见 [事件](/事件) |

常规样式：
![image.png](/.attachments/image-ec5ba2d7-0761-4c6c-9bb6-3288fa8ff9db.png)
