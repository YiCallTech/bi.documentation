# schema
```
{
  "type": "time",
  "frontendId": "ka3sakwg4rod41",
  "width": 800,
  "height": 300,
  "left": 0,
  "top": 50,
  "zIndex": 1,
  "config": {
    "style": {},
    "format": "YYYY-MM-DD HH:mm dddd",
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
| style | 时间文本样式 | 否 | object | react-css |
| format | moment.js 格式 | 否 | string | 详见：http://momentjs.cn/docs/#/displaying/format/|
