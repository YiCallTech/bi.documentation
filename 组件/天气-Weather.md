# schema
```
{
  "type": "weather",
  "frontendId": "ka3sakwg4rod41",
  "dataUrl": "https://control.hzxc.gov.cn/sqjsc/Community-Module/V2/Weather",
  "postData": {},
  "refreshInterval": 3000,
  "width": 800,
  "height": 300,
  "left": 0,
  "top": 50,
  "zIndex": 1,
  "config": {
    "style": {
      "width": "40%",
    },
    "showIcon": true,
  }
}
```

#### 数据说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| type | 组件类型 | 是 | string | 前端根据schema的type识别组件 |
| frontendId | 组件id | 是 | string | 唯一的key值 |
| dataUrl | 接口地址 | 否 | string |  |
| postData | 请求时的特定数据 | 否 | object | 自定义 |
| refreshInterval | 定时刷新时间 | 否 | number | 毫秒，大于999 |
| width | 组件宽度 | 否 | string \ number | 10% \ 10 |
| height | 组件高度 | 否 | string \ number | 10% \ 10 |
| top | 组件基于父组件的top值 | 否 | string \ number | 10% \ 10 |
| left | 组件基于父组件的left值 | 否 | string \ number | 10% \ 10 |
| zIndex | 组件堆叠顺序 | 否 | number |  |
| config | 组件配置 | 否 | object | 详见Schema.config |

#### schema.config：

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| style | 天气样式 | 否 | object | react-css |
| showIcon | 是否展示天气图标 | 否 | bool |  |

#### 返回数据说明:

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| temperature | 温度 | 是 | number | |
| weatherType | 天气类型 | 是 | string |  |
```
{
    "temperature": 28,
    "weatherType": "晴天",
}
```
