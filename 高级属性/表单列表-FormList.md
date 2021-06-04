# schema
```
{
  "type": "formList",
  "frontendId": "asfljwepuhasdas",
  "width": 800,
  "height": 300,
  "left": 0,
  "top": 50,
  "zIndex": 1,
  "config": {
    "title": "表单名称",
    "style": {"width": "40%"}
  }
}
```
#### 备注：推荐使用[复杂列表](/高级属性/复杂列表-%2D-ComplexList)，该组件完善度不高

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
| style | 组件样式 | 否 | object | react-css |
| title | 表单标题 | 否 | string |  |
| titleStyle | 表单标题样式 | 否 | object | react-css |
| listStyle | 列表整体样式 | 否 | object | react-css |
| itemDirection | 单项列表内容的布局方向 | 否 | string | 可选：'row', 'row-reverse', 'column', 'column-reverse' |
| itemStyle | 单项列表样式 | 否 | object | react-css |
| nameStyle | 单项列表名称样式 | 否 | object | react-css |
| contentStyle | 单项列表内容样式 | 否 | object | react-css |
| itemAction | 单项列表的点击事件 | 否 | object | 详见schema.config.itemAction |
| childComponents | 可自定义配置子基础组件 | 否 | array | 基础组件schema |
| action | 点击事件 | 否 | string | 详见 [事件](/事件) |
| actionData | 点击事件所需参数 | 否 | object | 详见 [事件](/事件) |

#### schema.config.itemAction：

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| action | 点击事件 | 否 | string | 详见 [事件](/事件) |
| actionData | 点击事件所需参数 | 否 | object | 详见 [事件](/事件) |

## 返回数据说明:

| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| list | 表单数据 | 是 | array | 详见：返回数据list说明 |
| childComponents | 可自定义配置子基础组件(后续可能会调整) | 否 | array | 基础组件schema |

## 返回数据说明:
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| name | 表单列表名称 | 是 | string |  |
| value | 表单列表的单项内容 / 完整的基础组件schema | 否 | string/object | 若为object 且包含 frontendId和type则进行组件解析 |

```
{
    "list": [{name: "名称", value: "内容"}],
    "childComponents": [{schema}],
}
```

##常规样式：
 ![image.png](/.attachments/image-5486f512-a47d-4df9-a795-28677559054d.png)
