# schema
```
{
  "type": "text",
  "frontendId": "asfljwepuhasdas",
  "width": 800,
  "height": 300,
  "left": 0,
  "top": 50,
  "zIndex": 1,
  "config": {
    "text": "text",
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
| style | 文本样式 | 否 | object | react-css |
| itemStyle | 单项的样式 | 否 | object | react-css |
| nameStyle | 气泡名称的样式 | 否 | object | react-css |
| countStyle | 气泡数值的样式 | 否 | object | react-css |
| unitStyle | 气泡单位的样式 | 否 | object | react-css |
| unit | 单位 | 否 | string |  |
| maxTagWidth | 最大气泡的宽度 | 否 | number | 默认：140 |
| minTagWidth | 最小气泡的宽度 | 否 | number | 默认：70 |
| displacement | 气泡运动时的百分比位移 | 否 | number | 默认：100 |
| animationTime | 气泡单次运动周期的时长(秒) | 否 | number | 默认：2 |
