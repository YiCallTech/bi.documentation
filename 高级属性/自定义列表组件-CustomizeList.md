# schema
```
{
  "structure": [
    {
      "key": "car",
      "name": "车牌号",
      "styles": {
        "width": "20%"
      }
    },
    {
      "key": "parkingLot",
      "name": "所在停车场",
      "styles": {
        "width": "40%"
      }
    },
    {
      "key": "street",
      "name": "所属街道",
      "styles": {
        "width": "20%"
      }
    },
    {
      "key": "time",
      "name": "停车时间",
      "styles": {
        "width": "20%"
      }
    }
  ],
  "headStyles": {
    "height": 48,
    "padding": "0 20px",
    "fontSize": 24,
    "color": "rgba(255,255,255,.5)",
    "background": "linear-gradient(90deg, rgba(0, 64, 191, 0.12) 0%, rgba(0, 64, 191, 0.2) 50%, rgba(0, 64, 191, 0.12) 100%)"
  },
  "listRowStyles": {
    "minHeight": 56,
    "padding": "0 20px",
    "fontSize": 24
  },
  "listOddRowStyles": {
    "background": "linear-gradient(90deg, rgba(0, 64, 191, 0.06) 0%, rgba(0, 64, 191, 0.1) 50%, rgba(0, 64, 191, 0.06) 100%)"
  },
  "listMaxHeight": 224,
  "autoScroll": true
}
```

# 接口返回
```
{
  [
    {
      "car": "颚A5J***",
      "parkingLot": "浙江出版物资大厦",
      "street": "文晖街道",
      "time": "2021-10-21"
    },
    {
      "car": "颚A5J***",
      "parkingLot": "浙江出版物资大厦厦",
      "street": "文晖街道",
      "time": "2021-10-21"
    },
    {
      "car": "颚A5J***",
      "parkingLot": "浙江出版物资大厦",
      "street": "文晖街道",
      "time": "2021-10-21"
    },
    {
      "car": "颚A5J***",
      "parkingLot": "浙江出版物资大厦",
      "street": "文晖街道",
      "time": "2021-10-21"
    },
    {
      "car": "颚A5J***",
      "parkingLot": "浙江出版物资大厦",
      "street": "文晖街道",
      "time": "2021-10-21"
    }
  ]
}
```

# 备注：
支持的功能: 分页刷新数据（pagination）、定时刷新数据（refreshInterval）、自动滚动加载更多数据（autoScroll + scrollLoadMore）、自动滚动（autoScroll）、滚动加载更多数据（scrollLoadMore）、滚动时鼠标移入暂停滚动（stopScrollingWhenHovered）
数据的更新模式（只取一种）:定时刷新数据 > 分页刷新数据 > 自动滚动加载更多数据 > 滚动加载更多数据


## schema说明：
| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| pageSize | 每页数量 | 是 | number |  |
| structure | 列表结构 | 是 | array | 详见structure |
| autoScroll | 自动滚动配置 | 否 | bool |  |
| scrollLoadMore | 滚动加载更多数据 | 否 | bool |  |
| stopScrollingWhenHovered | 鼠标移入停止滚动 | 否 | bool |  |
| pagination | 分页配置，同 antd.pagination | 否 | object |  |
| headStyles | 表头样式 | 否 | object | react-css |
| headItemStyles | 表头子项样式 | 否 | object | react-css |
| listStyles | 列表区域样式 | 否 | object | react-css |
| listRowStyles | 列表行样式 | 否 | object | react-css，列表间的间隔应该使用listRowInterval，不建议在listRowStyles中使用margin，会造成动画卡顿 |
| listOddRowStyles | 列表奇数行样式 | 否 | object | react-css |
| listEvenRowStyles | 列表偶数行样式 | 否 | object | react-css |
| listColStyles | 列表子项样式 | 否 | object | react-css |
| listMaxHeight | 列表区域最高高度 | 否 | number | scrollLoadMore时必填，否则无法触发数据加载 |
| listRowInterval | 列表每行之间的间隔 | 否 | number |  |
| rowKey | 列表的key | 否 | string | 默认showId |
| rowAction | 列表每行点击事件 | 否 | object | 详见 [事件](/交互事件.md) |
| data | 列表静态数据 | 否 | array | 参考接口返回数据 |


#### structure：
| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| name | 名称 | 是 | string | 表头名称 |
| key | key值 | 是 | string | 唯一key值，用于data中的数据提取 |
| styles | 每项样式 | 否 | object | react-css |
| template | html标签模拟 | 否 | string | 可配置html标签，并将"{}"替换为接口返回中的数据 |
| colAction | 列表每列点击事件 | 否 | object | 详见 [事件](/交互事件.md) |


## 接口返回说明:
接口返回为数组对象，根据structure的结构，从返回数据中取对应key的值，返回模型请参考：[数据来源](/数据来源.md)


| 名称 | 描述 | 必填 | 类型 |备注 |
|--|--|--|--|--|
| [structure.key] | 列表key的值 | 是 | string |  |