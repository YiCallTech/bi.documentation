# schema
```
{
  "type": "chart_pie",
  "frontendId": '10000',
  "width": 100,
  "height": 100,
  "left": 250,
  "top": 65,
  "zIndex": 2,
  "postData": {},
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/Chart/Pie/Rk",
  "refreshInterval": 5000,
  "config": {
    "structure": {}
  },
}
```

# Schema说明

## Schema
#### 数据说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| type | 组件类型 | 是 | string | 前端根据schema的type识别组件 |
| frontendId | 组件id | 是 | string | 唯一的key值, 会在请求接口地址的时候附加上本参数 |
| width | 组件宽度 | 否 | string \ number | 10% \ 10 |
| height | 组件高度 | 否 | string \ number | 10% \ 10 |
| top | 组件基于父组件的top值 | 否 | string \ number | 10% \ 10 |
| left | 组件基于父组件的left值 | 否 | string \ number | 10% \ 10 |
| zIndex | 组件堆叠顺序 | 否 | number |  |
| dataUrl| 接口地址 | 是 | string|  |
| postData | 请求时的特定数据 | 否 | object | 接口地址上的请求参数  |
| refreshInterval| 刷新间隔 | 否 | number |  |
| config | 组件配置 | Object | 否 | 参考Schema.config |

## Schema.config
| structure | 图表加载属性 | 是 | object | 对应图表所需配置，详见各子页 |
| style | 图表容器样式 | 是 | object | react-css |

#### type
目前type总共有4种不同的类型
| 名称 | 描述 |
|--|--|
|chart_pie|饼图|
|chart_bar|柱状图|
|chart_line|折线图|
|highchart_pie|3D饼图|