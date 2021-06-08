# schema

```json
{
  "defaultTab": 1,
  "direction": "column",
  "carousel": false,
  "carouselInterval": 10,
  "tabsType": "",
  "autoHeight": false,
  "hideTabs": false,
  "tabStyle":{},
  "tabActiveStyle":{},
  "items":[]
}
```

#### Schema说明:
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| defaultTab | 默认当前显示tab 下标 | number | 否 | 1 |
| direction | tab排布 row，column | String | 否 | row |
| carousel | tab是否自动轮播 | bool | 否 | false |
| carouselInterval | 自动轮播间隔时长 | number | 否 | 10 |
| tabsType | tab类型 type1，type2，type3 | String | 否 | type1 |
| autoHeight | 自动高度 | bool | 否 | false |
| hideTabs | 是否隐藏tab组件 | bool | 否 | false |
| tabStyle | tab样式 | Object | 否 |  |
| items | 子组件（参考items说明） | Array | 是 |  |

### Schema.config.items
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| iconType | 图标类型 img，antd | String | 否 | |
| iconStyle | 图标样式 | Object | 否 |  |
| activeIconStyle | tab高亮时的图标样式 | Object | 否 |  |
| icon | iconType - hideTabs type |  String | 否 |  |
| activeIcon | tab高亮时的icon， iconType - img：需要传图片url；antd：antd的icon type |  String | 否 |  |
| name | tab名称 |  String |  |
| formatter | 格式化字符串 | String | 否 |  |
| frontendId | 子组件 id | Array | 是 |  |
| postDataList | 子组件传参 | Array | 否 |  |

### Schema.config.items.postDataList.postDataMap
| 参数名称 | 参数说明 | 数据类型 | 是否必填 | 默认值 |
|--|--|--|--| -- |
| frontendId | 子组件 id | Array | 是 |  |
| updateData | frontendId对应子组件的传参 | object | 否 |  |