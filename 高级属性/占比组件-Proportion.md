# schema
```
{
  "type": "progressBar",
  "frontendId": "1d21sf3232fasdsdfdsfsdf",
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/ProgressBar/Mqzs",
  "postData": {},
  "left": 50,
  "top": 32,
  "width": 140,
  "height": 7,
  "zIndex": 1,
  "config": {
      "name": "string,
      "nameStyles": {},
      "totalUnit": "string",
      "totalStyles": {},
      "colors": ["#0fb6d9", "#01ffff"],
  }
}
```

#### 数据说明:

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| type | 组件类型 | 是 | string | 前端根据schema的type识别组件 |
| frontendId | 组件id | 是 | string | 唯一的key值 |
| dataUrl | 接口地址 | 否 | string | 用于进度条的数据 |
| postData | 请求时的特定数据 | 否 | object | 自定义 |
| refreshInterval | 定时刷新时间 | 否 | number | 毫秒，大于999 |
| width | 组件宽度 | 否 | string \ number | 10% \ 10 |
| height | 组件高度 | 否 | string \ number | 10% \ 10，progressBarType=circular时为进度条线的宽度 |
| top | 组件基于父组件的top值 | 否 | string \ number | 10% \ 10 |
| left | 组件基于父组件的left值 | 否 | string \ number | 10% \ 10 |
| zIndex | 组件堆叠顺序 | 否 | number |  |
| config | 特定属性 | 否 | object | 详见 Schema.config |

## Schema.config
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--| -- |
| name | 占比数据的名称 | 否| string |  |
| nameStyles | 进度条名称样式 | 否 | object | react-css |
| totalUnit | 总数的单位 | 否 | string |  |
| totalStyles | 总数的样式 | 否 | object | react-css |
| colors | 颜色取值范围 | 否 | array | 默认['#0fb6d9', '#01ffff', '#f7c73f', '#ff9742'] |

#### 返回数据说明:

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| id | id | 是 | string | 有点击事件且点击为弹出列表时，id会传入列表的postData中 |
| name | 每条占比数据的名称 | 是 | string | 有点击事件且点击为弹出列表时，name会显示为弹出框的标题 |
| value | 每条占比数据的数量 | 是 | number | 自动累加value算出总数和占比数 |
```
[{
    "id": "string",
    "name": "string",
    "value": 123,
}]
```
