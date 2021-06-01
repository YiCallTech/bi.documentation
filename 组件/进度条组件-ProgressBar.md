# schema
```
{
  "type": "progressBar",
  "frontendId": "1d21sf3232fasdsdfdsfsdf",
  "dataUrl": "https://control.hzxc.gov.cn/dxx/Community-Module/V2/ProgressBar/Mqzs",
  "left": 50,
  "top": 32,
  "width": 140,
  "height": 7,
  "config": {
    "progressBarType": "circular",
    "progressBarBackground": "rgba(1,255,255,0.1)",
    "progressBarColor": "#5FFFBE",
    "name": "社区创新活力指数",
    "nameStyles": {
      "marginTop": 20,
      "color": "#01ffff",
      "fontSize": 16,
    },
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
| action | 点击事件 | 否 | string | 详见 [事件](/事件) |
| actionData | 点击事件所需参数 | 否 | object | 详见 [事件](/事件) |
| config | 组件配置 | 否 | object | 参考Schema.config |

## Schema.config
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--| -- |
| progressBarType | 进度条类型 | 否| string | 可选值：fillet、skew、lattice、circular，不传则正常显示 |
| name | 进度条名称 | 否 | string |  |
| direction | 进度条方向 | 否 | string | 只当progressBarType为fillet、skew有效  |
| styles | 进度条样式 | 否 | object |
| progressBgStyles | 进度条背景·样式 | 否 | object |
| nameStyles | 进度条名称样式 | 否 | object | react-css |
| titleStyles | 进度条标题名称样式 | 否 | object | react-css，progressBarType=circular时无效 |
| progressBarBackground | 进度条背景 | 否 | string | |
| progressBarColor | 进度条样式 | 否 | string | |
| isTitleOnRight | 文字是否在右侧 | 否 | bool | progressBarType=circular时无效 |
| noPercentSign | 是否隐藏百分号 | 否 | bool |  |
| decimalPlace | 保留小数位数 | 否 | bool |  |

#### 返回数据说明:

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| percentage | 进度条进度 | 是 | number | 小数点，不超过1 |
| title | 进度条的标题文本 | 否 | string | progressBarType=circular时为圆形进度条中间的文本 |
```
{
    "percentage": .8,
    "title": "80%",
}
```
