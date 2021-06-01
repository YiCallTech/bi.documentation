# schema
```
{
    "type": "progressBar",
    "frontendId": "progressBar",
    "width": "10%",
    "height": 20,
    "top": 100,
    "left": '50%',
    "zIndex": 100,
    "config": {
      "type": "type2"
      "isStatic": false
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


## Schema.config
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 备注 |
|--|--|--|--| -- |
| type | 样式类型 | String | 否 | 默认：type1，可选：type1（下城样式）\type2（南苑样式） |
| isStatic | 是否静态展示 | bool | 否 | 默认：false |
| isCommandButtonShow | 是否显示一键应急指挥按钮 | bool | 否 | 默认：true |
| readMoreText | 查看更多文本 | string | 否 | 默认：查看更多>> |
| themeColor | 主题颜色 | string | 否 | 默认：#01ffff |
| themeColorDark | 主题颜色深 | string | 否 | 默认：#0fb6d9 |

南苑样式：
![image.png](/.attachments/image-f33d4558-2d12-4562-af0f-abe6962eaeb8.png)
