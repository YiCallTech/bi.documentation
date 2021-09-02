# schema
```
{
  "size": "middle",
  "items": [
    {
      "maxTagCount": 1,
      "style": {
        "width": 240,
        "border": "4px solid rgba(17, 174, 255, .5)"
      },
      "type": "select",
      "key": "b"
    },
    {
      "style": {
        "width": 240,
        "border": "4px solid rgba(17, 174, 255, .5)"
      },
      "type": "input",
      "key": "aa"
    },
    {
      "format": "YYYY-MM-DD HH:mm:ss",
      "startKey": "start",
      "endKey": "end",
      "noUnix": true,
      "style": {
        "width": 440,
        "border": "4px solid rgba(17, 174, 255, .5)"
      },
      "type": "datePicker",
      "key": "b"
    }
  ],
  "style": {},
  "itemStyle": {
    "height": 56,
    "lineHeight": "48px",
    "marginRight": 20,
    "marginBottom": 20,
    "fontSize": 28,
    "fontFamily": "Source Han Sans SC",
    "color": "#fff"
  }
}
```

# 接口返回
```
{
  [
    {
      "key": "a",
      "label": "类型1",
      "value": 1
    },
    {
      "key": "b",
      "label": "类型2",
      "value": 11
    },
    {
      "key": "b",
      "label": "类型2",
      "value": 22
    },
    {
      "key": "c",
      "label": "类型2",
      "value": 111
    },
    {
      "key": "c",
      "label": "类型2",
      "value": 222
    },
    {
      "key": "d",
      "label": "类型1",
      "value": 1,
      "children": [
        {
          "value": "hangzhou",
          "label": "Hangzhou",
          "children": [
            {
              "value": "xihu",
              "label": "West Lake"
            }
          ]
        }
      ]
    },
    {
      "key": "e",
      "label": "类型2",
      "value": 2,
      "children": [
        {
          "value": "hangzhou",
          "label": "Hangzhou",
          "children": [
            {
              "value": "xihu",
              "label": "West Lake"
            }
          ]
        }
      ]
    }
  ]
}
```

## schema说明：
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| size | 筛选器大小 | 是 | string | 默认：middle |
| items | 筛选器组合 | 否 | array | 详见items说明 |
| postDataListFrontends | 筛选器更新组件的frontendId | 是 | array |  |
| style | 筛选器区域样式 | 否 | object | react-css |
| itemStyle | 筛选器容器样式 | 否 | object | react-css |

#### items说明：
| 名称 | 描述 | 必填 | 类型 | 备注 |
|--|--|--|--|--|
| label | 标题 | 否 | string |  |
| key | key值 | 是 | string | 唯一的key，用于接口数据的提取及传入 |
| type | 筛选器类型：搜索框：input、 下拉筛选框：select、树形筛选框：treeSelect、级联筛选框：cascade、单选：radio、多选：checkbox、时间范围筛选：datePicker | 是 | string |  |
| placeholder | 提示文案 | 否 | string |  |
| mode | 下拉框组件是否多选 | 否 | string | 默认：单选 |
| multiple | 树形筛选框组件是否多选 | 否 | bool | 默认：false |
| maxTagCount | 多选时最多显示多少个选中项 | 否 | number | 默认：1 |
| format | 时间格式：年：YYYY、年月：YYYY-MM、年月日：YYYY-MM-DD、年月日 时：YYYY-MM-DD HH、年月日 时分：YYYY-MM-DD HH:mm、年月日 时分秒：YYYY-MM-DD HH:mm:ss、时：HH、时分：HH:mm、时分秒：HH:mm:ss | 否 | number | 默认：1 |
| startKey | 开始时间的key | 是 | string | 默认：startTime |
| endKey | 结束时间的key | 是 | string | 默认：endTime |
| noUnix | 是否是毫秒时间戳 | 否 | bool | 默认：true |
| style | 分页器样式 | 否 | object |  |


## 接口返回说明:
接口返回为数组对象，根据items.key，从返回数据中取对应key的值，返回模型请参考：[数据来源](/数据来源.md)


| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| key | 与items.key相对应 | 是 | string |  |
| label | 可选项的标题 | 是 | string |  |
| value | 可选项的值 | 是 | string |  |
| children | 树形筛选框、级联筛选框的树形结构数据 | 是 | object | {"label": "label","value": "value","children": []} |