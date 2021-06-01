# schema
```
{
  "type": "list",
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
    "name": "列表",
    "isLoading": true,
    "pageIndex": 1,
    "pageSize": 10,
    "structure": [{
      "name": "标题",
      "key": "title",
      "styles": {
        "width": "40%",
      },
      "schema": {}
    }],
    "filter": [{
      "key": "aaa",
      "name": "tab选项",
      "type": "tab",
      "width": 260,
      "height": 30,
      "isSingle": false,
      "fontSize": 14,
      "color": 'red',
      "activeColor": 'red',
      "data": [{
        "name": "活动报名",
        "value": 1,
      }],
    }],
    "head": {
      "color": "#eee",
      "fontFamily": "PingFangSC-Regular",
      "fontSize": 14,
      "fontWidth": 500,
      "fontStyle": 500,
      "padding": "5px 0", // 10 || "5px 10px"
      "background": "rgba(178,255,255,.17)"
    },
    "list": {
      "height": 200,
      "action": "popupComponent",
      "actionData": {
        "popupType": '',
        "popupData": '',
        "isClearAll": true
      },
      "isAutoScroll": true,
      "isStopScrollingWhenHovered": true,
      "isScrollLoadMore": true,
      "backgroundInterval": "odd", // odd, even, all
      "backgroundColor": "rgba(15,182,217,.12)",
      "action": "",
      "actionData": "",
      "showOrder": true,
      "orderFirstStyle": {},
      "orderSecondStyle": {},
      "orderThirdStyle": {},
      "orderStyle": {},
    },
    "pagination": {
      "textAlign": "right", // left center right
    },
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
| name | 组件名称 | 否 | string |  |
| direction | 列表方向 | 否 | string | 默认row，可选column，row |
| isLoading | 加载数据时是否需要loading状态 | 否 | bool |  |
| pageIndex | 当前页码 | 是 | number |  |
| pageSize | 每页数量 | 是 | number |  |
| structure | 列表结构 | 是 | array | 详见schema.structure |
| filter | 列表筛选项配置属性 | 否 | array | 详见schema.filter |
| head | 列表头部配置属性 | 否 | object | 详见schema.head |
| list | 列表配置属性 | 是 | object | 详见schema.list |
| pagination | 列表分页配置属性 | 否 | object | 详见schema.pagination |
| listStyle | 列表样式 | 否 | object | react-css |
| itemStyle | 列表子项/行样式 | 否 | object | react-css |


#### schema.config.structure：

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| name | 名称 | 是 | string | 表头名称 |
| key | key值 | 是 | string | 唯一key值，用于data中的数据提取 |
| styles | 样式 | 是 | object | react-css，宽度必填，不然可能会导致页面错乱 |
| schema | schema | 否 | object | 组件schema，直接显示对应的组件（text, textShowCase组件如果text为空，会使用表格数据作为text的值） |
| actionDataKeyMap | 传给行子组件的参数key | 否 | object | {"title": "content"} 将行数据的title的数据以actionData: {"content": rowData[title]}d的形式传给行子组件 |

#### schema.config.filter:

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| key | key值 | 是 | string | 唯一key值，列表筛选项的key |
| name | 筛选项名称 | 是 | string / array | 日历组件需要传数组，["起始时间", "截止时间"] |
| type | 筛选项类型 | 是 | string | select、search、radio、tab、calendarPicker、link |
| width | 筛选项宽度 | 否 | string \ number | 10% \ 10 |
| height | 筛选项高度 | 否 | string \ number | 10% \ 10 |
| isSingle | 是否单选 | 否 | bool | 仅支持：select、radio、tab |
| fontSize | 字体大小 | 否 | number |  |
| color | 字体颜色，边框颜色 | 否 | string |  |
| isButton | 是否展示button | 否 | bool | type为search时，控制搜索按钮的显隐 |
| activeColor | 高亮时字体边框颜色 | 否 | string | 仅支持：radio、tab |
| data | 可选数据/url地址 | 否 | array | select、radio、tab、link为必填，link时为url地址，详见schema.filter.data |

#### schema.config.filter.data:

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| name | 可选项名称 | 是 | string |  |
| value | 可选项的值 | 是 | string / number |  |

#### schema.config.head:

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| color | 颜色 | 否 | number |  |
| fontFamily | 字体 | 否 | string |  |
| fontSize | 字体大小 | 否 | string |  |
| fontWeight | 字体粗细 | 否 | string |  |
| fontStyle | 字体样式 | 否 | string |  |
| padding | 内边距 | 否 | string |  |
| background | 背景 | 否 | string |  |


#### schema.config.list:

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| height | 列表高度 | 否 | number | 不给则显示所有列表数据，自动滚动加载更多数据及滚动加载更多数据时为必填 |
| isAutoScroll | 是否自动滚动 | 否 | bool | 需要指定列表高度-height |
| isStopScrollingWhenHovered | 滚动时鼠标移入是否暂停 | 否 | bool |  |
| isScrollLoadMore | 滚动时是否自动加载数据 | 否 | string | 需要指定列表高度-height |
| color | 颜色 | 否 | number |  |
| fontFamily | 字体 | 否 | string |  |
| fontSize | 字体大小 | 否 | string |  |
| fontWeight | 字体粗细 | 否 | string |  |
| fontStyle | 字体样式 | 否 | string |  |
| padding | 内边距 | 否 | string |  |
| backgroundInterval | 列表背景间隔 | 否 | string | odd, even, all |
| backgroundColor | 列表背景颜色 | 否 | string |  |
| interval | 每行之间的间隙 | 否 | number |  |
| action | 列表点击事件 | 否 | string | 详见 [事件](/事件) |
| actionData | 列表点击事件所需参数 | 否 | object | 详见 [事件](/事件) |
| showOrder | 是否显示序号 | 否 | bool |  |
| orderColor | 序号颜色 | 否 | array |  |
#### schema.config.pagination:

| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| textAlign | 排版方向 | 否 | string | left, center, right |

#### dataApi:
根据不同的列表实例由前后端协调数据。
| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| schema.structure.key | 列表key值 | 是 | string |  |
| KEY_styles | 指定列指定单元格的样式 | 否 | object | react-css |
```
{
  [{
    "title": "tab选项",
    "title_styles": {"color": "#FF0000"},
    "content": "tab选项tab选项tab选项",
    "time": "2018-08-09"
  }]
}
```

#### 备注：
支持的功能: 分页刷新数据（pagination）、定时刷新数据（refreshInterval）、自动滚动加载更多数据（isAutoScroll + isScrollLoadMore）、自动滚动（isAutoScroll）、滚动加载更多数据（isScrollLoadMore）、滚动时鼠标移入暂停滚动（isStopScrollingWhenHovered）
数据的更新模式（只取一种）:分页刷新数据 > 定时刷新数据 > 自动滚动加载更多数据 > 滚动加载更多数据
