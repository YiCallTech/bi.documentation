# schema
```
{
  "type": "table",
  "frontendId": "ka3sakwg4rod41",
  "dataUrl": '',
  "postData": {},
  "refreshInterval": 3000,
  "width": 800,
  "height": 300,
  "left": 0,
  "top": 50,
  "zIndex": 1,
  "config": {
    "tableStyles": {},
    "structure": [{
      "key": "title",
      "styles": {
        "width": "40%",
      },
      "schema": {}
    }],
    "head": [{
      "name": "aaa",
      "styles": {},
      "colspan": 2
    }]
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
| tableStyles | 组件名称 | 否 | string | react-css |
| structure | 表格结构 | 是 | array | 详见schema.config.structure |
| head | 表格头部配置属性 | 否 | object | 详见schema.config.head |


#### schema.config.structure：

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| key | key值 | 是 | string | 唯一key值，用于data中的数据提取 |
| styles | 样式 | 是 | object | react-css |
| schema | schema | 否 | object | 组件schema，直接显示对应的组件 |

#### schema.config.head:

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| name | 当前单元格显示的名称 | 是 | string |  |
| styles | 样式 | 是 | object | react-css |
| colspan | 列合并数量 | 否 | number |  |

#### dataApi:
根据不同的表格实例由前后端协调数据。
| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| schema.structure.key | 表格key值 | 是 | string |  |
```
{
  [{
    "title": "tab选项",
    "content": "tab选项tab选项tab选项",
    "time": "2018-08-09"
  }]
}
```
